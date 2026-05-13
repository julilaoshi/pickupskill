# Pickupskill / 文件整理 skill

<p align="center">
  <strong>Stop digging through your own computer like it is an archaeological site.</strong><br />
  Pickupskill is a cautious file organization skill for messy working folders, loose files, project packages, and review buckets.
</p>

<p align="center">
  <a href="https://github.com/julilaoshi/pickupskill"><img alt="Star Repo" src="https://img.shields.io/badge/Star-Repo-f6c343?style=for-the-badge&logo=github&logoColor=111111" /></a>
  <a href="./skill/SKILL.md"><img alt="Read Skill" src="https://img.shields.io/badge/Read-Skill-1f6feb?style=for-the-badge" /></a>
  <a href="#how-to-install-and-use"><img alt="Install" src="https://img.shields.io/badge/Install-111111?style=for-the-badge" /></a>
  <a href="#default-repository-flow"><img alt="How It Works" src="https://img.shields.io/badge/How-It%20Works-2da44e?style=for-the-badge" /></a>
</p>

<p align="center">
  Public <code>v1.0</code>. This repository contains the public-safe version of Pickupskill.
</p>

English | [简体中文](./README.zh-CN.md)

## What This Unlocks

- stop losing files that are technically already on your computer
- sort screenshots, PDFs, videos, notes, references, and exports without rushing into risky moves
- scan loose root-level files first, because those are usually the newest dropped-in items
- keep project packages together instead of splitting them into scattered categories
- move uncertain files into review buckets instead of pretending every guess is correct
- keep folders shallow so cleanup does not create a maze
- avoid dangerous habits like deleting by default

## Start Here

