filters:
  and:
    - file.inFolder("social-post")
views:
  - name: All Social Posts
    order:
      - file.name
      - title
      - platform
      - status
      - coverImageId
      - publishedAt
      - platformPostId
      - sourceEntityId
      - sourceEntityType
    type: table
  - groupBy:
      direction: ASC
      property: status
    name: By Status
    order:
      - file.name
      - title
      - platform
      - status
      - coverImageId
      - publishedAt
      - platformPostId
      - sourceEntityId
      - sourceEntityType
    type: table
