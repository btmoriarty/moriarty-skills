# moriarty-skills

A Claude plugin marketplace for three skills, each built and maintained in its own repo:

- **kochab** ([btmoriarty/kochab](https://github.com/btmoriarty/kochab)): a personalized resume-based job-search assistant that runs a recurring scan and everything downstream of it. You always send.
- **pherkad** ([btmoriarty/pherkad](https://github.com/btmoriarty/pherkad)): a voice validator that checks whether a draft still sounds like you, with a dependency-free linter for AI-writing tells.
- **algol** ([btmoriarty/algol](https://github.com/btmoriarty/algol)): a review control plane for Claude Code. It governs how a project reviews code and keeps a record of every decision; it reviews nothing itself.

## Install

In Claude Code or Cowork, add the marketplace once, then install what you want:

```
/plugin marketplace add btmoriarty/moriarty-skills
/plugin install kochab@moriarty-skills
/plugin install pherkad@moriarty-skills
/plugin install algol@moriarty-skills
```

This marketplace points at each tool's own repo, so you install the current `main`. To refresh after an update, run `/plugin marketplace update`.

## Notes

Each plugin's version is set in its own `.claude-plugin/plugin.json` and is what Claude uses, so a plugin's manifest version moves with its release. The entries here track each repo's `main`; pin a plugin to a tag or an exact commit by adding a `ref` or `sha` to its `source` if you want a fixed version.
