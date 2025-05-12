# System: CRCT Submodule

## Purpose
Provides a structured framework for recursive chain-of-thought reasoning and project management, configured to operate as a submodule with all output stored within the submodule directory.

## Architecture
[parent_project] --> [src] + [docs]
                 |
                 +--> [.crct] --> [cline_docs] + [cline_utils]
                       |
                       +--> [.clinerules] (submodule config)
                       |
[.clinerules-parent] --+

## Module Registry
- [src]: Core implementation code (in parent repository)
- [docs]: Project documentation (in parent repository)
- [.crct/cline_docs]: CRCT system operational memory
- [.crct/cline_utils]: CRCT system utilities, including dependency tracking

## Development Workflow
1. Initialize the CRCT system as a submodule
2. Configure the system to store all output in the submodule directory
3. Run dependency analysis to populate trackers
4. Verify and resolve placeholder dependencies
5. Proceed with the standard CRCT workflow (Strategy → Execution → Cleanup/Consolidation)

## GitOps Integration
The CRCT submodule includes built-in GitOps integration to ensure proper version control when used as a submodule:

1. **Automatic Branch Management**: Creates feature branches based on task type and name
2. **Conventional Commits**: Generates standardized commit messages
3. **Seamless Integration**: Automatically performs Git operations at the beginning and end of task execution
4. **Reminder System**: Includes a reminder system to ensure GitOps operations are not forgotten

Key files:
- `.clinerules`: Contains GitOps configuration in `[GITOPS_WORKFLOW]` and `[GITOPS_REMINDER]` sections
- `cline_docs/prompts/gitops_plugin.md`: Detailed GitOps workflow instructions
- `cline_docs/prompts/gitops_integration.md`: Submodule-specific integration instructions

## Version: 1.0 | Status: Setup
