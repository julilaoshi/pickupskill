# Safety Rules

Use these rules before any real cleanup.

## Non-Destructive Default

Pickupskill never deletes by default.

Allowed default actions:

- scan
- classify
- propose
- create shallow folders
- move high-confidence files
- move uncertain files to review buckets when approved

Disallowed default actions:

- delete files
- overwrite files
- flatten software projects blindly
- move runtime dependencies without approval
- claim that cleanup is risk-free

## Approval Needed

Ask before:

- deleting anything
- moving a software project
- moving dependency folders
- merging folders with name conflicts
- renaming large batches
- moving files outside the user-specified target folder
- changing a structure the user has manually corrected

## Conflict Handling

If a destination file already exists:

1. do not overwrite it
2. compare names, sizes, and timestamps if tools are available
3. keep both files with a clear suffix if they are not confirmed duplicates
4. report the conflict

## Review Buckets

Review buckets are not trash.

They mean:

- the item was not confidently classified
- the item should stay visible
- the user should decide later

Suggested buckets:

- `review-images`
- `review-video`
- `review-documents`
- `review-design`
- `review-empty-folders`
- `review-unknown`

## Project Package Protection

Do not split a project package unless the user asks.

Common package signals:

- shared filename prefix
- source plus exports
- media plus subtitle or thumbnail
- design source plus preview
- code folders and lockfiles
- document plus image assets

## Runtime-Like Folder Protection

Leave runtime-like folders in place by default.

Examples:

- `.git/`
- `node_modules/`
- `.venv/`
- `venv/`
- `src/`
- `build/`
- `dist/`
- package lockfiles
- plugin folders
- generated runtime caches

