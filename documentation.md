# Documentation

## Inline Comments
- Comment **why**, not **what** — the code itself shows what it does.
- Use comments for non-obvious decisions, workarounds, or business rules.
- Keep comments up to date — stale comments are worse than no comments.
- Remove commented-out code; use version control for history.

## API Documentation
- Add doc comments (Javadoc, JSDoc) to all public classes, methods, and interfaces.
- Include: purpose, parameters, return values, exceptions/errors, and usage examples.
- Document edge cases and constraints (e.g., "must not be null", "thread-safe").

## README
- Every module/project should have a README covering: purpose, setup, usage, and contribution guidelines.
- Update the README when public behavior or setup steps change.
- Prefer concrete examples over abstract descriptions.

## Architecture and Design
- Document significant architectural decisions (ADRs or inline docs).
- Include diagrams for complex flows (keep them minimal and up to date).
- Explain the "why" behind non-obvious patterns or trade-offs.

## Changelog
- Maintain a changelog for user-facing changes.
- Use categories: Added, Changed, Deprecated, Removed, Fixed, Security.
- Reference issue/ticket numbers for traceability.

## Style
- Use clear, direct language — avoid jargon when a simpler term works.
- Be concise — respect the reader's time.
- Use consistent formatting (Markdown, heading levels, code fences).
- Prefer bullet points and tables over long paragraphs for reference material.

