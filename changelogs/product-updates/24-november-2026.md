---
title: '24 November 2026'
date: '2026-11-24'
published: true
---

- {% badge text="New" type="success" /%} **Pages**: Bring back a page deleted in the last 30 days from **Deleted pages** in the sidebar's **New** menu. See [restoring a deleted page](/support-center/managing-pages#restoring-a-deleted-page). Your AI client can do the same through the [Editor MCP Server](/support-center/editor-mcp-server).
- {% badge text="Improvement" type="info" /%} **Top Navigation**: New documentation sections and API references no longer join your first navigation group. They show as their own tab in the [top navigation](/support-center/top-navigation-bar) until you assign them one.
- {% badge text="Improvement" type="info" /%} **Editor MCP Server**: When creating, editing or publishing a page is refused, your AI client now sees why, such as a slug that is taken or a locked version, so it can fix the request or tell you. See the [Editor MCP Server](/support-center/editor-mcp-server).
- {% badge text="Bug Fix" type="error" /%} **Editor**: **Publish drafts** in a [documentation section's settings](/support-center/managing-documentation) now publishes every draft, and the [dashboard](/support-center/dashboard)'s Draft pages list shows exactly the pages with unpublished changes.
- {% badge text="Bug Fix" type="error" /%} **Editor**: The **New** menu at the bottom of the sidebar now opens below its row, with every item on screen.
- {% badge text="Bug Fix" type="error" /%} **Pages**: Two new pages with the same title in a section no longer share one address. The second gets a numbered slug, such as `overview-2`.
- {% badge text="Bug Fix" type="error" /%} **AI Agent**: **Save and publish** in the [AI Agent](/support-center/ai-agent) now publishes an API reference's new definition, and shows a hidden changelog post.
- {% badge text="Bug Fix" type="error" /%} **Slack**: Pages and API references that the [AI Agent](/support-center/ai-agent) or the API creates, edits or publishes now post to [Slack](/support-center/slack), naming "via AI agent" or the API key.
- {% badge text="Bug Fix" type="error" /%} **Translation**: Renaming a page now updates the links to it in your [translated pages](/support-center/localisation) as well.
- {% badge text="Bug Fix" type="error" /%} **Versions**: [Importing](/support-center/importing-documentation) a ZIP whose version your project already has, such as v1.0, now adds it as "v1.0 (2)" rather than a second version at the same address. Saving a [version's](/support-center/managing-versions) settings also no longer changes its address.
- {% badge text="Bug Fix" type="error" /%} **GitHub Sync**: Renaming a version now moves its API reference files to the version's new folder in your [synced repository](/support-center/github-sync).
