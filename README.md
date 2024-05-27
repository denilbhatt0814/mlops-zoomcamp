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

## 02-experiment-trackng

- understood following concepts
  1. ml experiment: the process of building an ml model
  2. experiment run: each trail in an ml experiment
  3. run artifact: any file associated with ml run
  4. experiment metadata
- experiment tracking makes note of relevant info from ml exp.
  - enviroments
  - source code
  - data
  - hyperparameters
  - models
  - ...
- 3 main reasons for experiment tracking
  1. reproducability
  2. organization
  3. optimization
- simplest tool for exp tracking is spreadsheets; but lacks a standard format, visiblity, is error prone
- ml flow: foss tool for ml lifecycle; contains 4 main modules:
  1. tracking
  2. models
  3. model registry
  4. projects
- mlops & ml lifecycle:
  1. data sourcing
  2. data labeling
  3. data versioning
  4. experiment tracking
  5. model versioning
  6. model deployment
  7. prediciton monitoring
- usually model management can be done by creating multiple models, but the issue is that it can be error prone, have no versioning, and
  has no model lineage
- model registry; from tracking server to model registry if model if production ready
- model registry stores models with labels called as stages: "staging", "production", "archive"
- model registry is not responsible for deployments; there must be ci/cd pipeline to handle that
