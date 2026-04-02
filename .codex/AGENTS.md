# .codex AGENTS

<!-- packetflow_foundry consumer bootstrap:start -->
## PacketFlow Foundry
- Vendor: `.codex/vendor/packetflow_foundry`
- Project-local overlays: `.codex/project/profiles/`, `.agents/skills/`, `.codex/agents/`
- `.codex/agents/` is the project-scoped subagent discovery surface. Bootstrap writes managed copies of vendored foundry agent TOMLs there from `.codex/vendor/packetflow_foundry/.codex/agents/`.
- `.agents/skills/` is a thin discovery-wrapper surface. Bootstrap writes managed copies of vendored wrappers there while reusable retained kernels stay under `.codex/vendor/packetflow_foundry/builders/packet-workflow/retained-skills/`.
- Entries that consumer bootstrap copied from the vendor subtree into `.codex/agents/` or `.agents/skills/` are managed bootstrap artifacts. Update the vendor source or replace them with a project-local entry, then rerun bootstrap instead of patching the copied artifact in place.
- Rerun consumer bootstrap after updating the vendor subtree to refresh managed agent and skill copies that were not modified locally.
- Do not edit `.codex/vendor/packetflow_foundry` for local needs.
- `.codex/project/profiles/default/profile.json` is a project-local scaffold.
- Skill-specific packet-workflow overrides may live at `.codex/project/profiles/<skill-name>/profile.json`.
- Legacy `.codex/project/agents/` is migration-only and should move to `.codex/agents/`.
- Legacy `.codex/project/skills/` is migration-only and should move to `.agents/skills/`.
<!-- packetflow_foundry consumer bootstrap:end -->
