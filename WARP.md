# WARP.md

This file provides guidance to WARP (warp.dev) when working with code in this repository.

## Newsletter Template Module Overview

This directory (`pub-template`) is a Git submodule containing templates and configuration for the newsletter component of the Carnival of Calamity content management system. It provides the foundation for creating newsletter publications across the various Carnival of Calamity content streams.

## Architecture & Structure

### Key Files
- `pub-template.md`: The main template file containing:
  - Content structure guidelines
  - Style definitions (palettes and fonts)
  - Status indicator definitions
  - Workflow documentation

### Style Elements
- **Primary Palette**: `#8230ff, #e3d0ff, #ff3046`
- **Fonts**:
  - Primary: Requiem
  - Secondary: Avenir

## Publishing Workflow

### Status Progression
1. **backlog**: Planned titles not in active development
2. **active**: Titles in development with beehiiv draft created
3. **processing**: (Editions only) All articles completed and ready for assembly
4. **ready**: All tasks completed, scheduled for publishing
5. **published**: Live content

### Content Hierarchy
```
Volume > Edition > Article > Element
```

- **Volume**: Collection of editions organized around serial publications
- **Edition**: Collection of articles plus newsletter issue
- **Article**: Individual content pieces (web posts)
- **Element**: Components within articles (images, headlines, content)

### Publication Process
1. Create article cards in Obsidian with text and header
2. Create draft in beehiiv with content elements and title card
3. Copy draft link to article metadata
4. Set status and track TODOs
5. Update status as work progresses

## Integration with Parent Project

This module is integrated into the main Carnival of Calamity project as a Git submodule at:
```
[submodule "newsletterTemplate"]
	path = pub-template
	url = git@github.com:madalexxx/newsletterModule.git
```

## Common Commands

### Git Submodule Management
```bash
# Update this submodule to the latest commit
git submodule update --remote pub-template

# Add changes to the submodule
cd pub-template
git add .
git commit -m "Update newsletter template"
git push

# From parent repository, update reference to submodule
cd ..
git add pub-template
git commit -m "Update newsletter template submodule"
git push
```

### Template Usage
This template module is used by the Templater plugin in Obsidian. Common Templater scripts that interact with these templates:

```javascript
// Create a new article based on template
await tp.file.create_new(
    tp.file.find_tfile('templates/dashboard-article'),
    articleFileName,
    true,
    editionPath
);

// Create a new edition based on template
await tp.file.create_new(
    tp.file.find_tfile('templates/dashboard-edition'),
    publicationEditionTitle,
    true,
    publicationEditionFolderPath
);
```

## External Service Integration

This module is designed to work with:
- **beehiiv**: Primary newsletter platform for content publishing
  - Draft links are stored in frontmatter
  - Publication requires creation of beehiiv drafts

## 🤖 Agent Protocol & Usage Boundaries

**CRITICAL**: Digital assistants are authorized for **administrative, documentation, and version control tasks ONLY**. 

### 🚫 **STRICTLY PROHIBITED**
- **Story writing assistance**: No creative content generation, plot development, character creation, or narrative assistance
- **Editorial content creation**: No writing of articles, posts, or publication content
- **Creative decision making**: No artistic or creative direction
- **Content generation**: No creation of fictional narratives, characters, or story elements

### ✅ **AUTHORIZED USAGE**
- **Documentation**: Technical documentation, WARP.md updates, README files, architectural guides
- **Administration**: File organization, workflow setup, system configuration  
- **Version Control**: Git operations, branch management, commit message formatting, PR creation
- **Code Development**: Plugin development, automation scripts, build tools, testing frameworks
- **Project Management**: Task tracking, progress documentation, workflow optimization
- **System Integration**: API connections, tool configurations, deployment procedures

### 📋 **End-of-Session Documentation Protocol**

**MANDATORY**: All agent sessions MUST conclude with proper documentation following established templates.

#### Pre-Commit Documentation Workflow
1. **Check for Templates**: Always verify and use existing templates in `.warp/` and `ARCHIVE/` directories
2. **CHANGELOG Creation**: 
   - Use `ARCHIVE/CHANGELOG-template.md` EXACTLY as provided
   - Fill in `commit-sha` field after commit
   - Check `digital-assistant-prominent` if agent was primary contributor
   - Follow established frontmatter format precisely
3. **Conversation Summary**:
   - Create session summary in `.warp/` directory
   - Document conversation flow, decisions made, and protocol adherence
   - Include agent contribution level and scope of work
4. **Template Adherence**: 
   - NEVER create custom formats when templates exist
   - Respect established workflow patterns
   - Follow carnival-specific terminology and structure

#### Git Workflow Integration
```bash
# Standard end-of-session sequence:
1. Create CHANGELOG using existing template
2. Create conversation summary in .warp/
3. Add commit SHA to changelog after commit
4. Follow established branch/PR workflow
```

### 🎪 Carnival-Specific Guidelines

#### Documentation Voice
- Use theatrical carnival terminology where established
- Maintain "systematic precision meets supernatural storytelling" tone for technical docs
- Respect existing voice patterns in carnival documentation

#### Template Priority
- Project templates take precedence over global patterns
- Use `.warp/` directory templates for conversation documentation  
- Use `ARCHIVE/` directory templates for changelog documentation
- NEVER improvise formats when templates exist

#### Protocol Violations
- **Template Bypass**: Creating custom formats instead of using provided templates
- **Unauthorized Content**: Any creative writing or story assistance
- **Workflow Deviation**: Skipping established documentation procedures
- **Context Ignorance**: Not reviewing existing protocols before proceeding

### 🔍 Template Verification Process

Before creating ANY documentation:
1. **Check `.warp/` directory** for conversation templates
2. **Check `ARCHIVE/` directory** for changelog templates  
3. **Review existing WARP.md** for project-specific requirements
4. **Confirm template usage** rather than creating custom formats

### 💻 Technical Documentation Standards

#### Code Documentation
- Full inline documentation for complex functions
- README updates for new features or workflow changes
- Architecture documentation for system-level changes
- API documentation for integration points

#### Workflow Documentation
- Step-by-step procedures for complex operations
- Troubleshooting guides for known issues
- Integration guides for external systems
- Deployment and configuration procedures

---

**Remember**: The carnival's systematic precision depends on protocol adherence. Every deviation from established workflows undermines the operational excellence that defines our distributed empire.