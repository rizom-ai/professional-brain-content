filters:
  and:
    - file.inFolder("project")
views:
  - name: All Projects
    order:
      - file.name
      - title
      - slug
      - status
      - publishedAt
      - description
      - year
      - coverImageId
      - url
    type: table
  - groupBy:
      direction: ASC
      property: status
    name: By Status
    order:
      - file.name
      - title
      - slug
      - status
      - publishedAt
      - description
      - year
      - coverImageId
      - url
    type: table
