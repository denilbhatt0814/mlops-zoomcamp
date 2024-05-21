# mlops-zoomcamp

## 01-intro

- analysed nyc taxi dataset; simple model for predicting the duration of a ride
- understood the basic outline of ml pipeline:
  1. load and prepare data -> pre-procesing of data
  2. vectorize -> gives out dictionary vectorizer
  3. train -> this finally outputs a model
- outline of model monitoring and mlops maturity model; ref: [ms learn](https://learn.microsoft.com/en-us/azure/architecture/ai-ml/guide/mlops-maturity-model)
- learnt about mlops matutity models (5 levels)

  - l0 - no mlops: all code on jupyter notbook, no automation; mostly for poc
  - l1 - devops, no mlops: automated releases, unit tests, ci/cd, ops metrics; best practices of software development but nothing related to ml, lacks experiment tracking, reproducability and ds seperated from engineers
  - l2 - automated training: have training pipeline/scripts, experiment tracking, use of model registery(training automated, deployment may not be); ds work with engineers
  - l3 - automated deployment: super low friction deployments, could be new stage in training pipeline, capabilities of a/b testing, model monitoring
  - l4 - full mlops automation: auto training, auto deploy, full monitoring
    > note: in most cases while having 1-2 models then level 1 is sufficient, the idea of moving to higher maturity level shall develop when ml cases grow to 3 or 3+.
