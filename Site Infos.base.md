filters:
  and:
    - file.inFolder("site-info")
views:
  - name: All Site Infos
    order:
      - file.name
      - title
      - description
      - copyright
      - logo
      - themeMode
      - cta
    type: table