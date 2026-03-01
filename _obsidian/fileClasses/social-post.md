---
fields:
  - name: title
    type: Input
  - name: platform
    type: Select
    options:
      "0": linkedin
  - name: status
    type: Select
    options:
      "0": draft
      "1": queued
      "2": published
      "3": failed
  - name: coverImageId
    type: Input
  - name: publishedAt
    type: Input
  - name: platformPostId
    type: Input
  - name: sourceEntityId
    type: Input
  - name: sourceEntityType
    type: Select
    options:
      "0": post
      "1": deck
---
