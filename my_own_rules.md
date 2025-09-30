##################################################################
# 🚨 CRITICAL: DOCUMENTATION IS NON-NEGOTIABLE 🚨
# 📁 ALWAYS CHECK FOR docs/ FOLDER FIRST
# 📝 ALWAYS UPDATE CHANGELOG AFTER ANY CODE CHANGE
# 🏗️ ALWAYS MAINTAIN PROJECT STRUCTURE DOCUMENTATION
##################################################################

- Always maintain a dedicated `docs/` folder at the project root containing two essential documentation files: `changelog.md` and `project_structure.md`.
- **🔍 MANDATORY INITIAL CHECK FOR EVERY TASK/REQUEST**: Before starting any code work, task, or request, **ALWAYS** review `docs/changelog.md` and `docs/project_structure.md` to understand the current project state, history, and architecture - this is non-negotiable.
- **🔄 IMMEDIATE SETUP**: Check if `docs/` folder exists - if not, CREATE IT IMMEDIATELY with both documentation files inside. If files exist elsewhere, move them INTO the `docs/` folder - this is MANDATORY. If files don't exist, create them inside `docs/` folder with appropriate initial content - DO THIS FIRST.
- **🔍 DOUBLE-CHECK REQUIREMENT FOR EVERY UPDATE/TASK/REQUEST**: For EVERY single update, task, or request, the AI must:
  - **Double-check the entire project structure** by listing directories and examining file organization
  - **Read the complete `docs/project_structure.md`** file to understand the current documented architecture
  - **Compare the actual project structure** with the documented structure
  - **Check if `project_structure.md` needs updating** based on the last update or changes made - if any discrepancies are found, UPDATE IT IMMEDIATELY before proceeding
  - **Verify changelog.md** is current and add entries for any structural changes
  - **MANDATORY SYNC TRIGGER**: If ANY file/folder is added, deleted, moved, or renamed; or if a file’s purpose, title, or section/topic changes, you MUST update `docs/project_structure.md` IMMEDIATELY to reflect the new current architecture. Do not defer.
- The `changelog.md` serves as a historical record of all code modifications with timestamped entries in format `# YYYY-MM-DD HH:MM` listing every modified file with descriptions.
- The `project_structure.md` provides complete CURRENT architectural documentation including visual directory trees (📁/📄), component relationships, configuration details, and implementation guidelines.
- **🚫 STRICT PROHIBITION**: `project_structure.md` MUST NEVER contain "## 🔍 Recent Implementations", "last updates", "recent changes", or any historical tracking sections. These belong in `changelog.md` ONLY.
- **📋 SEPARATION OF CONCERNS**: Project structure = current architecture snapshot. Changelog = historical change log. NEVER MIX THESE RESPONSIBILITIES.
- **🔄 UPDATE RELIGIOUSLY**: Update changelog after EVERY code change, and update `project_structure.md` on EVERY tree change (add/delete/move/rename) or role/title/section change - NO EXCEPTIONS.
- **📋 THIS IS SACRED**: Use this documentation system for historical tracking, team onboarding, architectural reference, and maintaining project transparency - NEVER SKIP THIS.
- **🎯 REMEMBER**: Well-documented projects are professional projects - treat documentation as important as the code itself.
- **⚠️ FINAL WARNING**: No code changes, tasks, or requests without reviewing and updating documentation - this is not optional, it's essential!
- **🔥 ROBUST ENFORCEMENT**: For every single task or request, the AI must confirm it has checked both `docs/changelog.md` and `docs/project_structure.md` before proceeding - no shortcuts allowed.
- **🚫 ABSOLUTE MANDATE**: If project structure has changed, DO NOT proceed with any task until `docs/project_structure.md` is fully updated and synchronized with the actual project layout.

##################################################################
# 📁 DOCUMENTATION SETUP CHECKLIST:
# ✅ Create docs/ folder at project root
# ✅ Create changelog.md inside docs/
# ✅ Create project_structure.md inside docs/
# ✅ DOUBLE-CHECK: For EVERY task/request, double-check entire project structure
# ✅ ALWAYS READ: Read complete project_structure.md before any work
# ✅ COMPARE & UPDATE: Compare actual structure with documentation and update if needed
# ✅ Always review changelog.md and project_structure.md for every task/request
# ✅ Update changelog after every code change
# ✅ Update project structure when architecture changes
# ✅ VERIFY SYNC: Ensure documentation matches actual project layout before proceeding
# 🚫 NEVER include "## 🔍 Recent Implementations" or "last updates/implementations" in project_structure.md
# 🚫 Project structure docs = CURRENT ARCHITECTURE ONLY, Changelog = HISTORICAL CHANGES ONLY
##################################################################

