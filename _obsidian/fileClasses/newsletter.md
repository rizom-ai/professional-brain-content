---
fields:
  - name: subject
    type: Input
  - name: status
    type: Select
    options:
      "0": draft
      "1": queued
      "2": published
      "3": failed
  - name: entityIds
    type: Multi
  - name: scheduledFor
    type: Input
  - name: sentAt
    type: Input
  - name: buttondownId
    type: Input
  - name: sourceEntityType
    type: Input
---
