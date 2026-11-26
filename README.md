# Quiz CLI

An interactive command-line quiz game for learning JavaScript. Choose a programming topic, answer questions, review your results, and optionally play again.

> **Repository status:** The current repository tree contains `index.js`, `package.json`, and `.DS_Store`. The application entry point imports `src/input.js`, `src/quiz.js`, and `src/colors.js`, and loads `data/questions.json`; those files are not currently present. As a result, the documented start command will not run successfully until those application files are added.

## Requirements

- Node.js 18 or newer
- npm (included with Node.js)

The project uses native Node.js modules and ES modules; `package.json` does not declare third-party dependencies.

## Getting started

From the project directory:

```sh
npm start
```

The start script runs `node index.js`. Once the missing modules and question data are available, the application is designed to let you select a category and question count, take the quiz, see results, and choose whether to play again.

## Question data and application modules

The entry point expects a `data/questions.json` file containing category data. It reads `data.categories`, uses each category's `name` and `questions`, and presents the questions to the `Quiz` class. The precise question object format is determined by the missing quiz implementation and cannot be specified from the files currently in the repository.

The entry point also expects these modules:

- `src/input.js` — interactive terminal input helpers (`createInterface`, `select`, `confirm`, and `pressEnter`)
- `src/quiz.js` — the `Quiz` class used to ask questions and display results
- `src/colors.js` — terminal formatting functions

## Tests

Run the configured test command with:

```sh
npm test
```

This invokes Node's built-in test runner (`node --test`). No test files are present in the current repository tree.

## Project structure

```text
.
├── index.js       # CLI entry point and quiz flow
├── package.json   # Project metadata and npm scripts
└── .DS_Store      # macOS metadata file
```

The entry point expects `src/` and `data/` directories, which are not included in the current repository tree.

## Project metadata

- **Version:** 1.0.0
- **License declared in package metadata:** MIT
- **Module format:** ECMAScript modules
- **Runtime requirement:** Node.js >=18
