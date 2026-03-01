---
fields:
  - name: title
    type: Input
  - name: slug
    type: Input
  - name: status
    type: Select
    options:
      "0": draft
      "1": queued
      "2": published
  - name: publishedAt
    type: Input
  - name: excerpt
    type: Input
  - name: author
    type: Input
  - name: coverImageId
    type: Input
  - name: seriesName
    type: Input
  - name: seriesIndex
    type: Number
  - name: ogImage
    type: Input
  - name: ogDescription
    type: Input
  - name: twitterCard
    type: Select
    options:
      "0": summary
      "1": summary_large_image
  - name: canonicalUrl
    type: Input
---
