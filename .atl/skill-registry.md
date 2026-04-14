# Skill Registry — prodecaribe-landing

**Generated**: 2026-04-09
**Mode**: SDD-engram

## Project Stack
- Astro 6 (SSG)
- Tailwind CSS
- Cloudflare Pages
- TypeScript (strict mode)
- GSAP + Lenis

---

## Available Skills

### SDD Workflow
| Skill | Trigger | Location |
|-------|---------|-----------|
| sdd-init | Initialize SDD context | ~/.config/opencode/skills/sdd-init/ |
| sdd-propose | Create change proposal | ~/.config/opencode/skills/sdd-propose/ |
| sdd-spec | Write specifications | ~/.config/opencode/skills/sdd-spec/ |
| sdd-design | Technical design | ~/.config/opencode/skills/sdd-design/ |
| sdd-tasks | Task breakdown | ~/.config/opencode/skills/sdd-tasks/ |
| sdd-apply | Implementation | ~/.config/opencode/skills/sdd-apply/ |
| sdd-verify | Verification | ~/.config/opencode/skills/sdd-verify/ |
| sdd-archive | Archive change | ~/.config/opencode/skills/sdd-archive/ |

### Project Management
| Skill | Trigger | Location |
|-------|---------|-----------|
| issue-creation | Create GitHub issue | ~/.config/opencode/skills/issue-creation/ |
| branch-pr | Create PR | ~/.config/opencode/skills/branch-pr/ |

### Code Quality
| Skill | Trigger | Location |
|-------|---------|-----------|
| judgment-day | Adversarial review | ~/.config/opencode/skills/judgment-day/ |

---

## SDD Phase Commands
```
/sdd-init          → Initialize project context
/sdd-propose       → Propose a new change
/sdd-explore       → Investigate before committing
/sdd-spec          → Write detailed specs
/sdd-design        → Create technical design
/sdd-tasks         → Break into tasks
/sdd-apply         → Implement tasks
/sdd-verify        → Verify against specs
/sdd-archive       → Archive completed change
```

---

## Project Conventions
1. Astro components in `src/components/*.astro`
2. Tailwind with custom brand colors (prode-blue, prode-gold)
3. GSAP animations: float, pulse-glow, fade-up
4. Cloudflare Pages deployment via Wrangler
5. No testing infrastructure (static site)

---

## Notes
- This is a static landing page — traditional TDD not applicable
- Type checking via `astro check` or `tsc --noEmit`
- Focus on visual regression testing if testing is needed for future work
