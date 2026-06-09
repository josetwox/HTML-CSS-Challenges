# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

A collection of standalone HTML/CSS challenges. Each challenge lives in its own directory with an `index.html`, `style.css`, and a `README.md` describing the tasks to complete.

## Running the Project

No build step or package manager. Open `index.html` directly in a browser:

```bash
# Linux
xdg-open zoo-css-challenge/index.html

# macOS
open zoo-css-challenge/index.html
```

## Repository Structure

Each challenge directory is self-contained:
```
<challenge-name>/
  README.md    # Task instructions for the challenge
  index.html   # HTML structure (may contain intentional mistakes to fix)
  style.css    # Linked stylesheet
```

## Current Challenge: `zoo-css-challenge`

The zoo site has a dark header (`#211a1d`), sections with `padding: 5%`, and a global purple heading color (`#6320ee`). Key CSS patterns already established:

- **Cards** (`.card`): `display: inline-block`, 30% width, `border-radius: 10px`
- **Badge** (`#badge`): `position: fixed`, bottom-right, circular via `border-radius: 50%`
- **Section backgrounds**: each `<section>` overrides the default `#f8f0fb` with its own background color
- **Images**: global `border: 5px solid #8075ff`; bears override this in `.image-container img`

The `README.md` inside each challenge directory is the source of truth for what needs to be fixed or added. Tasks are numbered and map to specific HTML sections/CSS selectors.

## Conventions

- CSS is organized in source order matching the HTML document flow, with `/* Section name */` comments separating major blocks.
- Accessibility: heading colors on dark backgrounds must pass WCAG AA contrast (use https://webaim.org/resources/contrastchecker/).
- New `<a>` elements acting as external links should include `target="_blank"`.
