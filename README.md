# How I build and test agents before they ship (concept demo)

**Live demo:** https://saeedfzn.github.io/agent-testing-pipeline-demo/

An agent that works in a demo is easy; one you can put in front of customers needs a clear setup, a review that hunts for what's wrong, tests that catch regressions, and a pipeline that refuses to ship a worse version. This one-page demo walks through each step for a sample support-triage agent.

- **Agent setup:** an interactive diagram of the orchestrator, its instructions file, sub-agents (classifier, reply drafter, policy checker), tools (an MCP server and REST tools) and code guardrails
- **Adversarial review panel:** four reviewer sub-agents raise ten findings on a pull request; you mark each one verified or rejected against its evidence, and half turn out to be false positives
- **Eval suite:** twelve deterministic test cases across four versions, with a pass-rate gate and regression tracking against the baseline (the last version that cleared the gate)
- **CI/CD pipeline:** a GitHub Actions workflow (lint, unit tests, agent evals with a gate, staging deploy, smoke test, approved promotion), with a simulation of a failing eval blocking deployment
- **Production monitoring:** runs, cost per run, failure categories and clickable traces
- **How I work with Claude Code:** project instructions, MCP and skills, sub-agent review panels and verification habits

Plain HTML, CSS and JavaScript in one file, no dependencies. Everything is simulated with made-up data and illustrative prices; nothing calls a model. The workflow YAML is a sketch written for this demo.

Built by Faizaan Saeed. Claude is a trademark of Anthropic. GitHub and GitHub Actions are trademarks of GitHub, Inc. Azure DevOps is a trademark of Microsoft. Independent demo.
