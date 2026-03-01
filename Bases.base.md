filters:
  and:
    - file.inFolder("base")
views:
  - name: All Bases
    order:
      - file.name
      - title
    type: table