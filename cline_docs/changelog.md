# Changelog
**The Changelog is for tracking changes to the *project's* files, not CRCT operations. CRCT operations are tracked in the HDTA documents.**

### Added GitOps Integration for Submodules - 2025-05-12

**Description:** Created a new GitOps integration system for submodules to ensure automatic Git operations during task execution.

**Impact:** Eliminates the need for manual reminders to perform Git operations when using the CRCT system as a submodule.

**Files Modified:**
- Created `cline_docs/prompts/gitops_integration.md`
- Updated `.clinerules` to add `[GITOPS_REMINDER]` section
- Updated `cline_docs/activeContext.md` to reflect current focus on GitOps integration
- Updated `cline_docs/system_manifest.md` to document GitOps integration

---
