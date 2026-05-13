---
name: pickupskill
description: Cautiously organize messy working folders by scanning loose files, protecting project packages, moving high-confidence items into shallow groups, and sending uncertain items to review buckets without deleting by default.
---

# Pickupskill

## Position

Pickupskill helps organize messy working folders safely.

It is designed for folders where users keep dropping loose files, downloads, references, creative assets, documents, video exports, and project packages.

Its main job is not to create a perfect archive. Its job is to make a messy active workspace easier to understand without damaging the user's work.

## When To Use

Use this Skill when the user asks to:

- clean up a messy folder
- organize loose files in a working directory
- sort downloads, screenshots, images, video exports, documents, or project packages
- review what can be moved safely
- build a shallow folder structure for active work
- separate obvious files from uncertain files

Do not use it for:

- deleting files by default
- blindly moving software projects, runtime dependencies, or build folders
- deep archival taxonomy design
- legal, medical, or compliance document retention decisions
- destructive cleanup without explicit user approval

## Core Safety Rules

1. Never delete by default.
2. Scan before moving.
3. Move only high-confidence items.
4. Keep uncertain items in a review bucket.
5. Keep obvious project packages together.
6. Keep folder depth shallow.
7. Preserve names that are already readable.
8. Treat root-level loose files as the first cleanup target.
9. User decisions override prior guesses.
10. Stop and ask before moving anything that looks like a runtime dependency.

## Folder Depth Rule

Prefer shallow structures:

- level 1: broad group or project entry
- level 2: subcategory or active working group
- level 3: only for real project packages

Avoid creating level 4 folders unless the user explicitly asks.

## Review Bucket Rule

If an item cannot be classified with high confidence, do not force it into a category.

Use review buckets such as:

- `review-images`
- `review-video`
- `review-documents`
- `review-design`
- `review-unknown`

Folder names created by this Skill should stay in English, regardless of whether the user writes in English, Chinese, or another language.

The response language should follow the user:

- reply in Chinese for Chinese users
- reply in English for English users
- keep newly created folder names in English in both cases

This keeps folder structures portable across systems, tools, and collaborators.

## Project Package Rule

Before moving files, decide whether a folder or group is a project package.

Signals of a project package may include:

- source files plus exports
- matching media and captions
- design files plus references
- `package.json`, `src/`, `public/`, `.git/`, or build configuration
- documents plus supporting images
- repeated prefix or shared project name

Do not break project packages apart just because their contents could fit several categories.

## Runtime And Dependency Caution

Stop and ask before moving folders that look like software projects or runtime dependencies.

Signals include:

- `.git/`
- `node_modules/`
- `venv/`
- `.venv/`
- `package.json`
- `pyproject.toml`
- `requirements.txt`
- `Cargo.toml`
- `go.mod`
- `src/`
- `dist/`
- `build/`
- lockfiles
- plugin, extension, or runtime folders

Default action:

1. classify them as project or runtime-like folders
2. list why moving them may be risky
3. leave them in place unless the user approves

## Workflow

### 1. Scan

Inspect the target folder before moving anything.

Gather:

- root-level loose files
- existing folders
- obvious project packages
- empty folders
- possible runtime or dependency folders
- ambiguous files

### 2. Classify

Classify items into:

- safe to move
- keep together as project package
- runtime-like or dependency-risk
- review bucket
- empty folder pending user decision

### 3. Propose

Before making file moves, produce a concise plan:

```text
Safe moves:
Keep in place:
Review bucket:
Do not move without approval:
Proposed shallow folders:
```

If the user has already approved direct cleanup, execute only the safe moves and report the rest.

### 4. Move Carefully

When moving files:

- avoid overwriting existing files
- preserve extensions
- preserve readable names
- keep matching pairs together, such as video plus subtitle
- use suffixes when name conflicts exist
- do not chase files the user has already moved manually

### 5. Re-scan

After moving, scan again.

Report:

- what moved
- what stayed
- what needs review
- any empty folders
- any risky objects that were not moved

## Naming Rules

Rename only when it improves clarity.

Prefer not to rename:

- already readable names
- versioned exports
- files with user-provided titles
- runtime files
- project files

Consider renaming:

- camera names such as `IMG_0042`
- pure numeric names
- obvious duplicate names
- files that need to be paired with a related asset

Do not hide important metadata such as dates, versions, or export markers.

## Empty Folder Rule

Do not delete empty folders by default.

If empty folders are found:

1. list them
2. move them only to an explicit review area if the user approved cleanup moves
3. otherwise leave them in place and ask

Recommended review folder:

```text
review-empty-folders
```

## Output Format

For planning:

```text
Current read:
Root-level loose files:
Project packages:
Safe moves:
Review bucket:
Risky or dependency-like items:
Empty folders:
Proposed structure:
Need approval:
```

For completed cleanup:

```text
Moved:
Kept in place:
Review bucket:
Not moved because risky:
Empty folders:
Next decision:
```

## Public Safety Rules

This public Skill must not contain private workspace assumptions.

Do not include:

- local absolute paths
- private project names
- user-specific folder structures
- personal identities
- school, team, client, or employer names
- private migration rules
- API keys, tokens, cookies, emails, or phone numbers

Examples should use synthetic folder trees.

## Standalone Execution Contract

This Skill should still be useful without any private local workflow.

If no file-moving tool is available, produce a safe cleanup plan.

If file-moving tools are available, use reversible moves, avoid overwrites, and report every action.

When in doubt, leave the item in place or move it to a review bucket only after approval.
