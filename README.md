# Agent Skills

A shared skills repository for installing focused skills into other projects.

## How To Use

From another project, install one skill by name:

```bash
npx skills add https://github.com/isomoes/skills --skill creating-figures
```

If the repo is published to the skills directory and supports the short form, you can also install from the repo slug:

```bash
npx skills add isomoes/skills
```

For general repo installs, a practical layout looks like this:

```text
repo-A/                    # your application project
repo-B/                    # another application project
skills/                    # central shared skills repo
```

Then in each project:

```bash
cd repo-A
npx skills add https://github.com/isomoes/skills --skill creating-figures

cd ../repo-B
npx skills add https://github.com/isomoes/skills --skill pdf
```

This gives you:

- one central repo to maintain
- one CLI command to import a specific skill into any project
- no need to copy all skills everywhere

If you are also using OpenAI Codex, its docs say Codex supports installed skills and symlinked skill folders when scanning skill locations. That can be useful for local shared development instead of repeated installs.

A solid team convention is:

```text
skills/
├── skills/
│   ├── creating-figures/
│   │   └── SKILL.md
│   ├── find-skills/
│   │   └── SKILL.md
│   └── pdf/
│       └── SKILL.md
```

Each skill folder name should match the CLI name passed after `--skill`.

## Project Structure

- `skills/creating-figures/` - Create publication-quality scientific figures with TikZ
- `skills/find-skills/` - Discover and install useful skills
- `skills/pdf/` - Work with PDF extraction, forms, splitting, and merging

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
