# Accessibility (a11y)

## Semantic HTML
- Use the correct HTML element for its purpose (`button` for actions, `a` for navigation, `nav`, `main`, `header`, `footer`).
- Do not use `div` or `span` for interactive elements.
- Use heading levels (`h1`–`h6`) in logical order without skipping.

## ARIA
- Use ARIA attributes only when semantic HTML is insufficient.
- Prefer native HTML semantics over ARIA roles (e.g., `<button>` over `<div role="button">`).
- Always pair `aria-labelledby` or `aria-label` with custom widgets.
- Use `aria-live` regions for dynamic content updates.

## Keyboard Navigation
- All interactive elements must be reachable and operable via keyboard.
- Maintain a logical tab order (avoid positive `tabindex` values).
- Provide visible focus indicators — never remove `outline` without replacement.
- Support Escape to close modals/popups, Enter/Space to activate buttons.

## Forms
- Every input must have an associated `<label>` (use `for`/`id` pairing or nesting).
- Group related inputs with `<fieldset>` and `<legend>`.
- Provide clear error messages associated with the invalid field (`aria-describedby`).

## Media and Visual
- Provide meaningful `alt` text for informative images; use `alt=""` for decorative ones.
- Ensure a minimum contrast ratio of 4.5:1 for text (3:1 for large text).
- Do not rely solely on color to convey information.
- Support reduced motion preferences (`prefers-reduced-motion`).

## Testing
- Test with keyboard-only navigation.
- Use automated tools (axe, Lighthouse) as a baseline.
- Validate with a screen reader for critical flows.

