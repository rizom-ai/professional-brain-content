filters:
  and:
    - file.inFolder("post")
views:
  - name: All Posts
    order:
      - file.name
      - title
      - slug
      - status
      - publishedAt
      - excerpt
      - author
      - coverImageId
      - seriesName
      - seriesIndex
      - ogImage
      - ogDescription
      - twitterCard
      - canonicalUrl
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
      - excerpt
      - author
      - coverImageId
      - seriesName
      - seriesIndex
      - ogImage
      - ogDescription
      - twitterCard
      - canonicalUrl
    type: table