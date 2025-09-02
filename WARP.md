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
