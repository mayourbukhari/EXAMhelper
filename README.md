# TCS NQT Question Bank

A responsive, single-file practice website for TCS NQT preparation.

It includes:
- Topic-wise multiple choice questions
- Instant answer feedback (correct/wrong/revealed)
- Search and section filters
- Pagination
- Topic intro blocks with key concepts and formulae
- Progress tracking (answered, revealed, accuracy, progress %)

## Project Structure

- `tcs_nqt_question_bank.html`: Complete app (HTML, CSS, and JavaScript in one file)

## How to Run

No build tools are required.

1. Open `tcs_nqt_question_bank.html` in any modern browser.
2. Start practicing by selecting answers, filtering topics, and viewing explanations.

## How to Customize

### 1. Add or Edit Questions

Questions are defined in the `allQs` array inside `tcs_nqt_question_bank.html`.

Each question object uses this structure:

```js
{
  n: 1,
  sec: "Quantitative Aptitude",
  q: "Question text",
  opts: ["Option A", "Option B", "Option C", "Option D"],
  ans: 1,
  explain: "Short explanation",
  example: "Worked example or practical note"
}
```

Notes:
- `n` should be unique.
- `ans` is zero-based (`0` for first option, `1` for second, etc.).

### 2. Add Concepts and Formulae for a Topic

Topic summaries are stored in `topicMeta`.

```js
"Topic Name": {
  concepts: ["Concept 1", "Concept 2"],
  formulae: ["Formula 1", "Formula 2"]
}
```

If a topic is missing in `topicMeta`, a default intro is shown automatically.

### 3. Change Questions Per Page

Update this constant:

```js
const perPage = 8;
```

## Features Overview

- Responsive UI for desktop and mobile
- Sticky control bar for quick filtering
- Visual stats cards for total/shown/correct/wrong
- Progress bar with accuracy and completion details
- Explanation toggle per question

## Future Improvements (Optional)

- Add dark mode toggle
- Save progress in local storage
- Add timer and mock test mode
- Export/import question bank as JSON

## License

Personal/educational use.
