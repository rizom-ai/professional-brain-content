filters:
  and:
    - file.inFolder("anchor-profile")
views:
  - name: All Anchor Profiles
    order:
      - file.name
      - name
      - description
      - avatar
      - website
      - email
      - socialLinks
      - tagline
      - intro
      - story
      - expertise
      - currentFocus
      - availability
    type: table