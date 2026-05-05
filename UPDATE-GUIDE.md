# Tomorrow's easy update guide

This version uses a single source of truth.

## Only edit this one block

Open `index.html` and find:

```js
const RANKINGS_DATA = [
  { rank: 1, team: 'Carleton College', region: 'NC1', pr: '2607.1' },
  ...
];
```

That is the only section you need to update when rankings change.

## What happens automatically

When you update `RANKINGS_DATA`, the page will automatically regenerate:
- the posted rankings list
- the team dropdown
- the “too high” checkboxes
- the “too low” checkboxes

## How to update tomorrow

1. Open `index.html` in VS Code.
2. Find `const RANKINGS_DATA = [` near the top of the script.
3. Replace the objects in that array with the new rankings.
4. Save the file.
5. Commit and push to GitHub.
6. Wait a few minutes for GitHub Pages to refresh.

## Format to follow

Each team must stay in this format:

```js
{ rank: 1, team: 'Team Name', region: 'RegionCode', pr: '1234.5' }
```

## Example

```js
{ rank: 1, team: 'Example University', region: 'NW1', pr: '2501.2' }
```

## Important notes

- Keep commas between each object.
- Keep the quotes around team, region, and pr.
- If the team list changes, you still only update this one array.
- You do not need to manually update the dropdown or checkbox sections anymore.
