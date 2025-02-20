---
title: BrainTool Philosophy
tagline: The Topic Manager for your Online Life
description: BrainTool is a way of organizing things you want to remember and get back to, using notes and nested tags. Its also a better way to control your browser.
---

# BrainTool Vision
While working on your computer you should be able to easily capture and categorize, all the information and knowledge you want to keep track of; right at the point you discover it or create it. Then you should be able to access that information and knowledge later if you need to refer to it or if you want to edit it as part of your personal information space.

Information discovery these days generally takes place in a browser tab, creation is either also in a tab or as some kind of note or task list or idea, written in text. BrainTool unifies these two information spaces - it makes it easy to organize all of your browseable information resources into a set of related 'Topics' and to capture free-form notes on those topics within your personal organizational system.

The long term vision for BrainTool is to be the tool your brain needs to keep track of all of your information. It will expand to offer a beautiful and satisfying in-place note taking and curation environment, full content search, productivity tools, and content sharing with the exchange of curated informational Topic Maps.

# Overview
The BrainTool browser extension is a knowledge/notes/links/browser manager. While browsing you assign a Topic to web pages you want to save and optionally add a note. Topics, links and associated notes are stored in your personal braintool file. 

Topics provide a way of organizing your information. Think of BrainTool as the index into your personal information space. Each topic is represented by a node in the tree shown on the BrainTool side-panel, and within Chrome by a dedicated window or tab group with tabs for saved links. 

The side-panel is your central controller. With drag and drop and powerful keyboard commands it allows you to organize and annotate your topic tree, and to operate your browser - opening, closing and navigating between tabs and windows with ease.

<br/>
<img src="/site/bt-screenshot1.png" style="border:solid; border-width:thin;">

By organizing links and capturing your notes about them you are mapping your personal information space. BrainTool stores that information space in a plain-text file. As you save pages, and add notes a file called BrainTool.org is kept updated. That file is regular text but structured in public [org-mode](http://orgmode.org) format. The text file can be edited in any text editor but ideally in emacs with org-mode.
<!--
<br/>
<br/><br/>
<img src="/site/bt-screenshot4.png" style="border:solid; width:50%; border-width:thin;">
-->
<br/><br/>
<img src="/site/ScreenShot.png" style="border:solid; border-width:thin;" alt="Screenshot showing BrainTool with emacs and Chrome views">
# Philosophy
The core BrainTool philosophy is that your data is stored in a human-readable plain text format and that you own and have complete control over its use. BrainTool endeavors to be a fantastic standalone tool but to work well within an emacs and org-mode text-based workflow and to readily integrate with an associated ecosystem of information management and productivity tools.

## Security
BrainTool is comprised of a Chrome extension and a JavaScript web application. The app is entirely a static source-available client-side app served from [a public software repository](https://github.com/tconfrey/BrainTool). Your data is stored in browser memory or optionally in a file called BrainTool.org on your Google Drive. In use the only communicating parties are your browser and the Google Drive server, no information is stored or accessible anywhere else. The app is as secure to use as Google's infrastructure. (See also the [official privacy policy.](./BrainToolPrivacyPolicy.pdf))

# <A href="#concepts">Concepts</A>
BrainTool (BT) is loosely based on the semantic web idea of [Topic Maps](https://ontopia.net/topicmaps/materials/tao.html) which define a 'TAO' of information: _Topics_ as an organizational unit, _Associations_ between topics, and _Occurrences_ of information about a topic. 

## Topics
Topics are the basic unit of organization. A project you are working on can be a topic. An area of responsibility can be a topic (eg Home Finances). As can a set of resources you want to keep track of (eg web sites related to programming Chrome Extensions). Every parent node in the BT side-panel tree is a topic.

## Associations
Associations are links capturing a relationship between topics. Currently in BT the only associations are containment relationships between a topic and its subtopics. In the longer term bidirectional links will capture other kinds of association.

## Occurrences
Occurrences of information about a topic are the things you save and capture into your braintool file. That includes all of your saved links as well as the notes associated with a link or topic.

# Roadmap
There will always be a fully functional, free and open source version of BrainTool with a continuously evolving and improving feature set. That said, after achieving a stable 1.0 release, efforts will be focused on adding premium features and scaling. The following is not intended to be complete or in priority order, [feedback is appreciated](https://groups.google.com/u/0/g/braintool-discussion).

Note that BrainTool is intended to help you actively curate an information space, it is not meant to passively observe or capture all of the random information that flows through your browser.

## Release 1.0
- **Search** : In 1.0 BrainTool search will be modeled on emacs forward and backward incremental text search across the full contents of your braintool file, perhaps with narrowing to rows containing the search term.

## Post 1.0
- **Preferences** : Factors such as font size and side panel location will be made configurable asap.
- **Browsers** : Firefox, Edge, Brave and Vivaldi will be supported.
- **Backups and Alternative Backends**: While the current app allows on-demand local file export and a continuously synced file on a Google Drive, it would be nice to support different back ends for continuous storage as well as regularly scheduled backup file creation.
- **Org Functions**: Org-mode itself provides a good roadmap for BrainTool's potential feature set. Org is a massively functional but highly complex personal organizational tool. BrainTool will provide an intuitive overlay for a subset of orgs most important functionality - TODO lists, journaling, agendas etc.
- **Session Save and Live Sessions**: While you can already save all the tabs in a window to a topic with a couple of clicks, there would be value in being able to save a snapshot of the whole browser session for later recovery. Relatedly, continuously capturing all activity in a browser window into a topic could be useful while researching.
- **In-Page Highlighting**: Some similar tools find value in allowing the user to capture text from within a saved page, this might make sense for BrainTool also.
- **Syncing Tree moves with Tab moves**: Currently if you drag and drop browser tabs the tree is not updated. Similarly operating on tree nodes does not move browser tabs. The two should remain in sync.
- **Notes Editor**: The current BT text editing capabilities are pretty basic. Given that its all just text, savvy users can use emacs or any other text editor. That said, it is a goal for BT to allow note-taking in place within the browser via some kind of simple but beautiful and highly satisfying editor tool.
- **Deep Search**: As noted above search across your braintool file will be part of 1.0. Longer term it will be possible to crawl the actual contents of all of your saved pages and to augment browser search with a search across your personal information space.
- **Tags and Bi-Directional Linking**: In addition to containment it should be possible to model other kinds of relationships between topics and to tag information occurrences as being relevant to multiple topics.
- **Multi-file Support**: It should be possible to save and load Topic Trees from a dedicated file. For example a node 'Recipes' could point to a dedicated recipes.org file which is loaded on demand.
- **Topic Tree Sharing**: Curated Topic Trees are a very good way of sharing knowledge. E.G. I could share my 'recipes' topic with a friend, my 'Kitchen Project' topic tree with my wife or a 'team links' topic with an employee as part of onboarding.
- **Topic Tree Repository**: Building on the above, BrainTool will host best-practice topic trees around common areas such as 'productivity tools', 'Knowledge Management' etc.
