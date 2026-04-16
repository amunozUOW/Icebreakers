# Icebreaker Activities for Management Education

Interactive digital icebreaker activities designed for use in management education tutorials and workshops. Each activity runs in any web browser and can be embedded directly into Moodle or other learning management systems.

## About This Project

This repository accompanies a manuscript submitted to *Management Teaching Review* (Sage Journals) on leveraging generative AI capabilities and vibe coding to develop pedagogical tools for higher education. The two activities included here were developed using iterative vibe-coding workflows and are designed to be accessible to educators with no programming background.

The activities serve as short, structured exercises that focus student attention, activate prior knowledge, and establish expectations for active participation at the start of a session.

## The Activities

### 1. Wordle Vocabulary Game

A Wordle-style word-guessing game adapted for educational settings. Students guess an educator-selected target word (3–14 letters) in up to six attempts, receiving colour-coded feedback after each guess.

**Use it to:** Activate prior knowledge, introduce key terminology, and create a low-stakes warm-up that transitions into the session's content.

**Key features:**
- Educator-friendly word setup — triple-click a hidden link to change the word mid-session, no code editing required
- Supports words of any length (3–14 letters)
- Built-in dictionary of 2,000+ business, management, and common English words
- Physical keyboard and on-screen keyboard support
- Works on desktop, tablet, and mobile

### 2. Number Guessing Game

A decision-making icebreaker framed as a management scenario. Students take on the role of a new manager estimating product demand with no prior data. They guess a number between 1 and 200, receive tiered feedback, and iteratively converge on the answer.

**Use it to:** Introduce iterative decision-making, demonstrate feedback-driven convergence, and set the expectation that workshops involve active participation.

**Key features:**
- Business scenario framing adaptable to any management discipline
- Tiered feedback system (way too high → too high → getting warm → very close)
- Live range indicator showing the narrowing solution space
- Activity log recording all guesses with colour-coded entries
- Interactive Chart.js chart plotting guesses over time with a target line revealed at the end
- No setup required — generates a random target each time

## Quick Start

### Option 1: Open in a Browser

1. Download or clone this repository.
2. Open `wordle/index.html` or `number-guessing-game/index.html` in any web browser.
3. For the Wordle game, triple-click the "v1.0" text at the bottom to set your target word.

### Option 2: Embed in a Learning Management System

Each `moodle-embed.html` file is designed for LMS embedding. However, **most LMS platforms strip JavaScript from their content editors by default.** The most reliable cross-platform approaches are:

1. **Upload the standalone `index.html` file** to your LMS file storage and embed it via iframe.
2. **Host on GitHub Pages** (free) and embed via iframe in any LMS.
3. **Wrap as a SCORM package** for universal LMS compatibility.

Platform-specific instructions (Moodle, Canvas, Blackboard, Brightspace) are included in each activity's instructor materials.

Each activity folder contains detailed instructor materials (`instructor-materials.md`) with setup instructions, LMS embedding guidance, facilitation tips, discussion prompts, and troubleshooting.

## Repository Structure

```
├── README.md
├── LICENSE
├── wordle/
│   ├── index.html          # Standalone game (open in browser)
│   ├── moodle-embed.html   # LMS-embeddable version
│   └── instructor-materials.md      # Instructor materials
└── number-guessing-game/
    ├── index.html           # Standalone game (open in browser)
    ├── moodle-embed.html    # LMS-embeddable version
    └── instructor-materials.md       # Instructor materials
```

## Educator Setup Reference

| Activity | Setup needed? | How to configure |
|----------|--------------|-----------------|
| **Wordle** | Yes — choose a target word | Triple-click "v1.0" at the bottom of the game, or edit `DEFAULT_WORD` in the code |
| **Number Guessing Game** | No | Random target generated automatically |

## Technical Notes

- Both activities are self-contained HTML files with no server-side dependencies.
- The Number Guessing Game uses [Chart.js](https://www.chartjs.org/) via CDN for the guess-tracking chart (requires internet access).
- The Wordle game has no external dependencies.
- All code runs client-side in the browser. No student data is collected or transmitted.

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.

## Citation

If you use these activities in your teaching or research, please acknowledge Dr. Albert Munoz (amunoz@uow.edu.au).

## Contributing

Suggestions, bug reports, and contributions are welcome. Please open an issue or submit a pull request.
