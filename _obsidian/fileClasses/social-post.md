---
fields:
  - name: title
    type: Input
  - name: platform
    options:
      - '0': linkedin
    type: Select
  - name: status
    options:
      - '0': draft
      - '1': queued
      - '2': published
      - '3': failed
    type: Select
  - name: coverImageId
    type: Input
  - name: publishedAt
    type: Input
  - name: platformPostId
    type: Input
  - name: sourceEntityId
    type: Input
  - name: sourceEntityType
    options:
      - '0': post
      - '1': deck
    type: Select
filesPaths: social-post
---
