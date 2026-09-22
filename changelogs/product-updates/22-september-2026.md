---
title: '22 September 2026'
date: '2026-09-22'
published: true
---

- {% badge text="New" type="success" /%} **WebMCP**: Your docs pages now offer tools to AI agents running in your readers' browsers, so an agent can search your docs, read a page and open one for the reader.
- {% badge text="Improvement" type="info" /%} **API References**: [llms.txt](/support-center/llms-txt) now lists every endpoint of each API reference, and an AI assistant can read a single endpoint instead of the whole definition.
- {% badge text="Bug Fix" type="error" /%} **Feedback**: Opening a page's [feedback](/support-center/feedback) in the editor no longer gets stuck on some pages.
- {% badge text="Bug Fix" type="error" /%} **Reader**: A list that carries on past a [synced block](/support-center/synced-blocks) or [conditional block](/support-center/conditional-blocks) now stays one list, and a numbered list keeps counting.
- {% badge text="Change" type="warning" /%} **Reader**: We turned off font antialiasing on your docs, so text draws at its intended weight on Mac instead of looking thin. To turn it back on, add this to your [Custom CSS](/support-center/custom-css):

```css
body {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
```
