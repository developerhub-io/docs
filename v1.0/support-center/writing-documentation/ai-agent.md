---
type: page
title: AI Agent
listed: true
description: 
index_title: AI Agent
hidden: false
keywords: 
tags: ai
---

AI Agent turns a conversation into proposed edits across your documentation. Ask for a change and it reads your content, works out everything the change touches, and stages the edits for you to review.

A single request can change many pages at once. It also works on API references and [changelog](/support-center/changelogs) posts, not just pages.

Nothing AI Agent does is written to your documentation on its own. Every change is staged, you review it line by line, and nothing reaches your readers until you save it.

{% image url="../../../assets/ai-agent-window.png" %}
The conversation, the staged changes, and the change under review
{% /image %}

## Who can use AI Agent

AI Agent needs a plan that includes AI features, and an admin has to switch it on:

- Open Project Settings → **AI** → **AI Features**.
- On the **Agent** tab, under **Writing**, turn on **AI writing agent**.
- Click **Save changes** in the top menu.

Writers and above can then use it. Saving and publishing in one step, deleting anything, and changing a page's sidebar icon all need the publisher role, so a writer may be able to edit something they cannot remove.

## Opening AI Agent

Select **AI Agent** {% icon classes="fas fa-robot" /%} in the editor's top bar. It opens as a near full-screen window headed **AI Editor**, with the conversation on the left and the review panes on the right.

Closing the window does not stop a run. The agent carries on working while you go and look at the pages it is changing, and the top bar button keeps pulsing until it finishes.

## Asking for a change

The agent works across the documentation version you are in, including drafts and unpublished pages. Some examples of what to ask for:

- Rename the `legacy_token` parameter to `api_token` everywhere it appears.
- Add a "Rate limits" section to every endpoint page that does not have one.
- Write a changelog post covering what changed in v3.
- Find the reader searches that returned nothing, and fix the pages that should have answered.
- Fix all the broken links on this page.

### Pointing at something with @

Type `@` in the message box to point the agent at something specific. You can pick:

- **this page**: the page open behind the window.
- Any page in the version.
- An API reference.
- A file from a [code repository](/support-center/self-updating-docs), if one is attached.

Deleting the label from your message removes the mention again.

### What the agent can read

Beyond your pages, AI Agent can look at [search analytics](/support-center/search-analytics) to find the terms readers searched for and found nothing for, check every link in a version at once, and list the pages that link to a page before it changes it.

## Reviewing what it staged

Proposed changes collect in the **Changes** list, grouped under **Documentation**, **API references** and **Changelog**. Each row shows what it would add and remove.

You have two levels of control:

- **A whole change**: the tick box decides whether a change is included in the next save. Untick anything you do not want. Selecting **Drop this change** removes it from the list entirely.
- **Part of a change**: open a change to see it line by line, then use **Accept** or **Reject** on each edited section. A rejected section is marked **Won't be saved**, and the rest of the change still applies.

Rows can carry a tag that explains their state:

| Tag | What it means |
|---|---|
| Saved | Already written to the page as a draft. |
| Live | Already published. |
| Blocked | Cannot be saved as it stands. Ask the agent to redo it. |
| Changed since | The page changed after the agent read it, so the proposal no longer fits. Ask the agent to look at that page again, or drop the change. |
| Not saved | The save was attempted and did not succeed. |

When you are happy, use the bar at the bottom:

- **Save to draft** puts the selected changes into [draft mode](/support-center/draft-mode), where you can edit further before publishing.
- **Save and publish** writes and publishes them in one step. This needs the publisher role.
- **Discard all** throws the staged changes away.

Saving does not end the conversation. Saved changes stay in the list, and you can keep asking for more.

{% callout type="warning" title="Some changes have no draft" %}
Deletions and page settings changes (a page's address, title, sidebar icon or position) are not drafted. They take effect the moment you save, with either button.

Links to a renamed page from inside your documentation are repointed for you, but links from anywhere else, such as bookmarks, emails and search results, will stop working. A deletion cannot be undone.

Changelog posts have no draft either: **Save and publish** makes a post public immediately, and **Save to draft** leaves it unpublished for someone to release later.
{% /callout %}

## Conversations

Each conversation keeps its own thread and its own staged changes.

- Select {% icon classes="fas fa-plus" /%} to start a **new conversation**. The current one is closed, not deleted.
- Select {% icon classes="fas fa-clock-rotate-left" /%} to reopen an earlier conversation. Opening one keeps the other, and nothing staged is lost either way.

The same list has a **Pull requests** section, holding the runs that started from a pull request on an attached [code repository](/support-center/self-updating-docs). You can read those and reply to them, but they stay with the pull request rather than becoming one of your own conversations.

## Keeping a conversation sharp

A dial at the top of the conversation shows how full it is as a percentage. Past 75% the agent suggests starting a new conversation, and past 90% it asks you to confirm before sending. Starting a new conversation never loses what is already staged.

The **Context** button next to the message box shows which version the agent is editing and which code repositories it is reading, and warns you when an attached repository cannot be read or has not been read for a while.

## Choosing the model

Admins can pick the model every agent run in the project uses, including the pull request checks under Self-Updating Docs. Open Project Settings → **AI** → **AI Features** → **Agent** tab, and use **Agent model** in the **Model** card.

Each model is rated out of three for **Cost**, **Speed** and **Judgement**, and shows the provider that serves it and the region it runs in, so you can rule out a jurisdiction if you need to. **Auto** follows our current recommendation and moves with it.

## What AI Agent cannot do

- It cannot create an API reference. That means [uploading a definition](/support-center/uploading-references) yourself.
- It cannot delete a page that has pages nested under it, the only page left in a documentation section, or the last section in a version.
- It cannot move a page to a different documentation section, or rename and reorder the sections themselves.
- It cannot clear a page completely. Emptying a page is not the same as deleting it, so the agent refuses and points you at deleting it properly instead.
- It cannot generate images.
- It cannot change your code. Attached repositories are read only.

If a request needs one of these, the agent says so and does the part it can rather than approximating the rest.

## AI Agent and AI Writer

[AI Writer](/support-center/ai-writer) works inline on text you have highlighted and applies its changes straight away. AI Agent works from a conversation, can change many pages, API references and changelog posts at once, and stages everything for review first.

## Activity log

Applying changes is recorded in the [activity log](/support-center/activity-log) as **published AI changes** or **saved AI changes as drafts**, once per save rather than once per page. Changing the agent model is logged too.

## What data is sent

The pages, API references and changelog posts the agent reads and edits are sent to the model you have chosen, along with your conversation.

Agent runs are served through OpenRouter, and only providers with zero data retention are used. Your content is never kept and never used to train a model. See [AI Features](/support-center/ai-features) for how this differs from our other AI features.
