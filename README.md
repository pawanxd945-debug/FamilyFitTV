# FamilyFit TV — Fire TV-oriented fitness demo

FamilyFit TV is a remote-friendly family fitness experience designed for a TV-sized screen. It includes four short guided workout plans, favorites, an elapsed session timer, completion tracking, and a progress screen. It is a front-end demo; workout guidance is illustrative and does not provide medical advice.

## Important hackathon eligibility note

This repository is a web-technology prototype designed with TV navigation in mind. **It has not been verified on Fire OS or Vega OS by this project generator.** The Amazon Developer Hackathon Fire TV track requires the app to run on Fire OS or Vega OS and the public demo video to show it running on a real Fire TV device or the Fire TV/Vega simulator. Do not claim device testing unless you have performed it. A browser screenshot or desktop-only demo does not satisfy that requirement.

## Run locally

Requirements: Node.js 18+ and npm.

```bash
npm install
npm run dev
```

Open the local URL printed by Vite. Use arrow keys to move the TV focus indicator, Enter to activate the focused control, and Escape/Backspace to return to Home from a workout detail.

Production build:

```bash
npm run build
npm run preview
```

## Features

- TV-friendly 16:9 layout and large focusable controls
- Home, Workouts, Favorites, Progress screens
- Family Warm-up, Living Room Cardio, Calm & Stretch, Family Dance Party
- Session timer, reset, and mark-complete flow
- Responsive layout for local development

## Submission checklist

- [ ] Package or load the app using a Fire OS/Vega OS-supported method and test it on the target device or official simulator.
- [ ] Verify D-pad/remote navigation and app launch on that target.
- [ ] Record a public English demo video under 3 minutes showing the app running on the target device/simulator.
- [ ] Add the repository URL, video URL, feature description, and required product feedback to the Devpost submission form.
- [ ] Ensure the repository is public with a visible open-source license, or private and shared with the specified reviewers.

## Product feedback draft (edit to reflect your actual experience)

This prototype uses React and Vite for a TV-first fitness UI. The focusable controls and keyboard-based remote simulation were useful for rapidly iterating on navigation. Before submission, test with the actual Fire TV/Vega environment and report the real setup experience, errors, performance, and missing device-specific capabilities. Do not submit this draft unchanged unless it accurately describes your experience.
