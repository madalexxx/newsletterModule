---
class: project
---

# todo

# contents
[[#guidelines]] 
	[[#terms]] 
	[[#workflow]] 
	[[#status indicators]] 
[[#style guide]] 
	[[#palettes]] 
		[[#primary]] 
		[[#brown tetradic]] 
		[[#tan tetradic]] 
		[[#green tetradic]] 
		[[#dark blue tetradic]] 
	[[#fonts]] 
# guidelines
## terms

> [!info]- article
> An article is a section of an edition. For example, a single web-post for a Classic Tale of Horror is an element.

> [!info]- element
> An element consists of an article's image, headline, and content.

> [!info]- edition
> An edition is a collection of articles, including their corresponding newsletter issue.

> [!info]- issue
> An issue is the newsletter copy to be delivered to subscribers. It contains a summary of the entire edition, as well as a chapter of the ongoing serial, for ease of consumption. Issues are denoted by a "Number" following the volume designation.

> [!info]- volume
> A volume is collection of editions. Volumes are established around the serials they ship, thus a new volume begins when a new serial begins.

> [!info]- title
> A title refers to any edition, article, or issue in planning or development. If it exists as an independent draft or post on beehiiv, it is considered a title generally. This term is specifically established for ease of referral in project notes.

A *volume* comprises a collection of editions; *editions* comprise a collection of articles and issues; *issues* comprise a collection of elements.
## workflow
*Elements* are listed out as tasks to be fulfilled in article cards. Article cards are linked to in edition cards. From top to bottom, the hierarchy is:
	Volume > Edition > Article > Element

Content is produced from bottom to top as follows:
1. create the article card under the respective folder here in Obsidian. add the text and the header. 
2. create a draft in beehiiv, insert the main content elements, and upload the title card element. no draft may be saved for later until both the main content and title card elements are in place, at the very minimum. Having these staged in the article card is ideal
3. copy the draft link from beehiiv and add it to the respective article card's metadata
4. set the status. see [[#status indicators]] for details
5. note any TODOs
6. when all TODOs are complete, change the status in accordance with the [[#status indicators]].
## status indicators

> [!info]- backlog
> The title is planned.
> - Editions: one or more articles may have been created/started, but the edition as a whole is not in active development.
> - Articles: titles, headers, and tentative publish dates may be input, but the article as a whole is not in active development. 
> - PDFs: if a title has been created and set to backlog, the `pdf-status` should be set to `backlog` as well, whether or not a document has been created.
> When the title is in active development, change status to `active`.

> [!info]- active
> This indicates the title is in active development and a beehiiv draft has been created. It may or may not yet be scheduled, and is not yet ready for publishing. Once the title is scheduled and ready for publishing, change to `ready`.

> [!info]- processing
> **For Editions Only**
> This indicates all articles are completed and in `ready` status, all tasks are completed, and the issue is ready for assembly. As completion of the issue is dependent upon the articles of the edition being published, this status helps differentiate between an article's readiness and an edition's perceived completion.

> [!info]- ready
> This indicates all tasks for a given title have been completed, and the title is scheduled and ready for publishing. When the title is published, change the status to `published`.

> [!info]- published
> This indicates the title has been published.

For articles, the status progression is as follows:
	backlog > active > ready > published

For editions, the status progression is as follows:
	backlog > active > processing > ready > published
# style guide
## palettes
### primary
```palette
#8230ff, #e3d0ff, #ff3046
```

```palette
#8230ff, #e3d0ff, #ff3046
{ "gradient": true }
```

## fonts
Primary: Requiem
Secondary: Avenir
Accent: 