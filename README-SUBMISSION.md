# FamilyFit TV — Fire OS Hackathon Starter

**Project idea:** a remote-first family fitness experience for the living room. Users can discover short routines, save favourites, play a preview, and track completed sessions.

This repository contains a React/Vite interface and a native Android WebView shell configured with a Leanback launcher entry point for Fire OS testing. It is a starter implementation; you must build and test it on Fire OS or the official Fire TV/Vega simulator before representing it as a working Fire TV app.

## Features in the source
- TV-first dark interface with high-contrast focus styling
- D-pad directional navigation and Enter selection
- Workout categories and search
- Workout details, sample video preview, session timer
- My List favourites and progress page
- Profile name and weekly goal
- Browser storage persistence
- Help overlay and Escape/Back navigation

## Prerequisites
- Node.js LTS and npm
- Android Studio with Android SDK Platform 35 and a compatible JDK (JDK 17 recommended)
- A Fire OS device or compatible emulator for runtime validation

## Build web assets (Windows PowerShell)
From the extracted project root:

```powershell
Set-ExecutionPolicy -Scope Process Bypass
.\build-fireos.ps1
```

This runs `npm install`, `npm run build`, and copies the `web/dist` output into `android/app/src/main/assets/www`.

## Build the Fire OS APK
1. Open Android Studio.
2. Choose **Open** and select the `android` folder in this repository.
3. Let Gradle sync finish; install any requested SDK Platform 35/build tools.
4. Select **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
5. The debug APK is normally created under `android/app/build/outputs/apk/debug/app-debug.apk`.
6. Install/run it on a Fire OS device or the compatible emulator and test every remote key before recording the demo.

If Gradle sync or build fails, resolve the specific SDK/JDK/Gradle error before submission. This ZIP has not been built or tested against your local Android Studio setup.

## Submission requirements checklist
- [ ] Run on Fire OS or the Fire TV/Vega simulator and record proof in the demo video.
- [ ] Replace the sample public test clips with original/licensed workout footage. Do not submit content you do not have rights to use.
- [ ] Test video playback and all D-pad/Back interactions on target runtime.
- [ ] Create a public GitHub repository containing all source, instructions, and this LICENSE file.
- [ ] Add a demo video under 3 minutes, hosted publicly on YouTube or Vimeo, in English.
- [ ] Complete the Devpost project description, track selection, demo/repository links, and product feedback.
- [ ] Only claim features that you personally verified in the final demo.

## Suggested Devpost description
**FamilyFit TV — Feel Good. Move Together.**

FamilyFit TV makes everyday movement feel approachable by bringing short, family-friendly workout sessions to the biggest screen in the home. A remote-first interface helps users browse routines by mood and activity, save favourites, launch video sessions, and celebrate completed workouts with simple progress tracking. The prototype prioritizes readable TV-scale layouts, directional navigation, and a low-friction path from discovery to movement.

**Current implementation:** React/Vite UI packaged into an Android WebView shell with a Leanback launcher entry point for Fire OS testing. Workout metadata and progress are demo data stored locally; the bundled public test video URLs are placeholders and must be replaced with licensed workout content before public release.

## Demo outline (under 3 minutes)
1. Launch FamilyFit TV on the Fire TV device/simulator.
2. Use the remote to move across the home screen and select a category.
3. Open a routine, save it to My List, then start a session.
4. Demonstrate player controls and finish a session.
5. Show the Progress screen and weekly goal settings.

## Important honesty note
This is source code and a packaging starter, not a guarantee of hackathon eligibility or a prebuilt, tested APK. The hackathon requires a demo-ready app that runs on Fire OS or Vega OS. Build, install, and verify on the target runtime before submission.
