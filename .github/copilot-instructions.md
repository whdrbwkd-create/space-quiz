# Copilot instructions

## Project shape

Orbit is a single-page space quiz implemented entirely in `index.html`. The document contains the page markup, inline CSS, the question bank, and the quiz controller; there is no framework, module bundler, or backend. The quiz flow is driven by `questions` and the `index`, `score`, and `answered` state: `renderQuestion()` creates answer buttons, `selectAnswer()` locks and grades a response and displays its fact, and `showResults()` displays the final score. Restart resets the state and returns to the first question.

## Build, test, and lint

There is no package manifest, build script, test runner, or linter configured. To run the app, open `index.html` directly in a browser. There is no automated single-test command; verify behavior manually by answering questions, advancing through the final result, and using “Explore again.”

## Code conventions

- Keep the app dependency-free and self-contained in `index.html` unless the project structure is intentionally changed.
- Store quiz content as objects in the `questions` array; keep each answer's `correct` value as its zero-based index in `answers`.
- Use the existing DOM IDs and small state/flow functions when updating the UI. Insert dynamic text with `textContent` or DOM nodes, rather than HTML-string interpolation.
- Keep styles in the existing `<style>` block. Reuse its CSS custom properties for colors and preserve its dark color-scheme and reduced-motion behavior.
- Preserve the existing accessibility patterns: semantic sections and labels, visible keyboard focus, live feedback, question/result focus on transitions, and hidden decorative SVGs.
- The question count is derived from `questions.length` in some places but is also written literally as `10` in the progress bar's `aria-valuemax`, question numbering, and result score denominator. Update these together if the number of questions changes.
