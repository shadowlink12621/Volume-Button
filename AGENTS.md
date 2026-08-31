# Agent Rules

* Never commit directly to `main`.
* Never force push.
* Never rewrite Git history.
* Never reset or revert another developer's changes.
* Never delete files unless the current task explicitly requires deletion.
* Never overwrite another developer's work.
* Never use destructive Git commands without explicit approval.
* Never commit secrets, API keys, passwords, signing keys, keystores, or local machine configuration.
* Never modify unrelated files simply to make a task easier.
* Inspect existing code before changing it.
* Keep changes focused.
* Run appropriate tests/build checks before considering a feature complete.
* If merge conflicts occur, stop and report the conflict instead of blindly resolving it.
* The developer is responsible for deciding when commits and pushes happen.

### Feature Isolation
* Work only on your task-specific branch. Feature branches are not permanently assigned to specific developers. Both developers can work on any feature depending on the current task.
* ONE FEATURE / TASK = ONE WORK BRANCH.
* Do not modify unrelated feature areas.
* Do not combine two independent features into one branch.
* If a feature requires another feature, explicitly document the dependency.
* Do not cherry-pick another developer's commits unless explicitly instructed.
* Before modifying shared architecture, inspect current work and communicate the impact.

### Changelog
* Keep `CHANGELOG.md` updated whenever a meaningful feature/fix is merged into `dev`.
* Record meaningful changes regardless of which developer made them. The changelog should describe actual project changes, not permanent developer ownership.
* Record the following details for each entry:
  - Date
  - Branch
  - Developer
  - Change
  - Testing status
* Do not fabricate changelog entries.
* Record what actually changed.
* Record testing results when available.

### Git
* Never force push shared branches.
* Never rewrite shared history.
* Never reset another developer's work.
* Never delete another developer's branch.
* No direct pushes to `main`.
* Feature branches require Pull Requests.
* At least one developer should review the other developer's feature before merging into `dev`.
* `dev` must be tested before merging into `main`.
* Never automatically merge pull requests.
* Never blindly resolve merge conflicts.
* Keep feature branches focused on one feature.

### Antigravity
Antigravity may modify any project area required by the current task. However, before making changes:
1. Inspect the current branch.
2. Inspect Git status.
3. Identify existing uncommitted changes.
4. Understand the requested task.
5. Avoid unrelated modifications.
6. Never destroy another developer's work.
7. Never force-push.
8. Never rewrite shared history.
9. Do not automatically merge branches.
