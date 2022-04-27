# Documentation for GitHub Pages

This repository contains the bloXmove Confluence documentation exported as HTML files, and converted to Markdown. The list of Confluence pages that have been exported is [here](#documentation-contents). For more files, see tag v1.01.

## Source files

### Documentation in .md format:
[.md files](./Markdown)

Per Marvin Kassuehlke, Markdown rendered by GitHub Pages is the preferred format.
### Documentation in HTML format:
[HTML files](./HTML)

**Note:** For the iOS SDK, as neither the [exported HTML](./HTML/iOS%20Identity%20SDK/) nor generated [.md files](./Markdown/iOS%20Identity%20SDK/) look good, the **[original HTML documentation](./HTML/Identity%20SDK%20Documentation/)** has been packaged as well for possible inclusion. It is advisable to use this one.

### Documentation in PDF format:

[Identity iOS SDK Manual](./Identity%20SDK%20methods%20in%20the%20Mobility%20Blockchain%20Platform%20UI%20app%20Rental%20Flow.pdf)

## Demo

A demonstration of what the documentation on the GitHub page would look like can be seen here:

https://bloxmove-com.github.io/demo/

[Source files](https://github.com/bloxmove-com/demo)

Note that this has to be a public repository.

## Deployment

Copy the appropriate directories (HTML, Markdown) to either an appropriate repository for housing the public documentation and for which GitHub Pages is enabled (for example bloxmove-com.github.io/documentation, which would be hosted in https://github.com/bloxmove-com/documentation), or possibly to the root [bloxmove-com](https://github.com/bloxmove-com/bloxmove-com.github.io) GitHub page repo (confirm with Product Owner). 

If using Markdown, make sure the [\_config.yml](https://github.com/bloxmove-com/demo/blob/main/_config.yml) has the proper includes pointing to the markdown files to render.

Note that the repository hosting a GitHub Page must be public so anyone can access anything uploaded there. There is no way to "preview" the results privately without signing up for Enterprise services.

## ToDos

### General

1. Create an index/splash page w/ Table of Contents (see the Component ToC and Technical Doc ToC as a guide)
1. Create links back to the proper index page
1. Review what parts of the [Confluence documentation](https://bloxmove.atlassian.net/wiki/spaces/DLT/overview?homepageId=1395261034) to make public \[partly done with Marvin & Mark\]
1. Curate files and make sure nothing sensitive is uploaded \[to be done by Harry\]
1. Remove "Atlassian" footer?
1. Remove dates and authors? 
1. Make figures clickable links
1. Remove "attachments" list?

### Markdown
1. Fix navbar header so it displays properly and doesn't appear as a list
1. Clean up useless HTML left from the conversion process

### HTML
1. Use [original iOS Identity SDK HTML documentation](./HTML/Identity%20SDK%20Documentation/) 

# Documentation Contents

* Fleet Node
* Architecture Overview
* Rental Flow - Ethereum Implementation
* \(iOS Identity SDK\)
* iOS Identity SDK Manual
