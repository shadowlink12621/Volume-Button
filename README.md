# Custom Volume Controller

## Project Purpose
We are building a collaborative Android-first custom volume-control application. The goal is to create a highly customizable alternative volume-control experience that appears when physical volume buttons are pressed, inspired by unusual and custom interfaces.

## Technology Stack
- **Platform Strategy:** Android-first (iOS to be considered later as a separate native target)
- **Language:** Kotlin
- **UI Framework:** Jetpack Compose
- **Android APIs:** Android SDK / AudioManager
- **Architecture:** MVVM (UI -> ViewModel -> VolumeController abstraction -> AudioManager implementation)

## Repository Workflow
This repository follows a strict branch-based collaboration workflow.

Two developers will work independently on separate feature branches without mixing unrelated changes. For example:
- Developer A: `feature/android-volume`
- Developer B: `feature/volume-overlay`

When a feature is complete, it will be merged into `dev` via a Pull Request. After `dev` has been tested and is stable, it will be merged into `main`.

### Branches
```text
main
└── dev
    ├── feature/android-volume
    ├── feature/volume-overlay
    ├── feature/settings
    ├── feature/android-polish
    └── feature/ios
```

### Starting Work
A developer should do:
```bash
git checkout dev
git pull origin dev
git checkout -b feature/my-feature
```

### Before Finishing
```bash
git status
git add .
git commit -m "feat: description"
git push -u origin feature/my-feature
```
Then create a Pull Request into `dev`.

### Important
* Never directly push feature work to `main`.
* Never force-push.
* Never rewrite shared history.

### Commit Convention
Use conventional commit-style messages:
- `feat`: add custom volume overlay
- `fix`: correct volume state detection
- `ui`: redesign volume HUD
- `refactor`: extract volume controller
- `test`: add volume controller tests
- `docs`: update setup instructions
- `chore`: update dependencies

Keep commits small and logically focused.

### Running the Android Application
*(Instructions to be added once the Android project is initialized)*

## Safety Rules
Please refer to `AGENTS.md` for AI collaboration rules and strict guidelines on Git safety, file modification, and repository management.
