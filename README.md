# The GreenZone Plugin Repository

This is the live custom Dalamud repository for The GreenZone, a private Free Company plugin
for The Studium in Final Fantasy XIV.

Use this repository URL in Dalamud's custom plugin repository settings:

```text
https://raw.githubusercontent.com/Ninethirty77/the-greenzone-repo/main/repo.json
```

## What This Repo Contains

- `repo.json`: Dalamud custom repository metadata and update notes
- `latest.zip`: the current plugin package
- `icon.jpg`: plugin icon
- `fc-week.json`: the shared weekly FC Credits base and target
- `HOW_TO_USE.md`: short member guide
- `CHANGELOG.md`: human-readable release notes

## Shared FC Week

`fc-week.json` controls the FC Credits progress ring for all users:

```json
{
  "week": "Week 1",
  "baseCompanyCredits": 573000000,
  "targetCompanyCredits": 7500000
}
```

The plugin reads this public GitHub raw file periodically and caches it locally. Editing this file
is enough to update the shared baseline and target for all users once their plugin refreshes it.

Do not overwrite `fc-week.json` during plugin releases unless the weekly base or target is being
intentionally changed.

## Phone Update Workflow

Use GitHub Actions on the GitHub website or mobile app:

1. Open this repository.
2. Go to Actions.
3. Choose `Update FC Week`.
4. Run the workflow.
5. Enter the week label, base Company Credits, and target Company Credits.

The workflow validates the values and commits only `fc-week.json`.
