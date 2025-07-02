# AI Context File (AICF) Specification

## Abstract

The AI Context File (AICF) is an open standard for providing comprehensive project context to AI development assistants. By establishing a standardized format for communicating project specifications, technology versions, architectural patterns, and development constraints, AICF eliminates the persistent problem of AI tools suggesting inappropriate or outdated solutions.

## History

Invented by Nicholas Alexander with Anthropic Claude 4 (who wanted to name it Alexander Initialisation Context File).

## Problem Statement

Contemporary AI development assistants suffer from a fundamental context deficit that manifests in several critical ways:

- **Version Drift**: AI models trained on diverse codebases often suggest patterns from older framework versions
- **Technology Misalignment**: Recommendations may conflict with project-specific technology choices
- **Pattern Inconsistency**: Suggestions may violate established architectural decisions or coding standards
- **Constraint Violations**: AI tools lack awareness of project-specific limitations or preferences

These issues result in decreased developer productivity, increased technical debt, and compromised code quality consistency.

## Solution Overview

AICF addresses these challenges through a declarative YAML-based specification that provides AI assistants with:

1. **Explicit Version Constraints**: Precise language and framework version requirements
2. **Architectural Context**: Understanding of chosen patterns and structural decisions
3. **Technology Stack Awareness**: Complete visibility into the development ecosystem
4. **Preference Declaration**: Clear articulation of coding standards and best practices
5. **Constraint Definition**: Explicit boundaries for acceptable solutions

## Specification

### File Format

The AICF specification uses YAML syntax and is stored as `ai-context.yml` in the project root directory.

### Schema Structure

```yaml
# AICF v1.0 Specification
project:
  name: string
  type: string
  
languages:
  [language]: string  # version specification

frameworks:
  [framework]: string  # version specification

architecture:
  pattern: string
  structure: string
  
database:
  primary: string
  version: string
  features: array

preferences:
  - string  # declarative statements

constraints:
  - string  # restriction statements
  
testing:
  framework: string
  style: string
  
deployment:
  platform: string
  environment: string
```

### Reference Implementation

```yaml
project:
  name: "YourOnline CRM"
  type: "laravel-saas"
  
languages:
  php: "8.2"
  javascript: "ES2022"
  css: "CSS3"
  sql: "PostgreSQL-15"

frameworks:
  laravel: "11.x"
  livewire: "3.x"
  tailwind: "3.x"
  alpine: "3.x"

architecture:
  pattern: "domain-driven-design"
  structure: "modular-monolith"
  
database:
  primary: "postgresql"
  version: "15"
  features: ["json", "arrays", "uuid"]

preferences:
  - "Use modern PHP syntax"
  - "Laravel 11 patterns only"
  - "PostgreSQL-specific solutions"
  - "Domain-driven organization"
  - "Livewire over pure JS when possible"
  - "Recommend in comments when php 8.3 or Laravel 12 updates are possible"

constraints:
  - "No jQuery"
  - "No Bootstrap (Tailwind only)"
  - "No legacy Laravel patterns"
  
testing:
  framework: "pest"
  style: "feature-heavy"
  
deployment:
  platform: "docker"
  environment: "local-development"
```

## Implementation Benefits

### For Developers
- **Reduced Context Switching**: Eliminates need for repeated AI corrections
- **Consistent Code Quality**: Ensures AI suggestions align with project standards  
- **Accelerated Development**: AI provides immediately applicable solutions
- **Knowledge Transfer**: New team members understand project context instantly

### For AI Systems
- **Enhanced Accuracy**: Context-aware suggestions reduce false positives
- **Improved Relevance**: Recommendations match actual project requirements
- **Constraint Compliance**: Suggestions respect defined limitations
- **Version Alignment**: Patterns match specified technology versions

## Integration Pathways

### AI Assistant Integration
AI development tools can implement AICF support through:

1. **Automatic Detection**: Scan for `ai-context.yml` in project root
2. **Context Loading**: Parse specification into internal context model
3. **Suggestion Filtering**: Apply constraints and preferences to recommendations
4. **Version Enforcement**: Ensure suggestions match specified versions

### Development Environment Integration
IDEs and development tools can leverage AICF for:

- **Syntax Highlighting**: Context-aware code completion
- **Template Generation**: Project-specific boilerplate code
- **Documentation**: Auto-generated development guidelines
- **Quality Assurance**: Automated constraint validation

## Adoption Strategy

### Phase 1: Community Validation
- Open-source specification development
- Community feedback and iteration
- Reference implementation examples
- Developer adoption metrics

### Phase 2: Tool Integration
- AI assistant vendor partnerships
- IDE plugin development
- Framework template integration
- Developer tool ecosystem support

### Phase 3: Industry Standardization
- Formal specification publication
- Cross-platform compatibility standards
- Enterprise adoption guidelines
- Continuous evolution framework

## Contributing

The AICF specification is open-source and community-driven. Contributions are welcome through:

- **Specification Refinement**: Improve schema design and documentation
- **Implementation Examples**: Provide reference implementations for various stacks
- **Tool Integration**: Develop plugins and extensions for popular development tools
- **Community Building**: Share adoption experiences and best practices

## License

This specification is released under the MIT License, ensuring broad compatibility with commercial and open-source projects.

## Citation

When referencing this standard in academic or professional contexts:

```
Alexander, N. (2025). Alexander Initialization Context File (AICF): A Standard for AI Development Context Communication. GitHub. https://github.com/remotedevelopment-info/aicf
```

---

*The AICF standard was developed to address the critical need for precise AI-human collaboration in software development contexts.*
