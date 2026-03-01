filters:
  and:
    - file.inFolder("brain-character")
views:
  - name: All Brain Characters
    order:
      - file.name
      - name
      - role
      - purpose
      - values
    type: table