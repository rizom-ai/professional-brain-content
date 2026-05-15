---
title: OG images and PDF carousels
status: new
priority: medium
requested: 1
---
## Goal

Add generated OG images and PDF carousel support using the existing template system.

## Approach

- Reuse `createTemplate` and existing Zod/data-source flow.
- Add media render targets to templates, starting with `image` and optionally `pdf`.
- Use Satori + Resvg for PNG output.
- Use pdf-lib to assemble carousel PNG pages into PDFs.
- Keep Satori-specific components small and separate from full web components.

## OG images

- Generate OG PNGs from template data.
- Store generated PNGs as existing `image` entities.
- Add optional `ogImageId` support.
- Fallback: `ogImageId` → `coverImageId` → site default.
- Ensure head metadata emits absolute OG image URLs.

## PDF carousels

- Use template-driven carousel cards, not Playwright screenshots.
- Render each carousel slide to PNG via Satori + Resvg.
- Assemble slides into a PDF with pdf-lib.
- Store PDF as a future `document` or `media-asset` entity.
- Attach generated PDF to `social-post` media.

## Publishing

- Extend publish contract from single `imageData` to `media[]`.
- Support image and document media.
- Publish LinkedIn PDF carousels as document/PDF posts.

## Implementation order

1. Add image renderer support to template/render contracts.
2. Add shared Satori/Resvg media rendering helper.
3. Generate OG PNGs into `image` entities.
4. Wire `ogImageId` into site head generation.
5. Add document/media-asset entity for PDFs.
6. Add carousel PDF generation.
7. Extend social publishing media contract.
8. Add LinkedIn document upload support.
