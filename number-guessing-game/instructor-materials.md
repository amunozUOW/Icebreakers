# Number Guessing Game — Instructor Materials

## Overview

| | |
|---|---|
| **Activity type** | Icebreaker / decision-making exercise |
| **Duration** | 10–15 minutes (including discussion) |
| **Group size** | Any (individual, pairs, or whole-class) |
| **Delivery mode** | Face-to-face, online, or hybrid |
| **Technical requirements** | Any device with a web browser |
| **Preparation time** | None — the game generates a random number each time |

The Number Guessing Game is a decision-focused icebreaker designed for use in the first tutorial or workshop of a management course. Students take on the role of a new manager who must estimate product demand with no prior data. They guess a number between 1 and 200, receive immediate feedback (higher/lower), and iteratively refine their estimate.

The activity introduces students to the iterative nature of decision-making and establishes the expectation that workshops are active, participation-driven learning environments.

---

## Learning Objectives

By completing this activity, students will:

1. **Explore the decision-making process** — identifying decisions, gathering information, evaluating alternatives, acting, and reviewing outcomes.
2. **Experience iterative convergence** — narrowing a range of options through sequential feedback and adjustment.
3. **Interpret graphical feedback** — reading a chart that maps their guesses over time and observing convergence towards the target.
4. **Reflect on cognitive patterns** — examining their own assumptions, risk tolerance, and responses to feedback.

---

## Connection to Decision-Making Theory

The activity is explicitly tied to a structured decision-making framework:

| Step | In the Game |
|------|-------------|
| **Identify the decision** | How many units should we stock? |
| **Gather information** | Read the feedback — higher or lower, and by how much. |
| **Identify alternatives** | The narrowing range shows what options remain. |
| **Weigh evidence and choose** | Use feedback to select the next guess. |
| **Act** | Submit the guess. |
| **Review the decision** | Observe the result and prepare the next iteration. |

This maps onto a process-oriented view of the activity:
- **Input:** Feedback from previous guesses (information)
- **Transforming resource:** The student's cognitive effort and decision strategy
- **Transformation process:** Interpreting feedback and refining the estimate
- **Output:** The next guess
- **Performance measure:** Number of guesses to reach the correct answer

---

## Setup Instructions

### Option A: Standalone HTML File (Browser)

1. Open `index.html` in any web browser.
2. The game is ready immediately — no configuration needed.
3. Share your screen or distribute the file to students.

### Option B: Embedding in a Learning Management System

The `moodle-embed.html` file is designed to be pasted into an LMS page resource. However, **most LMS platforms restrict or strip JavaScript** from their built-in content editors. The approach you use will depend on your platform.

#### Moodle

Moodle's editors (Atto, TinyMCE) strip `<script>` tags by default. Options:

1. **Plain Text Area editor** (most practical): Go to *User menu > Preferences > Editor preferences* and switch to "Plain text area." Then create a Page resource and paste the contents of `moodle-embed.html`. **Important:** If anyone later opens the page with the default WYSIWYG editor and saves, all JavaScript will be permanently removed.
2. **Trusted content** (requires admin): Your Moodle administrator can enable "Trusted Content" in *Site administration > Security > Site policies* and assign the `moodle/site:trustcontent` capability to the instructor role.
3. **Upload as a file** (most reliable): Upload `index.html` to the course files in Moodle, then link to it or embed it in a Page resource using an iframe:
   ```html
   <iframe src="YOUR_FILE_URL_HERE" width="100%" height="700" frameborder="0"></iframe>
   ```

#### Canvas

Canvas strips all `<script>` tags and inline event handlers. Direct embedding is not possible.

1. **Upload + iframe** (recommended): Upload `index.html` to *Course Files*. Get the file URL, remove the query string, and ensure it ends with `/download`. Then embed in a Canvas page:
   ```html
   <iframe src="https://your-canvas-instance/.../index.html/download" width="100%" height="700" frameborder="0"></iframe>
   ```
2. **Host externally**: Host the file on GitHub Pages or another web server and embed via iframe.

#### Blackboard

- **Original Course View**: Instructors have "Add/Edit Trusted Content With Scripts" by default. Pasting the embed code directly into the HTML editor may work without modification.
- **Ultra Course View**: JavaScript is not supported in HTML blocks. Upload the file as an HTML object in Course Files, or use a SCORM package (see below).

#### D2L Brightspace

Brightspace strips scripts from its content editor.

1. **Upload as a Content Topic** (recommended): Upload `index.html` to *Managed Files*, then add it as a content topic. When students click it, the file loads with full JavaScript support.
2. **Widget with iframe rendering**: Create a widget in *Course Admin > Widgets*, check "Render in iFrame," and paste the code.

#### Universal Approach: SCORM Package

