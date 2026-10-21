# Project Guidelines

## Project Shape
- This is Quickfire, a single-page quiz implemented in `index.html` with plain HTML, CSS, and JavaScript.
- Keep routine UI and quiz changes in `index.html`; do not add a framework, package manager, build step, or runtime dependency unless the project scope explicitly changes.
- The page should remain usable when opened directly from disk. Treat external font imports as optional and preserve fallback fonts.

## Quiz Behavior
- Keep quiz content in the `questions` array and render choices from that data rather than duplicating question markup.
- Preserve one answer per question, immediate correctness feedback, score/progress updates, a final results view, and a replay that resets all state.
- Keep user-facing content safe to insert into the page; use text APIs for dynamic question and answer strings.

## Accessibility and Responsive UI
- Use semantic elements and native buttons; maintain visible keyboard focus and move focus to a meaningful control when the question changes.
- Keep the progressbar's accessible value synchronized with its visual fill and the current question.
- Respect reduced-motion preferences and verify the layout at desktop and narrow mobile widths without horizontal overflow.

## Validation
- There is no install, build, or test command configured. For quiz changes, open `index.html` in a browser and smoke-test initial state, correct and incorrect answers, progression through all questions, final score, replay reset, and mobile layout.
