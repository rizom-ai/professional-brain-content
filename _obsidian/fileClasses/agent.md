---
fields:
  - id: name
    name: name
    type: Input
  - id: kind
    name: kind
    options:
      '0': professional
      '1': team
      '2': collective
    type: Select
  - id: organization
    name: organization
    type: Input
  - id: brainName
    name: brainName
    type: Input
  - id: url
    name: url
    type: Input
  - id: did
    name: did
    type: Input
  - id: status
    name: status
    options:
      '0': active
      '1': archived
    type: Select
  - id: discoveredAt
    name: discoveredAt
    type: Input
  - id: discoveredVia
    name: discoveredVia
    options:
      '0': atproto
      '1': manual
    type: Select
filesPaths: agent
---
