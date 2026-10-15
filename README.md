# Orbit - Space Quiz

Orbit is an untimed, ten-question space exploration quiz. Choose an answer,
learn a fact after each question, and see your score and missed-answer review
at the end. Select **Explore again** to start a new attempt.

The app supports keyboard navigation, light and dark device themes, and
reduced-motion preferences. It is a dependency-free page with HTML, CSS, and
JavaScript in `index.html`.

## Run locally

Clone this repository and open `index.html` directly in a web browser.
No installation, build step, or local server is needed.

To check the quiz manually, try correct and incorrect answers, advance to the
results, review missed answers, and restart. There is no automated test runner
or linter configured.

## GitHub Pages

The published site is available at:
https://whdrbwkd-create.github.io/space-quiz/

The workflow in `.github/workflows/pages.yml` prepares and uploads the static
page for pull requests targeting `main`. Pushes to `main` also deploy it to
GitHub Pages. The workflow can be run manually from the Actions tab.

Only `index.html` is published; repository documentation and configuration are
not included in the site artifact. In repository **Settings > Pages**, the
deployment source must be **GitHub Actions**.
