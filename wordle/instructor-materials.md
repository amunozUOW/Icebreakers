# Wordle Vocabulary Game — Instructor Materials

## Overview

| | |
|---|---|
| **Activity type** | Icebreaker / vocabulary activation |
| **Duration** | 5–10 minutes |
| **Group size** | Any (individual, pairs, or whole-class) |
| **Delivery mode** | Face-to-face, online, or hybrid |
| **Technical requirements** | Any device with a web browser |
| **Preparation time** | Under 2 minutes |

The Wordle vocabulary game is a digital icebreaker that engages students with key terminology at the start of a tutorial or workshop. It replicates the mechanics of the popular Wordle word-guessing game, adapted for educational settings. Students guess an educator-selected target word in up to six attempts, receiving colour-coded feedback after each guess.

The activity is deliberately short and low-stakes, designed to activate prior knowledge, focus attention on the session's theme, and lower barriers to participation before moving into more substantive content.

---

## Learning Objectives

By completing this activity, students will:

1. **Recognise and recall** subject-specific terminology from lecture or pre-reading materials.
2. **Activate prior knowledge** by connecting the target word to concepts they have already encountered.
3. **Engage early** in the session through a quick, interactive task that sets an expectation of participation.

---

## Changing the Target Word

The game defaults to the word "INVENTORY." You can change the word at any time using the built-in educator setup — **no code editing is required.**

### How to Change the Word (Triple-Click Method)

1. Look for the small, grey **"v1.0"** text at the very bottom of the game area.
2. **Click it three times quickly** (within about half a second). A setup popup will appear.
3. Type your chosen word (3–14 letters, any subject area) into the text field.
4. Click **Set Word & Reset**. The game will immediately restart with your new word.

This works in both the standalone (`index.html`) and LMS-embedded (`moodle-embed.html`) versions.

> **Why triple-click?** The trigger is deliberately hidden so students don't accidentally discover it. The "v1.0" text looks like a version label and blends into the background.

### Alternative: Edit the Default Word in Code

If you prefer to set the word before deploying to your LMS, locate this line near the top of the `<script>` section:

```
var DEFAULT_WORD = 'INVENTORY';
```

Replace `INVENTORY` with your chosen word in uppercase, then save and upload.

---

## Setup Instructions

### Option A: Standalone HTML File (Browser)

1. Open `index.html` in any web browser.
2. Triple-click **"v1.0"** at the bottom to set your target word (see above).
3. Share your screen or distribute the file to students.

### Option B: Embedding in a Learning Management System

The `moodle-embed.html` file is designed to be pasted into an LMS page resource. However, **most LMS platforms restrict or strip JavaScript** from their built-in content editors. The approach you use will depend on your platform.

#### Moodle

Moodle's editors (Atto, TinyMCE) strip `<script>` tags by default. Options:

1. **Plain Text Area editor** (most practical): Go to *User menu > Preferences > Editor preferences* and switch to "Plain text area." Then create a Page resource and paste the contents of `moodle-embed.html`. **Important:** If anyone later opens the page with the default WYSIWYG editor and saves, all JavaScript will be permanently removed.
2. **Trusted content** (requires admin): Your Moodle administrator can enable "Trusted Content" in *Site administration > Security > Site policies* and assign the `moodle/site:trustcontent` capability to the instructor role.
3. **Upload as a file** (most reliable): Upload `index.html` to the course files in Moodle, then link to it or embed it in a Page resource using an iframe:
   ```html
   <iframe src="YOUR_FILE_URL_HERE" width="100%" height="800" frameborder="0"></iframe>
   ```

#### Canvas

Canvas strips all `<script>` tags and inline event handlers. Direct embedding is not possible.

