# Model Deployment and Predition Service
  * This chapter discuss the steps after the model is developed and ready for serving. It moves from development environment to Staging, testing and production environment
  * Production is a spectrum, for some team - its generating plots in notebook and for other team - its a about serving for many users
  * Simplest form of serving is - expose it as a endpoint using Flask/Fast API and then run the container along with dependency in Cloud
  * Hard part is serving millions of user, having 99% uptime, low latency etc
  * Sometimes model needs to be exported to handoff to deployment team. Exporting is sometimes called as Model serilaization. There are two parts to the process of exporting: the model definitions and model parameters value

## Machine Learning Deployment Myths
* Myth 1: You only deploy one or two models at a time : Academic Vs Industry
* Myth 2: If we dont do anything, Model performance remains the same : Concept, data distribution shifts
* Myth 3: You wont need to update your models as much: Model re-training frequency
* Myth 4: Most ML Engineers Dont Need to Worry about Scale: Number of request need to be served or predicted

## Batch Prediction Vs Online Prediction Vs Streaming Predictions
* Fundamental design decision - either to serve by Batch prediction Or by Online prediction
* Batch prediction - uses only batch features. Online prediction - either uses batch feature or batch features and streaming features ( Called streaming prediction)
 
    | Batch | Online | Streaming |
    |---|---|---|
    | Prediction generated and stored | Prediction generated as the request arrives | Prediction generated as the request arrives |
    | aSynchronous prediction | Synchronous prediction | Synchronous prediction |
    | ex: Netflix recommendation | eg: Google Translate | eg: Delivery time prediction |
    | Batch features | batch features | Batch and steaming features |
    | high throughput | low latency | Latest features values |
    | Generate prediction for all users | Generate features for current users | Generate features for current users |
    | <img width="555" alt="image" src="https://github.com/arunachalamev/Learning-Notes/assets/249746/6e3efc6c-cd49-494f-8d2f-4f19a3b376f1"> | <img width="554" alt="image" src="https://github.com/arunachalamev/Learning-Notes/assets/249746/6cf97105-a266-42e6-b03b-6a0ecb8f9b62"> | <img width="565" alt="image" src="https://github.com/arunachalamev/Learning-Notes/assets/249746/258d35db-764b-4e77-8e6e-602271dbcb6a"> |


* In some use case, batch and online prediction used side by side. eg: restaurant recommendation using batch prediction and then food item predicition using online predicition
* Academic uses online prediction, because it uses simple endpoint based integration for generating predictions. However, the latency might be higher for generating the predictions. To overcome, we might generate prediction before hand and sore which leads to batch predictions
* Batch prediction can reduce inference latency for complex model by precomputing them. However, they are less reponsive to changing users preference. For eg: Netflix recommendation for the current mood of the user
* Another issue with Batch prediction, we need to know the request upfront - like recommendation. For case of unpredictable queries, ( eg: translate ) we need to use online prediction
* Non catastrophic application , we can use Batch predictions. For time crucial applications, we need to use online predictions
* Legacy system mainly used batch prediction, since the techonlogy was mainly dominated by big data processing components like MapReduce framework. Recent advancement in streaming technologies and feature stores, enabled for unified frameword for batch and online predictions


## Faster Inference
There are three approaches to reduce inference latency - make model smaller (model compression), make the hardware faster, make faster inference (inference optimization).
### Model Compression
* Common Four type of techniques for Model Compression
  - **Low-Rank-optimization:** Replace high dimensional tensors to lower-dimensional tensors. For example: compact convolutional filters
  - **Knowledge distillation:** Smaller model (student) is tranied to mimic a larger or ensemble models (teacher). Example: DistillBert and BERT models. Pros: work irrespective of difference in architecture b/w student and teacher model. Cons: Student is highly dependent on availability of teacher network. 
  - **Pruning:** Idea of pruning for NN is borrowed from decision trees. Either we can remove the less important node (changes architecture) or setting the least useful parameter to zero (no change to architecuture)
  - **Quantization:** Reduce the size of model by using fewer bits to represent model parameters. It reduces model memory footprint and also improves the computational speed.
 
 ### ML on the cloud and on the Edge
* Running model on cloud is easier due to exitence of managed cloud services. They allow to host the model, expose the endpoint for requesting prediction and also enables backend computations. However, the drawback of cloud computing is increasing cloud cost. 
* Model are moved toward edge computing for various reasons: lower cost, can serve no internet location, less bandwidth usage since data need not be uploaded, privacy and GDPR are taken care. However, the edge devices needs to be powerful enough to run models. Hardware are being developed to achieve edge computing. 

### Model Optimization
* Two ways to optimize ML models: Locally (optimize set of operators) and Globally(optimize entire computation graph).
* There are 4 common technique employed for local optimization, namely - Vectorization, Paralleization, Loop tilting, Operator fusion.
* Another approach is to use ML to optimize ML models - like using ML to find the optimal architecture, optimal initial weight etc
