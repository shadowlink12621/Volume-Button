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
This repository follows a strict GitHub Flow-inspired branch-based collaboration workflow, preserving our `main → dev → feature/*` architecture.

**Important Principle: ONE FEATURE / TASK = ONE WORK BRANCH**
Feature branches are NOT permanently assigned to specific developers. Both developers are allowed to work on any feature depending on their current task. For example, either developer may work on `feature/android-volume` or `feature/volume-overlay`.

**Simultaneous Work:**
If both developers need to work on the same broad feature simultaneously, create more specific task branches instead of editing the exact same branch (e.g., `feature/android-volume-detection` and `feature/android-volume-service`). This minimizes conflicts. Coordinate first if both developers intentionally need to modify the same branch.

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

### Daily Workflow
Before starting work, sync your local integration branch:
```bash
git checkout dev
git pull origin dev
```
**Important Clarification:** Do NOT routinely run `git pull origin main` while working on feature branches. Our project uses `dev` as the integration branch, so the normal synchronization target is `origin dev`. This prevents unfinished or unrelated work from being mixed into active development.

Then create or switch to your task-specific branch:
```bash
git checkout -b feature/description-of-task
```

### Development
Work only on your task-specific branch. Commit focused changes:
```bash
git add .
git commit -m "feat: description of change"
```

### Push
Push your feature branch to the remote repository:
```bash
git push -u origin feature/my-feature
```

### Pull Request & Review Rules
Create a Pull Request to merge your feature into `dev`:
```text
feature/my-feature
        ↓
       dev
```
- **No direct pushes to `main`.**
- Feature branches require Pull Requests.
- At least one developer should review the other developer's feature before merging into `dev`.
- Keep feature branches focused on one feature.
- Never force-push shared branches.
- Never rewrite shared history.
- Never blindly resolve merge conflicts.

### Integration
After review and approval, merge the feature into `dev`. The `dev` branch is where both developers' completed features are integrated and tested.

Only after `dev` is tested and completely stable should it be merged into `main`:
```text
dev
 ↓
main
```

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
