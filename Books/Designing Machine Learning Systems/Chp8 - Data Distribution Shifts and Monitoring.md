# Data Distribution Shifts and Monitoring
* Deploying a mode isnt the end of the process. A Model's performance degrades over time in production

## Causes of ML System Failures
* In any ML system, we mostly care about Operational metrics and Performance metrics. For example, in case of Translation app, operation metrics is the result returned within a sec, and performance metrics is the accurate oft the translation
* Operation expectations are easier to track and detect. Performance expectations are harder to detect and track
* Two types of failures discussed: Software system Failure and ML- Specific Failures

  ### Software System Failures:
  - Dependency Failure
  - Deployment Failure
  - Hardware Failure
  - Downtime or crashing

  ### ML-Specific Failures:
  * ML specific failures are more dangerous than non-ML specific failures since they are hard to detect and fix
  * Example: data collection & preprocessing problems, poor hyperparameters, change in training and inference pipeline etc

    #### Production data differing from training data
    - The assumption of production data distribution is same as training data is incorrect for two reasons, namely, the sampled training data wont cover all the production scenarios and real world data is not a startionary distribution. for eg: wuhan search before and after covid
    #### Edge cases
    - These are the cases where the model makes catastrophic mistake, for eg: car accident due to self driving car algorithms
    #### Degenerate Feedback loops
    - Happens when a predictions themselves influences the feedback, in turn, influences the next iteration of the model. For eg: recommendation system, resume-screening model
    - If no action taken to identify and resolve degenerate feedback loop, the model will perform suboptimal
        ##### Detecting degenerate feedback loops
        - Difficutl to detect in offline system. In case of such as recommendation engine, we can measure the popularity diversity even in offline.
        - Hit rate against the popularity - divide the items into bucket and measure the perfromance of the model in each bucket
        ##### Correcting degenerate feedback loops
        - Use randomization and use positional features

  ### Data Distribution Shifts
    - Source distribution - distribution of data the models is trained on. Targed distribution - distribution of data the model is inferenced on
    - Both can change, so we have
        - covariate shift - when P(X) changes but P(Y|X) remains the same. Input distribution changes. Eg: when training data is artifically altered to make it easire for model to learn.
        - label shift - when P(Y) changes but P(X|Y) remains the same. Output distribution changes. when input changes, output changes. But not all covariate shifts results in label shift
        - concept shift - P(Y|X) changes but P(X) remains same. Same input but different output. In many cases, concept drifts are cyclic or seasonal. for example - rideshare price will fluctuate on weekdays vs weekeds. Compaines will have different model for seasonal or cyclic drifts.

//Test from VS code- test

