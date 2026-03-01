filters:
  and:
    - file.inFolder("link")
views:
  - name: All Links
    order:
      - file.name
      - status
      - title
      - url
      - description
      - keywords
      - domain
      - capturedAt
      - source
    type: table
  - groupBy:
      direction: ASC
      property: status
    name: By Status
    order:
      - file.name
      - status
      - title
      - url
      - description
      - keywords
      - domain
      - capturedAt
      - source
    type: table