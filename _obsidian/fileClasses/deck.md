---
fields:
  - name: title
    type: Input
  - name: slug
    type: Input
  - name: description
    type: Input
  - name: author
    type: Input
  - name: status
    options:
      - '0': draft
      - '1': queued
      - '2': published
    type: Select
  - name: publishedAt
    type: Input
  - name: event
    type: Input
  - name: coverImageId
    type: Input
---
