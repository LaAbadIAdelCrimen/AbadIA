# Wiki Schema: abadIA (Teaching Edition)

## Domain
Software refactoring from Vibe Coding to Harness Engineering v3.0, focused on educational production (Book, Podcast, Medium).

## Conventions
- Every step of the refactoring must be documented with an "Atomic Teaching" mindset.
- File names: lowercase, hyphens (e.g., `harnessing-the-authenticator.md`).
- Every page must have a `## The Why` section explaining the HE technology behind the change.
- Outbound links: Minimum 2 to other abadIA wiki pages + 1 to the central Research Hub (`~/wiki`).

## Frontmatter
```yaml
---
title: Page Title
created: YYYY-MM-DD
updated: YYYY-MM-DD
type: concept | step | entity | production-lead
tags: [he-v3, teaching, refactoring, abadia]
step_number: N
target_media: [book, podcast, medium, video]
---
```

## Special Sections for Education
- **`## Technical Concept`**: Deep dive into the HE v3.0 theory applied.
- **`## The Lesson`**: How to teach this specific step to a human developer.
- **`## Visual Cues`**: Description of what should be in the associated diagram/Excalidraw.