## File Length and Structure – **🔥 CRITICAL: FILE SIZE CONTROL**
- Never allow a file to exceed 500 lines under any circumstances.
- If a file approaches 400 lines, **BREAK IT UP IMMEDIATELY** - this is non-negotiable.
- Treat 1000 lines as **COMPLETELY UNACCEPTABLE** even temporarily - refactor immediately.
- **MANDATORY ORGANIZATION**: Use folders and naming conventions to keep small files logically grouped - no exceptions.
- **DISCIPLINE REQUIRED**: Large files are technical debt - maintain them small or face the consequences.
- **ROBUST ENFORCEMENT**: Strictly monitor and enforce file size limits to ensure maintainability and readability.

## Object-Oriented Design – **🏗️ FOUNDATIONAL: OBJECT-ORIENTED DESIGN**
- Every functionality **MUST** be in a dedicated class, struct, or protocol, even if it's small - no shortcuts allowed.
- **PRIORITY: COMPOSITION OVER INHERITANCE** - Always favor composition over inheritance, but maintain object-oriented thinking religiously.
- **REUSABILITY MANDATE**: Code must be built for reuse from day one, not just to "make it work" - this is essential.
- **ARCHITECTURAL INTEGRITY**: Every component must follow OOP principles - this foundation cannot be compromised.
- **ROBUST ENFORCEMENT**: Ensure all code adheres strictly to OOP principles for scalability and maintainability.

## Single Responsibility Principle – **🎯 NON-NEGOTIABLE: SINGLE RESPONSIBILITY**
- Every file, class, and function **MUST** do one thing only - enforce this relentlessly.
- If anything has multiple responsibilities, **SPLIT IT IMMEDIATELY** - no compromises on this principle.
- **LASER FOCUS REQUIRED**: Each view, manager, or utility **MUST** be laser-focused on one concern - maintain discipline.
- **CLARITY ENFORCEMENT**: Multiple responsibilities create confusion and bugs - eliminate them without mercy.
- **ROBUST ENFORCEMENT**: Actively identify and resolve violations to maintain clean, focused code.

## Modular Design – **🧩 ESSENTIAL: MODULAR ARCHITECTURE**
- Code **MUST** connect like Lego — interchangeable, testable, and isolated - no tight coupling allowed.
- **REUSABILITY TEST**: Ask constantly: "Can I reuse this class in a different screen or project?" If not, **REFACTOR IT NOW**.
- **DEPENDENCY INJECTION MANDATE**: Reduce tight coupling between components using dependency injection or protocols - this is critical.
- **TESTABILITY REQUIREMENT**: Every component must be independently testable - design for isolation from the start.
- **ROBUST ENFORCEMENT**: Design with modularity as a core requirement to enable flexibility and testing.

## Manager and Coordinator Patterns – **📋 MANDATORY: ARCHITECTURAL PATTERNS**
- **ALWAYS** use ViewModel, Manager, and Coordinator naming conventions for logic separation - no exceptions.
- **UI LOGIC → ViewModel** - This separation is sacred and must be maintained religiously.
- **BUSINESS LOGIC → Manager** - Keep business rules isolated and pure - never mix concerns.
- **NAVIGATION/STATE FLOW → Coordinator** - Handle navigation and state transitions properly - this pattern is essential.
- **SEPARATION DOGMA**: Never mix views and business logic directly under any circumstances - this violation is unacceptable.
- **ROBUST ENFORCEMENT**: Strictly enforce these patterns to ensure clean architecture and maintainability.

## Function and Class Size – **📏 SIZE DISCIPLINE: CODE LIMITS**
- Keep functions under 30–40 lines **AT ALL TIMES** - longer functions are forbidden.
- If a class exceeds 200 lines, **ASSESS SPLITTING** into smaller helper classes immediately - no delays.
- **COGNITIVE LOAD CONTROL**: Smaller functions and classes are easier to understand and maintain - enforce these limits strictly.
- **MAINTAINABILITY MANDATE**: Large functions and classes create maintenance nightmares - keep them small religiously.
- **ROBUST ENFORCEMENT**: Regularly audit and refactor to adhere to size constraints.

## Naming and Readability – **🔤 CLARITY REQUIREMENT: DESCRIPTIVE NAMES**
- All class, method, and variable names **MUST** be descriptive and intention-revealing - vagueness is unacceptable.
- **FORBIDDEN TERMS**: Avoid vague names like data, info, helper, or temp **UNDER ANY CIRCUMSTANCES** - use meaningful names.
- **SELF-DOCUMENTING CODE**: Names should reveal intent clearly - if you need comments to explain a name, the name is wrong.
- **PROFESSIONAL STANDARDS**: Clear naming is non-negotiable - it affects code quality, maintainability, and team collaboration.
- **ROBUST ENFORCEMENT**: Ensure all names are clear and purposeful to enhance code readability.

