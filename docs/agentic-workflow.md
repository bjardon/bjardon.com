# Agentic Workflow

These rules apply to agent work in this repo, including Codex and Cursor.

## Interactive Local Work

When working in an interactive agent session, assume Bruno already has the project running locally.

- Do not launch a dev server.
- Do not stop or restart an existing dev server unless Bruno explicitly asks.
- If browser-use, computer-use, screenshots, or localhost verification would help, ask Bruno for the localhost URL first.
- If the URL is not provided, use non-browser verification such as tests, type checks, builds, linting, or source inspection.

In an unattended agent run, starting the minimum required local server for verification is acceptable when needed, unless other repo guidance says otherwise.

## Commit Messages

When Bruno asks you to commit, use Conventional Commits. Do not ask Bruno to look up the Notion page; apply this local guidance directly.

Format:

```text
<type>[optional scope][!]: <description>

[optional body]

[optional footer(s)]
```

Allowed types:

- `feat`: A new user-facing feature or capability.
- `fix`: A bug fix.
- `docs`: Documentation-only changes.
- `style`: Formatting or presentation changes that do not affect behavior.
- `refactor`: Code restructuring that does not add a feature or fix a bug.
- `perf`: A performance improvement.
- `test`: Adding or updating tests.
- `build`: Build system, dependency, or packaging changes.
- `ci`: Continuous integration changes.
- `chore`: Maintenance work that does not fit the other types.
- `revert`: Reverting a previous commit.

Message rules:

- Use a short, imperative, lowercase description after the colon.
- Keep the subject line focused on the user-visible or repo-visible change.
- Add a scope only when it clarifies the affected area, for example `docs(agentic): ...` or `feat(projects): ...`.
- Use `!` after the type or scope for breaking changes, and explain the breaking change in the body or footer.
- Include a body when the reason, tradeoff, or context would not be obvious from the diff.
- Include footers for issue links or breaking changes when relevant, for example `Refs: LIN-123` or `BREAKING CHANGE: ...`.

Examples:

```text
docs(agentic): add interactive workflow rules
feat(projects): add selected work detail page
fix(resume): correct role date range
chore(deps): update astro dependencies
```
