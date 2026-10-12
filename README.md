# LLM SkillHub plugin

Connects Claude to [LLM SkillHub](https://llmskillhub.com), a catalogue of
agent skills and the evals that test them, where every public version is
scanned and read by a person before it's listed.

## What it adds

- **MCP server** `llmskillhub` (`https://api.llmskillhub.com/mcp`, no key
  needed): search the catalogue by task, read any skill's files, and get the
  exact install command.
- **Skill `find-skills`**: when you ask for something a published skill
  already does, Claude searches, reads the skill, tells you what it needs
  access to, and installs it or follows it for the task once you agree.
- **Skill `skill-evals`**: finds evals (reviewed test suites), attaches them
  to your own skills, runs them and reads the scores, and helps you write and
  publish an eval (`manifest.yaml`, `dataset.jsonl`, rubrics).
- **Skill `publish-skill`**: packages your own instructions as a skill and
  publishes it with the `llmsh` CLI.

## Install

From Anthropic's directory once listed, or from this repository:

```
claude plugin marketplace add llmskillhub/claude-plugin
claude plugin install llmskillhub@llmskillhub
```

Installing skills into Claude Code, running evals and publishing need the CLI:
`npm install -g llmskillhub`.

## Privacy

Searches and reads go to `api.llmskillhub.com`. See the
[privacy policy](https://llmskillhub.com/privacy) and
[terms](https://llmskillhub.com/terms).

## License

MIT