1. **Upload + iframe** (recommended): Upload `index.html` to *Course Files*. Get the file URL, remove the query string, and ensure it ends with `/download`. Then embed in a Canvas page:
   ```html
   <iframe src="https://your-canvas-instance/.../index.html/download" width="100%" height="800" frameborder="0"></iframe>
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

## Choosing a Good Target Word

- Select a word directly related to the week's topic (e.g., "STRATEGY" for a strategy session, "DEMAND" for supply chain content, "CULTURE" for organisational behaviour).
- Words between 5 and 9 letters work best — long enough to be challenging, short enough to be solvable.
- The word must be in the game's built-in dictionary to be guessable by students. Business, management, and common English words are included (2,000+ words). If you set a highly specialised term via the educator setup, it will be automatically added to the dictionary for that session.
- Avoid obscure abbreviations or proper nouns that students may not recognise as valid guesses.

---

## Running the Activity

### Before Class
- Decide on the target word for the session.
- Set the word using the triple-click method or by editing the default (see above).
- Test the game yourself to confirm it works.

### During Class (Suggested Flow)

| Time | Action |
|------|--------|
| 0:00 | Display the game on screen or direct students to the LMS page. |
| 0:01 | Briefly explain: "We're starting with a quick word game. You have six tries to guess today's key term. The colours tell you which letters are correct." |
| 0:02 | Let students play. Allow 3–5 minutes. Circulate or observe. |
| 0:05 | After most students have finished (or after six attempts), reveal the word if needed. |
| 0:06 | Transition to discussion using the prompts below. |

### Facilitation Tips

- **Let students struggle a little.** The point is engagement, not instant success. Six attempts is usually enough.
- **Encourage collaboration.** In face-to-face settings, pairs or small groups can work together on a shared screen.
- **Don't over-explain the rules.** Most students are familiar with Wordle. The on-screen instructions are sufficient.
- **Use the word reveal as a teaching moment.** Whether students guess correctly or not, the word itself is the bridge into the session.

---

## Discussion Prompts

After the activity, use one or more of these prompts to transition into the session content:

### Activating Prior Knowledge
- "What do you already know about [word]?"
- "Where have you encountered this term before — in lectures, readings, or real life?"
- "Can you give a one-sentence definition of [word]?"

### Connecting to the Session
- "Why do you think this is today's key term?"
- "What industries or companies come to mind when you hear [word]?"
- "How might [word] relate to what we discussed last week?"

### Exploring Depth
- "What's the difference between [word] and [related concept]?"
- "Can you think of a real-world example where [word] was applied well — or poorly?"
- "If you had to explain [word] to someone outside this course, what would you say?"

---

## Adapting for Different Contexts

| Context | Adaptation |
|---------|------------|
| **Large lectures** | Display on the main screen. Run as a collective exercise — take guesses from the audience. |
| **Online/hybrid** | Embed in your LMS. Students play individually before the synchronous session. |
| **Revision sessions** | Use terms from across the entire subject to test retention. |
| **Different disciplines** | The word list includes common English words and can accept any custom word via the educator setup. Use for any subject that involves terminology. |
| **Repeated use** | Change the word each week. Students come to expect and enjoy the ritual. |

---

## How the Game Works (Technical Reference)

- **Feedback colours:**
  - **Green** — correct letter in the correct position.
  - **Yellow** — correct letter in the wrong position.
  - **Grey** — letter not in the word.
- **Validation:** Each guess must be a real word of the correct length (validated against an internal dictionary of 2,000+ words).
- **Attempts:** Students have 6 guesses. If they don't get it, the answer is revealed.
- **Keyboard:** Works with both the on-screen keyboard and physical keyboard.
- **Reset:** The "Reset" button restarts the game with the same word.
- **Word length hint:** The game displays "Guess the X-letter word" so students know the target length.
- **Dependencies:** None — fully self-contained, no internet required.

---

## Troubleshooting

| Issue | Solution |
|-------|----------|
| Game doesn't load in LMS | Most LMS editors strip JavaScript. See the **Embedding in a Learning Management System** section above for platform-specific instructions. |
| Students see "Not a valid word!" | Their guess isn't in the dictionary. They need to try a different word of the same length. |
| Word is too easy/hard | Adjust word length and obscurity. 7–9 letter discipline-specific terms tend to hit the sweet spot. |
| Students can see the answer in the code | In the standalone version, the word is only set in memory after triple-clicking. In the LMS version, a determined student could inspect the source — this is acceptable for a low-stakes icebreaker. |
| Triple-click setup doesn't open | Make sure you're clicking the small grey "v1.0" text at the very bottom of the game area. Three clicks within about half a second. It won't work if you click elsewhere. |