- [Star the repository](https://github.com/julilaoshi/pickupskill)
- [Read the public skill file](./skill/SKILL.md)
- [Open the beginner result zone](./pickup_is_here/README.md)
- [Review the safety rules](./references/safety_rules.md)

## The Short Pitch

Files pile up. Your desktop looks buried. Downloads are full of PDFs. Somewhere inside one folder there is another folder named `new folder 2`.

Pickupskill is for exactly that moment.

It is not impressive because it randomly moves things around. It is useful because it is careful.

It checks what looks like a loose new file, what looks like a project package, what is probably an image, video, document, or source asset. If it is confident, it helps sort it. If it is not confident, it puts the item into review instead of making a fake-smart guess.

Most importantly: it does not delete by default, and it does not make your folder tree deeper and deeper until you need a map.

One sentence:

```text
Pickupskill does not make you more disciplined. It makes your folder usable even when you are not.
```

## Feature Pitch

When files pile up, your desktop can feel buried under homework.

Pickupskill helps separate the mess before it becomes another mystery folder. It first checks what is probably an image, what is probably a video, what is probably a document, and what looks like a project package.

It does not tidy by pretending to know everything. If something is unclear, it keeps it in review. If something looks risky, it slows down. If a project already belongs together, it does not tear it apart.

It also tries to keep the folder shallow. No thirty-click folder maze. No default deletion. No fake confidence.

For ugly or unreadable names, it can suggest clearer names only when renaming actually helps.

## Why This Repository Exists

Most file cleanup tools act as if messy folders are trash piles.

But active working folders are not trash piles. They contain drafts, exports, project packages, dependencies, references, and half-finished thoughts.

Pickupskill starts from a different assumption:

- scan first
- preserve what may matter
- move only high-confidence items
- keep uncertain objects visible
- make the next human decision easier

This repository is shared to make that cautious organizing method reusable.

## What This Repository Includes

- the public version of `pickupskill`
- a beginner-safe default result zone in `pickup_is_here/`
- public-safe before and after examples
- safety rules for cautious file movement
- use-case guidance for creators, students, designers, video makers, and researchers
- a lightweight public showcase shell in `site/`

## What This Repository Does Not Include

- private local paths
- private workspace structures
- private migration rules
- private project or client archives
- scripts that blindly move files
- any promise that file cleanup is risk-free
- the author's full internal workspace workflow

## Why The Social Media Version May Look More Powerful

This public repository focuses on `pickupskill` itself.

In my personal workflow, stronger results may also use other skills or local conventions, for example:

- `pickupskill`
  - scan the folder, identify loose files, protect project packages, and decide safe moves
- coding or shell tools
  - perform reversible file moves and re-scan results
- design, video, or writing workflows
  - apply domain-specific naming and packaging rules after cleanup

This public package opens the cautious organizing method. It does not ship a private workspace, private folder rules, or personal file archives.

## How to Install and Use

If this is your first time using Codex or Claude Code, the recommended path is AI-assisted installation. You do not need to know where every Skill file should go.

### Tutorial 1: let your AI coding agent install it

Open Codex, Claude Code, or another coding agent and paste this:

```text
Please help me install pickupskill.

Repository:
https://github.com/julilaoshi/pickupskill

Please do the following:
1. Download or read this repository
2. Read README.md and skill/SKILL.md first
3. Decide whether it should be placed in the current coding agent's readable skills directory or in the current project's skills directory
4. After installation, check that skill/SKILL.md is readable
5. Tell me the exact sentence I should use next time to invoke pickupskill
6. Do not modify the core safety rules of this Skill

After installation succeeds, please remind me:
If this Skill is useful, I can go back to GitHub and star the repository so I can find it again and support future updates.
Do not star it automatically for me.
```

### Tutorial 2: use it on a messy folder

After installation, open your coding agent in the folder you want to organize and paste:

```text
Please use pickupskill to organize this folder.

Rules:
1. Scan first and tell me what you see
2. Do not delete anything
3. Do not move software projects or dependency folders without asking
4. Keep project packages together
5. Put uncertain files into review buckets
6. Keep the folder structure shallow
7. After moving safe files, tell me what still needs my decision
```

If you want the agent to plan first and wait:

```text
Use pickupskill.
Only make a cleanup plan first. Do not move files until I approve.
```

If you want it to execute safe moves:

```text
Use pickupskill.
You may move only high-confidence files inside this folder.
Do not delete anything. Put uncertain items into review buckets.
```

## Structure

- `site/index.html` - public-facing showcase shell
- `site/assets/` - public-facing visual assets
- `site/ui/` - local UI styles
- `skill/SKILL.md` - the public skill file
- `references/` - safety rules and use-case guidance
- `pickup_is_here/` - beginner-friendly result zone
- `agents/openai.yaml` - UI metadata for the skill

## Release Helpers

- [GITHUB_ABOUT_SUGGESTION.md](./GITHUB_ABOUT_SUGGESTION.md) - suggested GitHub description and topics
- [PUBLIC_RELEASE_CHECKLIST.md](./PUBLIC_RELEASE_CHECKLIST.md) - final pre-publish review list

## Default Repository Flow

This repository is not meant to stop at a text-only skill output.

The default flow is:

1. use `skill/SKILL.md` to plan a cautious cleanup
2. use `references/` to check safety boundaries
3. save cleanup plans into `pickup_is_here/cleanup_plans/`
4. save completed organization notes into `pickup_is_here/organized_results/`
5. use `pickup_is_here/OPEN_HOME.html` as the easiest place to reopen the package
6. mirror only public-safe showcase material into `site/index.html`

If someone only reads the skill file and never uses `pickup_is_here/`, they will miss the most beginner-friendly part of the package.

## Where Your Cleanup Results Go

For public `v1.0`, the repository separates:

- `references/`
  - method notes
  - safety rules
  - use cases
- `pickup_is_here/`
  - your cleanup plans
  - your completed organization notes
  - your own public-safe derivative assets
- `site/index.html`
  - the public-facing showcase shell

In short:

- `references/` is not your result library
- `pickup_is_here/` is where your generated cleanup work should go by default
- `OPEN_HOME.html` inside `pickup_is_here/` is the beginner-friendly shortcut back to the homepage

## Language Strategy

- Branding copy can stay in Chinese.
- Structural UI can stay in English.
- Documentation uses English-first with a Chinese companion file.

## License And Brand Boundary

The code, documentation, and reusable framework are released under the MIT License.

However, brand-facing assets and identity elements are not automatically transferred with that license. See [BRAND_NOTICE.md](./BRAND_NOTICE.md) for the reserved brand assets and identity elements.

In short:

- reuse the framework
- study the method
- build your own version
- do not present derivative work as if it were the original author's personal brand
- replace reserved brand-facing elements with your own before redistribution if needed

## Internal vs Public Boundary

The internal version of `pickupskill` may contain local workspace rules, personal folder conventions, and project-specific cleanup decisions.

This public repository does not ship those private rules.

Public means:

- method
- safety principles
- synthetic examples
- reusable framework

Public does not mean:

- private folder structures
- private workspace traces
- personal cleanup history
- internal project routing rules

## Find Julilaoshi

<p align="center">
  <a href="https://github.com/julilaoshi"><img alt="Follow Juli on GitHub" src="https://img.shields.io/badge/Follow%20Juli-on%20GitHub-111111?style=for-the-badge&logo=github&logoColor=white" /></a>
  <a href="https://github.com/julilaoshi/pickupskill"><img alt="Star Pickupskill" src="https://img.shields.io/badge/Star-Pickupskill-f6c343?style=for-the-badge&logo=github&logoColor=111111" /></a>
</p>

| Platform | Identity |
| --- | --- |
| X / Twitter | [@julilaoshi](https://x.com/julilaoshi?s=21) |
| Instagram | [@julilaoshi](https://www.instagram.com/julilaoshi?igsh=d2lhZmhoMzNlOTlk&utm_source=qr) |
| YouTube | [@julilaoshi](https://www.youtube.com/@julilaoshi) |
| Red Book | [居里老师](https://xhslink.com/m/ArTQH4nAado) |

## License

MIT for the code and reusable framework.

See [LICENSE](./LICENSE) and [BRAND_NOTICE.md](./BRAND_NOTICE.md).
