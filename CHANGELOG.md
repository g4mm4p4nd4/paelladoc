# Changelog
All notable changes to PAELLADOC will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.2.1] - 2025-04-06

### Added
- Nuevo script `run_continue.py` para mejorar la funcionalidad del comando CONTINUE

### Changed
- Mejorado el sistema de interactividad de los comandos PAELLA y CONTINUE para presentar una pregunta a la vez
- Refactorizado los scripts subyacentes para usar rutas relativas en lugar de absolutas
- Mejorada la detección de proyectos en subdirectorios para el comando CONTINUE
- Actualizado el script `run_generate_doc.py` para mejorar su portabilidad

### Fixed
- Corregido el comportamiento de los comandos para respetar la configuración de interactividad
- Solucionado el problema con la detección de la raíz del proyecto
- Arreglado el script de CONTINUE para mostrar un mensaje adecuado cuando no hay proyectos disponibles

## [0.2.0] - 2025-04-05

### Added
- **Dynamic Template-Based Menu System**: Replaced fixed menu with a dynamic menu generated from existing templates
- **Improved Multilingual Support**: Implemented full support for both Spanish and English in documentation generation
- New `enforce_fixed_menu.py` script modified to generate a dynamic menu from templates
- Documentation file creation now uses templates as structural guides
- Reorganized output instructions to save documentation to `/docs/generated/`
- Improved integration between dynamic menu and documentation file generation

### Changed
- GENERATE_DOC command configuration now supports additional templates
- Generated files are now always saved in `/docs/generated/` while following template structure
- Improved template organization and integration with the documentation system
- System now respects user's language selection, without forcing Spanish or English

### Fixed
- Fixed issues with documentation output file location
- Solved inconsistency between menu and available templates
- Improved documentation file saving process

## [0.1.0] - 2024-04-04

### Breaking Changes
- Implementation of repository documentation generation system (GENERATE_DOC)
- Addition of code repository analysis and documentation extraction capabilities
- Comprehensive reorganization of the `.cursor/rules` directory structure
- Enhanced modularity with clearer separation of concerns
- Addition of new interfaces and conversation workflows
- Improved documentation of the system architecture

### Added
- **Repository Analysis & Documentation**: New GENERATE_CONTEXT and GENERATE_DOC commands for code-to-documentation reverse engineering
- Repository context extraction scripts and analysis tools
- Interactive documentation generation from repository analysis
- Repository content extraction to optimized text format
- Architecture pattern detection and automatic documentation
- Multi-step repository documentation process with user guidance
- New help system in `core/help.mdc`
- User interface definitions in `features/interfaces.mdc`
- Enhanced conversation workflow in `features/conversation_workflow.mdc`
- Detailed directory structure documentation in `DIRECTORY_STRUCTURE.md`
- Feature mapping documentation in `feature_map.md`
- Configuration file for conversation flows in `paelladoc_conversation_config.json`
- New template directories:
  - `templates/conversation_flows/` for conversation configurations
  - `templates/methodologies/` for development methodologies
  - `templates/Product/` for main product documentation
  - `templates/scripts/` for template-specific scripts
  - `templates/selectors/` for selection guide templates
  - `templates/simplified_templates/` for simplified documentation
- Improved organization of code generation templates

### Changed
- Modular architecture with cleaner file organization
- Enhanced product management capabilities
- Improved code generation system
- Better documentation of the directory structure
- Enhanced mapping between features and their implementations
- Reorganized template structure for better maintainability

### Fixed
- Directory structure inconsistencies
- Feature implementation mapping gaps
- Template organization clarity
- Documentation of system architecture

## [2.0.0] - 2024-03-12

### Breaking Changes
- Complete restructuring for Cursor 0.47 compatibility
- New `.cursorrules` architecture for dynamic rule loading
- Changed template organization structure
- Modified AI interaction patterns
- Updated for Cursor's new MDC format

### Added
- Dynamic rule loading system with priorities
- Timestamp management system with multiple formats
- AI operation modes (autonomous, collaborative, advisory)
- Template hooks system for automation
- Enhanced memory system with better categorization
- Comprehensive template organization in `.cursor/rules/templates/`
- New documentation validation system
- Support for Cursor 0.47 features
- Automatic deep research system for market research documents
- Comprehensive market validation with cross-referencing
- New `FORCE_RESEARCH` command for mandatory automatic document research
- Architecture Decision Record (ADR) lifecycle management
- `UPDATE_ADR` command for architectural decision tracking
- Proper timestamping system for all generated documents
- Frontmatter YAML management with metadata standardization
- Template variable substitution with context-aware values
- Confidence scoring system for research reliability
- Deep validation system with multiple verification levels
- Global priorities configuration for research automation
- Document settings with standardized formatting rules
- Automatic MDC generation from completed documentation
- `GENERATE_MDC` command for creating development MDC files
- Documentation completeness tracking and reporting
- Seamless transition from documentation to development
- Automatic extraction of development rules from docs
- Improved MDC generation system with true orchestrator architecture
- Dedicated MDC template focusing on referencing documentation
- Enhanced MDC structure with explicit source references for each rule
- Clear separation between documentation and MDC orchestration
- File pattern-based rules mapping to specific documentation files

### Changed
- Moved to new Cursor 0.47 rules architecture
- Improved command structure with more specific arguments
- Enhanced template system organization
- Updated priorities system with descriptions
- Improved documentation structure validation
- Enhanced security review system
- Optimized for Cursor 0.47 performance
- Enhanced the CONTINUE workflow with automatic research detection
- Modified document generation to include academic references
- Updated market research process to validate all claims with 3+ sources
- Improved document templates with proper YAML frontmatter
- Enhanced research workflow to prevent hallucinations
- Optimized command structure for professional use cases
- Modified CONTINUE to check documentation completeness
- Added auto-detection of documentation completeness
- Enhanced workflow to offer MDC generation when ready
- Changed MDC file extension to .mdc.example for clarity on required renaming
- Improved CONTINUE workflow to automatically generate MDC when user indicates documentation is complete
- Added explicit "MARK DOCUMENTATION AS COMPLETE" option to trigger immediate MDC generation
- Redesigned MDC generation to act as a true orchestrator that references documentation instead of duplicating it
- Updated messages to clearly explain the orchestrator role of the MDC file

### Fixed
- Timestamp generation in document frontmatter
- Template variable substitution during document creation
- Research workflow to prioritize automatic data gathering
- Documentation structure validation for market research
- MDC file generation path to store files in the project's directory instead of a fixed location
- Instructions for using generated MDC file and documentation in the actual development project
- MDC structure to properly reference documentation files instead of duplicating content

### Removed
- Old Cursor integration methods
- Legacy template structure
- Deprecated command formats
- Support for Cursor versions below 0.47

## [1.0.0] - 2024-03-11

### Added
- Initial release of PAELLADOC
- Basic MECE documentation system
- Core commands (PAELLA, CONTINUE, ACHIEVEMENT, ISSUE, DECISION, MEMORY, VERIFY)
- Basic template system
- Documentation structure
- Memory system
- Project directives 