## Scalability Mindset – **🚀 SCALABILITY IMPERATIVE: FUTURE-PROOF DESIGN**
- Always code as if someone else will scale this to massive proportions - design for growth from day one.
- **EXTENSION POINTS MANDATORY**: Include extension points (e.g., protocol conformance, dependency injection) from the very beginning - this is essential.
- **GROWTH PREPARATION**: Assume your code will need to handle 10x, 100x, or 1000x more load - architect accordingly.
- **MAINTAINER CONSIDERATION**: Future developers will thank you for scalable architecture - or curse you if it's not.
- **ROBUST ENFORCEMENT**: Build with scalability in mind to prevent future refactoring crises.

## Avoid God Classes – **🚫 FORBIDDEN: GOD CLASSES**
- Never let one file or class hold everything (e.g., massive ViewController, ViewModel, or Service) - this is architectural sin.
- **IMMEDIATE ACTION REQUIRED**: Split god classes into UI, State, Handlers, Networking, etc. **WITHOUT DELAY** - no compromises.
- **CONCERN SEPARATION**: Every class must have a single, clear purpose - enforce this boundary religiously.
- **MAINTAINABILITY PROTECTION**: God classes create maintenance nightmares - eliminate them as a priority.
- **ROBUST ENFORCEMENT**: Proactively identify and dismantle god classes to maintain code health.

## MCP Server Utilization – **🔧 MANDATORY: MCP TOOL UTILIZATION**
- **ALWAYS** utilize available MCP (Model Context Protocol) servers and tools to enhance development capabilities - this is non-optional.
- **UP-TO-DATE KNOWLEDGE**: Use MCP servers for retrieving current documentation, code examples, and implementation details - never rely on outdated information.
- **SPECIALIZED DOMAINS**: Leverage MCP tools for AI, machine learning, computer vision, and other specialized areas to get current best practices - this is essential for quality.
- **CONTEXT MAINTENANCE**: Apply MCP servers for project context, knowledge persistence, and collaboration tracking across sessions - maintain continuity.
- **SMART SELECTION**: Choose the most appropriate MCP server based on task requirements rather than using generic approaches - precision matters.
- **MAXIMIZE EFFICIENCY**: Use available MCP tools to accelerate development, ensure accuracy, and maintain comprehensive documentation - no shortcuts allowed.
- **ROBUST ENFORCEMENT**: Integrate MCP tools into every relevant task for enhanced capabilities.

## Cipher MCP Setup – **🧠 MANDATORY: ADVANCED MEMORY LAYER**
- **ALWAYS** configure Cipher MCP server for persistent memory and knowledge graphs - this is essential for projects exceeding 200k context limits.
- **GEMINI API INTEGRATION**: Use Gemini API as primary LLM provider for Cipher to leverage Google's advanced models:
  - Set `GEMINI_API_KEY` environment variable with your Google AI API key
  - Provider: `gemini` in Cipher configuration
  - Benefits: Advanced reasoning, multimodal capabilities, cost-effective for memory operations
- **VECTOR STORE CONFIGURATION**: Use `in-memory` vector store for local development or configure Qdrant/Milvus for production scalability.
- **MEMORY OPERATIONS**: Leverage Cipher's built-in tools (`cipher_memory_search`, `cipher_add_node`, `cipher_search_graph`) for all knowledge persistence tasks.
- **CONTEXT OFFLOADING**: Store project history, component relationships, and decisions in Cipher to free up context window for active coding.
- **WORKSPACE MEMORY**: Enable team collaboration features for multi-developer environments.
- **ROBUST ENFORCEMENT**: For any task requiring multi-session context or complex refactoring, initialize Cipher memory layer first.

## Responsive Design – **📱 UNIVERSAL: RESPONSIVE DESIGN MANDATE**
- Design and implement applications that work seamlessly across ALL device resolutions - from mobile phones to large desktop displays.
- **PRINCIPLES ENFORCEMENT**: Use responsive design principles with flexible layouts, scalable typography, and adaptive components - no fixed dimensions allowed.
- **TESTING REQUIREMENT**: Test applications on multiple devices and screen resolutions to ensure consistent experience - this is mandatory quality control.
- **MOBILE-FIRST APPROACH**: Implement mobile-first design where applicable, ensuring touch-friendly interfaces and optimal performance on smaller screens.
- **INPUT CONSIDERATIONS**: Consider different input methods (touch, mouse, keyboard) and interaction patterns for various devices - universal accessibility required.
- **CONSISTENCY MAINTENANCE**: Maintain design consistency and usability standards across all platforms while optimizing for each device's unique characteristics.
- **ROBUST ENFORCEMENT**: Ensure responsive design is a core requirement for all applications.

