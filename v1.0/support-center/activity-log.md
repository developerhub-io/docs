---
type: page
title: Activity Log
listed: true
description: 
index_title: Activity Log
hidden: false
keywords: 
tags: 
---

We audit all actions on %product% made by your team. These include the creation, update and deletion of the following:

- Projects
- Versions
- Documentation
- Pages
- Indices (Categories, Links, ...)
- API References
- Imports
- Users / Teammates
- API Key
- Landing Page
- Custom Pages
- Glossary
- Comments
- Changelogs
- Template Pages

The activity log is scoped as such:

- Content
- Users
- Security
- Hosting
- Plan
- Other

Admins are able to see all all logged activity. Users with other roles would only see logged activity that are concerned with content.

On the dashboard, the last 100 logs will show.

## Across a Whole Organisation

If your projects are grouped under an [organisation](organisation-settings.md), the organisation owner can read the activity of every project the organisation owns in one place, with search, project and scope filters, and paging. See [Activity log](organisation-settings.md#activity-log).

### Enterprise Auditing

Enterprise users can query full audit log for any activity in the past 6 months using our [API](/v1.0/api/ref#get-audit-log). The audit log would show details of each change.

Example of how to query full audit log is as such:

{% code %}
```bash {% title="cURL" %}
curl --request GET \
 --header "X-Api-Key: 689bbce8acc68b7a4346acca6a028e6f8126eb792b19a334f8e3f2a12ca8f561"
 --url https://api.developerhub.io/api/v1/audit?max_date=2021-01-19T21:08:44%2B0000
```
{% /code %}
