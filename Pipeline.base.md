filters:
  and:
    - or:
        - file.inFolder("post")
        - file.inFolder("deck")
        - file.inFolder("link")
        - file.inFolder("project")
        - file.inFolder("social-post")
        - file.inFolder("newsletter")
    - status != "published"
views:
  - groupBy:
      direction: ASC
      property: status
    name: Pipeline
    order:
      - file.name
      - file.folder
      - status
    type: table