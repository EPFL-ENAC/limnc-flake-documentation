# Overview of the quality assurance and quality control (QA/QC) pipeline

## QA/QC in FLAKE - overview

```mermaid
graph LR
  subgraph LéXPLORE
  A[Sensors] --> B[L0 data]
  A --> C[Tethis pre-processing] --> B
  end
  subgraph Data pipeline
  B --> D[EAWAG]
  E[Metadata] --> D
  D --> F[Cloud server]
  F --> G[Quality assessment]
  G --> H[L1 data]
  H --> I[Processing]
  I --> J[L2 n+1 data]
  J --> K[Datalakes]
  L[QA JSON] --> G
  G --> M[Metadata]
  K --> N[Pull request on Renku]
  N --> O[Validation by code maintainer]
  O --> P[events.csv] --> F
  end
```

## Submission of a maintenance report - Sequence diagram

The following diagram describes the flow of a submission by a user on Datalakes, the QA/QC process by the data curator and/or advisor, and their relation to the web and server aspects of Datalakes as well as the instrument repository.

```mermaid
sequenceDiagram
  participant reporter as Reporter
  participant maintainer as Maintainer
  participant james as Owner
  participant datalakes as Datalakes (web)
  participant datalakes_node as Datalakes (server)
  participant gitlab as Gitlab

  reporter ->>+ datalakes: add maintenance report
  datalakes ->>+ gitlab: create issue
  datalakes ->>- datalakes_node: create maintenance report + issue id
  gitlab -->>- maintainer: issue created email
  Note over reporter,datalakes: Maintenance report applied to data viz on-demand
  %% opt From datalakes
    maintainer ->>+ datalakes: confirm maintenance report
    datalakes ->> gitlab: issue label = "confirmed"
    datalakes ->>- datalakes_node: state = "confirmed"
  %% end
  %% opt From Gitlab
  %%  maintainer ->> gitlab: issue label = "confirmed"
  %%  gitlab ->>+ datalakes_node: webhook - issue updated
  %%  datalakes_node ->>- datalakes_node: state = "confirmed"
  %% end
  Note over reporter, datalakes: Maintenance report applied to data viz for all
  maintainer ->>+ datalakes: resolve maintenance report
  datalakes ->>+ gitlab: create merge request (events.csv)
  datalakes ->>- datalakes_node: update maintenance report + merge id
  gitlab -->> james: merge request created email
  james ->> gitlab: close merge request
  gitlab -->>+ datalakes_node: webhook - merge request updated
  datalakes_node ->>- datalakes_node: close maintenance report
  Note over reporter, gitlab: Maintenance report applied to data pipeline
```
