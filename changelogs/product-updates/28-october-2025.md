---
title: '28 October 2025'
date: '2025-10-27 21:05:12'
published: true
---

- {% badge text="New" type="success" /%} **API Reference**: We are excited to announce that we have initiated incremental support for OpenAPI 3.2. You can now upload and validate OpenAPI 3.2 definitions. Additionally, we have extended our capabilities to include support for the QUERY, OPTIONS, TRACE, and HEAD methods.
- {% badge text="Change" type="warning" /%} **API Reference**: New API reference validator with better output. Invalid OpenAPI structure might no longer be accepted. `nullable` is no longer accepted in OpenAPI 3.1+, instead `type: [string, "null"]` can be used.
