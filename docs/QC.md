# Overview of the quality assurance and quality control (QA/QC) pipeline

## QA/QC in FLAKE - overview

![Screenshot](img/qc_overview.png)

## From issue reporting to data curation

The issue can have four different states:

- **Draft**: the issue has been created by the reporter but not reviewed by the data curator/advisor yet. At this stage, the reporter can still edit the issue. The data is still visible in Datalakes to the users.
- **Confirmed**: the issue has been reviewed and confirmed by the data curator/advisor. The data is masked in Datalakes but remains present in the database.
- **Validated**: the issue has been validated by the data curator/advisor. A merge request is created in the instrument repository to permanently remove the data from Datalakes.
- **Closed**: the issue has been closed after the merge request has been accepted and merged in the instrument repository. The data is permanently removed from Datalakes.

### Sequence diagram

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