## Design Consistency – **🎨 SACRED: DESIGN SYSTEM ADHERENCE**
- **ALWAYS** adhere to the project's established design system, component library, and architectural patterns - no deviations without approval.
- **COMPONENT REUSE MANDATE**: Use existing UI components, design tokens, and styling conventions rather than creating new ones - reuse is essential.
- **VISUAL CONSISTENCY**: Follow documented design principles and maintain visual consistency across all screens and features - this is non-negotiable.
- **DOCUMENTATION REQUIREMENT**: Document any new components or design patterns in project structure documentation for team reference - maintain records.
- **SEAMLESS INTEGRATION**: Ensure all new features integrate seamlessly with existing design language and user experience patterns - no fragmentation allowed.
- **GUIDELINE ENFORCEMENT**: Avoid design fragmentation by consistently applying established visual and interaction guidelines - maintain system integrity.
- **ROBUST ENFORCEMENT**: Strictly enforce design consistency to preserve system integrity.

## Respectful Development – **🤝 ESSENTIAL: RESPECTFUL DEVELOPMENT PRACTICES**
- **ALWAYS** review the `docs/changelog.md` and `docs/project_structure.md` files before making code changes - understand the project first.
- **THOUGHTFUL MODIFICATIONS**: Make purposeful modifications that add genuine value rather than changing for the sake of changing - quality over activity.
- **DISCIPLINED REFACTORING**: Avoid unnecessary refactoring, renaming, or restructuring unless it provides clear maintainability or functionality benefits.
- **TEAM IMPACT CONSIDERATION**: Consider the impact of changes on other team members and project stability before implementation - collaborative thinking required.
- **QUALITY PRIORITY**: Focus on quality over quantity - a few well-considered improvements are infinitely better than numerous superficial changes.
- **CODEBASE RESPECT**: Respect existing codebase and design decisions unless there's a compelling reason to deviate - honor previous work and decisions.
- **ROBUST ENFORCEMENT**: Approach every task with respect for existing work and thorough review of documentation.

---

## 🚨 **COMPREHENSIVE RULE REMINDER - NON-NEGOTIABLE** 🚨

**📋 BEFORE ANY TASK/REQUEST - MANDATORY CHECKLIST:**
- ✅ **ALWAYS** DOUBLE-CHECK entire project structure by listing directories and examining file organization
- ✅ **ALWAYS** READ complete `docs/project_structure.md` to understand current documented architecture
- ✅ **ALWAYS** COMPARE actual project structure with documentation and UPDATE if discrepancies found
- ✅ **ALWAYS** review `docs/changelog.md` and `docs/project_structure.md` FIRST
- ✅ **ALWAYS** ensure `docs/` folder exists with both documentation files
- ✅ **ALWAYS** use descriptive, meaningful names (no vague terms like "data", "info", "helper")
- ✅ **ALWAYS** follow OOP principles with single responsibility and composition over inheritance
- ✅ **ALWAYS** implement modular, testable, and reusable code design
- ✅ **ALWAYS** use ViewModel/Manager/Coordinator patterns for logic separation
- ✅ **ALWAYS** keep functions ≤30-40 lines and classes ≤200 lines
- ✅ **ALWAYS** build with scalability and extension points in mind
- ✅ **ALWAYS** eliminate god classes immediately upon detection
- ✅ **ALWAYS** utilize MCP tools for current knowledge and efficiency
- ✅ **ALWAYS** implement responsive design for all devices
- ✅ **ALWAYS** adhere to established design systems and consistency
- ✅ **ALWAYS** prioritize quality over quantity and respect existing work
- ✅ **ALWAYS** update documentation after every change - NO EXCEPTIONS

**🔥 CORE PRINCIPLES - NEVER COMPROMISE:**
- **Documentation is sacred** - Treat it as important as code itself
- **Single responsibility** - Every component must have one clear purpose
- **Modularity first** - Code must be interchangeable, testable, and isolated
- **Size discipline** - Small files, functions, and classes only
- **Naming clarity** - Names must reveal intent without comments
- **Scalability mindset** - Design for 10x-1000x growth from day one
- **Robust enforcement** - Actively monitor and resolve violations immediately
- **Respectful development** - Honor existing work and consider team impact

**⚠️ FINAL WARNING:** These rules are not suggestions - they are mandatory requirements for professional, maintainable, and scalable code. Violating any rule creates technical debt and maintenance nightmares. Adhere to ALL rules RELIGIOUSLY for every task, every request, and every code change. No shortcuts allowed - quality and discipline above all!

