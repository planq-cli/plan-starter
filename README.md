# PlanQ starter

This repository is a ready-to-use [PlanQ](https://planq.dev/docs/) project
template. It includes a small starter plan and a larger CRM example that share
one project resource catalog.

## Get started

Install the supported `planq` CLI for your platform by following the
[installation guide](https://planq.dev/docs/install).

Create a repository from this template in GitHub, or clone it directly:

```bash
git clone https://github.com/planq-cli/plan-starter.git
cd plan-starter
planq project validate
planq dev
```

`planq dev` opens the starter plan first and also makes `crm-demo.plan`
available in the entry switcher. To preview only the full example, run:

```bash
planq dev crm-demo.plan
```

The preview is read-only. Edit `starter.plan`, `crm-demo.plan`, and
`resources.plan` in your repository, then run `planq project validate` again.
No Node.js, Vite, or source checkout is required.

## Use a coding agent

The template does not include a pinned copy of the PlanQ Agent Skill. Install
the Skill into your project with the CLI that your agent will use:

```bash
planq skill status
planq skill install
planq skill status
```

Read `result.status` from `planq skill status`:

- `missing`: install the Skill and check the status again.
- `current`: read `.agents/skills/plan-gantt/SKILL.md` before editing plans.
- `conflict`: stop and review the reported project files; do not overwrite
  them automatically.

See the [coding-agent handoff guide](https://planq.dev/docs/getting-started/agent-skill)
for the complete workflow.

## Project files

- `starter.plan`: a small plan intended for editing.
- `crm-demo.plan`: a complete example derived from PlanQ's canonical demo.
- `resources.plan`: the shared mock people catalog for both entries.
- `plan.manifest.json`: the ordered project entry list.

## License

The files in this template repository are licensed under the MIT License. The
PlanQ CLI and product source are separate works distributed under
`PolyForm-Noncommercial-1.0.0`.