If none of the above options work at your institution, wrapping the HTML file as a SCORM 1.2 package is the most reliable cross-platform solution. SCORM packages are supported by virtually all LMS platforms and execute JavaScript without restriction. See the [SCORM packaging guide](https://scorm.com/scorm-explained/) for details.

#### Universal Approach: External Hosting + iframe

Host `index.html` on any HTTPS web server (GitHub Pages is free) and provide an iframe embed code. This works on all platforms that allow iframes.

---

## Running the Activity

### During Class (Suggested Flow)

| Time | Action |
|------|--------|
| 0:00 | Display the game or direct students to the LMS page. Read the scenario aloud or let students read it. |
| 0:02 | Ask: "What's your first guess and why?" Take a few responses before anyone submits. |
| 0:03 | Let students play individually or in small groups. Allow 5–7 minutes. |
| 0:08 | Ask: "How many guesses did it take? What was your strategy?" |
| 0:10 | Facilitate discussion using the prompts below. |
| 0:15 | Wrap up by connecting the activity to the course themes. |

### Facilitation Tips

- **Ask "why" before they guess.** Eliciting reasoning before submission is more valuable than the guess itself. Questions like "Why that number?" or "Why not 100?" surface student thinking.
- **Don't rush to the answer.** The learning is in the process, not the result. Let students experience uncertainty and iteration.
- **Use the chart.** After the game ends, the chart shows all guesses plotted against the actual demand. Walk through it with students — it's a visual story of convergence.
- **Highlight the range narrowing.** The live range indicator (e.g., "Range: 45–120") makes the process of elimination visible and concrete.
- **Vary the group format.** Individual play encourages personal reflection. Small groups encourage discussion. Whole-class play (taking guesses from the audience) creates energy.

---

## Discussion Prompts

Use these prompts after the activity to guide reflection. You don't need to use all of them — choose based on what resonates with the group.

### Initial Strategy and Assumptions
- "What was your first guess? Why did you start there?"
- "Did you have a strategy before you began, or did one emerge as you played?"
- "Did anyone start at 100? Why is that a common choice?"

### Feedback Interpretation
- "How did you interpret the feedback? Did you find it easy or difficult to adjust?"
- "Did anyone ignore the feedback at any point and go with their gut?"

### Optimisation and Convergence
- "Did your strategy change as the game went on? How?"
- "How did you decide how big a jump to make between guesses?"
- "If you played again, would you do anything differently?"

### Risk Appetite
- "Were you a big-jump guesser or a small-step guesser? Why?"
- "What are the trade-offs between large leaps and small increments?"
- "How does risk appetite relate to real management decisions — like how much inventory to order or how many staff to roster?"

### Frustration and Persistence
- "Did anyone feel frustrated at any point? What caused it?"
- "How did you manage that frustration and keep going?"

### Connecting to Your Discipline
- "Can you see how the skills you used here might apply in your field of study?"
- "What was the 'input' in this activity? What was the 'output'? What was the process in between?"
- "How is this different from making a single, one-shot decision versus an iterative one?"
- "In real management, you rarely have perfect information. How does this game simulate that reality?"

---

## Adapting for Different Contexts

| Context | Adaptation |
|---------|------------|
| **First class of the course** | Use as the opening activity to set expectations for active participation. Emphasise that workshops will always involve making decisions, not just listening. |
| **Large lectures** | Display on the main screen. Take guesses from the audience and submit them collectively. Discuss strategy between guesses. |
| **Online/synchronous** | Students play individually, then share scores and strategies in chat or breakout rooms. |
| **Online/asynchronous** | Embed in the LMS. Ask students to play and then post a short reflection (e.g., "Describe your strategy in 2–3 sentences") in a discussion forum. |
| **Revision or later sessions** | Revisit the game and ask students to articulate their strategy using formal decision-making terminology they've learned since the first class. |

---

## How the Game Works (Technical Reference)

- **Target number:** Randomly generated between 1 and 200 on each play.
- **Feedback tiers:**
  - **> 50 away:** "Way too high/low! Go much higher/lower."
  - **21–50 away:** "Too high/low. Go higher/lower."
  - **6–20 away:** "Getting warm! Go a little higher/lower."
  - **1–5 away:** "Very close! Just a touch higher/lower."
- **Range indicator:** Updates after each guess to show the narrowed range.
- **Activity log:** Records all guesses with colour-coded entries (collapsible panel).
- **Chart:** Plots guesses over time. After the game ends, a dashed green line shows the actual demand.
- **Play Again:** Resets everything with a new random number.
- **Dependencies:** Chart.js loaded from CDN (requires internet access).

---

## Troubleshooting

| Issue | Solution |
|-------|----------|
| Chart doesn't render | The game requires Chart.js from a CDN. Ensure the device has internet access. If your LMS blocks external scripts, check with IT. |
| Game doesn't load in LMS | Most LMS editors strip JavaScript. See the **Embedding in a Learning Management System** section above for platform-specific instructions. |
| Students finish too quickly | This is fine — the discussion is the main learning activity. Ask fast finishers to play again and try to beat their score, or to coach a neighbour. |
| Students can't see the chart | On very small screens the chart may be compressed. The game works without it — the activity log provides the same information textually. |
