# Say No 2 Cyber Bullying

> An educational React web app that raises awareness about cyberbullying — what it is, why it happens, who it affects, and how to respond — paired with interactive review games. Built to inform and equip teens with practical steps for staying safe online.

---

## About

**Say No 2 Cyber Bullying** is a single-page React application designed as an awareness resource. It walks a visitor through the topic in plain language and then reinforces it with an interactive quiz, so the experience is part lesson, part activity.

The app is organized around two views, toggled from the header:

- **Home** — the educational content.
- **Games** — a link out to a Blooket review set so visitors can test what they learned.

---

## Features

- **Topic walkthrough** — a series of illustrated cards, each answering one question:
  - What is cyberbullying?
  - Why do people cyberbully?
  - Who is affected?
  - What are the mental, physical, and social effects?
  - How can you protect yourself? (the **SMART** framework)
  - What should you do if you're being bullied?
- **Statistics section** — key figures conveying the scale and impact of cyberbullying.
- **Interactive games** — a linked Blooket quiz set for reviewing the material.
- **Two-view navigation** — a header toggle switches between the Home content and the Games view, handled with React state.

---

## How it's built

The app keeps content and presentation separate, which makes it easy to update:

- **`src/Public/Answers.jsx`** holds the educational copy as exported strings — the "content layer."
- **`src/Components/Home/TextBox.jsx`** is a single reusable card component (title + image + description). The `Info` component feeds each piece of content into a `TextBox`, so every section shares one consistent layout.
- **`src/App.jsx`** holds the top-level state that switches between the Home and Games views.

```
src/
├── App.jsx                     # Top-level view switching
├── Components/
│   ├── Header/                 # Logo, title, Home/Games toggle
│   ├── Home/                   # Image, Info, TextBox, Statistics, ProgressBar
│   └── Games/                  # Blooket quiz links
├── Public/
│   └── Answers.jsx             # Educational content (text)
└── Assests/                    # Images and logo
```

---

## Getting started

This is a [Create React App](https://create-react-app.dev/) project.

```bash
npm install      # install dependencies
npm start        # run locally at http://localhost:3000
npm run build    # produce an optimized production build
```

### Deployment

The repo includes an `amplify.yml`, so it's configured to deploy on **AWS Amplify** (it installs, builds, and serves the `build/` folder). It can also be deployed to any static host (Netlify, Vercel, GitHub Pages) using the output of `npm run build`.

---

## Tech stack

- **React 18**
- **Create React App** (react-scripts)
- **AWS Amplify** (deployment configuration)

---

## A note on the topic

This project deals with cyberbullying and its effects, including impacts on mental health. If you or someone you know is struggling, reach out for support — in the US, you can call or text **988** to reach the Suicide & Crisis Lifeline. Adding an in-app "Get Help" section with resources like this is a recommended next step for the project.
