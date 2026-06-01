---
fields:
  - id: title
    name: title
    type: Input
  - id: platform
    name: platform
    options:
      '0': linkedin
    type: Select
  - id: status
    name: status
    options:
      '0': generating
      '1': draft
      '2': queued
      '3': published
      '4': failed
    type: Select
  - id: coverImageId
    name: coverImageId
    type: Input
  - id: documents
    name: documents
    type: Multi
  - id: publishedAt
    name: publishedAt
    type: Input
  - id: platformPostId
    name: platformPostId
    type: Input
  - id: sourceEntityId
    name: sourceEntityId
    type: Input
  - id: sourceEntityType
    name: sourceEntityType
    options:
      '0': post
      '1': deck
    type: Select
filesPaths: social-post
---
