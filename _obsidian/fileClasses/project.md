---
fields:
  - id: title
    name: title
    type: Input
  - id: slug
    name: slug
    type: Input
  - id: status
    name: status
    options:
      '0': generating
      '1': draft
      '2': published
      '3': failed
    type: Select
  - id: publishedAt
    name: publishedAt
    type: Input
  - id: description
    name: description
    type: Input
  - id: year
    name: year
    type: Number
  - id: coverImageId
    name: coverImageId
    type: Input
  - id: ogImageId
    name: ogImageId
    type: Input
  - id: url
    name: url
    type: Input
filesPaths: project
---
