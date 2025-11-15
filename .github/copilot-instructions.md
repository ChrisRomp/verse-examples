# Copilot Instructions for Verse/UEFN Codebase

## Overview
This repository contains a large collection of Verse scripts for UEFN/Fortnite Creative, organized by gameplay domain (abilities, object manipulation, player management, etc.). Most scripts are authored by the project owner, with some extensions from other creators. The codebase is modular, with each script or system in its own file or subfolder.

## Architecture & Structure
- **Major Folders:**
  - `Ability Scripts/`: Individual ability scripts (e.g., `invisibility.verse`, `life_steal.verse`)
  - `Object Manipulation Scripts/`: Systems for object logic, including submodules like `CrateSystem/`
  - `Player Manipulation Scripts/`: Player state, persistence, and stat management
  - `Fortnite/`, `UnrealEngine/`, `Verse/`: Digest/reference files for APIs and language features
  - `vproject/`: Project configuration
- **Digest Files:** (`*.digest.verse`) contain API definitions and are the source of truth for function signatures and usage.
- **Reference & Patterns:** Local `.github/instructions/` files and referenced `.verseRules/` files define project-specific patterns, error handling, and best practices. Always check these before implementing or suggesting code.

## Key Conventions
- **Pattern-First:** Always search for and follow patterns in `verse-patterns.md` and local instructions before inventing new solutions.
- **Explicit API Usage:** Quote API signatures from digest files and explain their use. Handle all possible return values.
- **Error Handling:** Follow the two-phase error resolution protocol. Document error messages, research in `verse-code-database.md`, and only implement fixes after documenting findings.
- **Documentation:** Use `#` for comments. Document complex logic, edge cases, and design decisions. Reference the source of patterns and APIs.
- **Testing:** Test components in isolation. Use mocks for dependencies. Document test cases and edge conditions.

## Developer Workflow
1. **Design First:** Review requirements and plan using the feature request template if adding new features.
2. **Reference Search:** Before coding, search for patterns, error cases, and API definitions in local reference files and digest files.
3. **Implementation:** Follow established patterns, document reasoning, and keep code modular and clear.
4. **Verification:** Check against verification checklists and ensure error handling and documentation are complete.
5. **Review:** Ensure code follows project conventions, is well-documented, and passes all tests.

## Examples
- **Crate System:** See `Object Manipulation Scripts/CrateSystem/` for a modular system with its own README and settings.
- **Player Management:** `Player Manipulation Scripts/Persistence/` contains reusable modules for player state and stats.

## Integration & Extensibility
- New scripts should be placed in the appropriate domain folder and follow the modular, single-responsibility pattern.
- Cross-component communication should use events or clearly defined interfaces, as seen in digest files and system modules.

## References
- `.github/instructions/` for project rules and best practices
- `.verseRules/` for language and pattern references
- Digest files for API definitions
- Local READMEs for system-specific guidance

> **Always prefer local documentation and patterns over general knowledge. Reference specific files and document your reasoning for all changes.**
