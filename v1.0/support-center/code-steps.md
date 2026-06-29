---
type: page
title: Code Steps
listed: true
slug: code-steps
description: 
index_title: Code Steps
hidden: 
keywords: code walkthough, recipe
tags: 
---

{% code-steps %}
Code steps are pages just like this one, where you can show the steps to achieving something in code. To add a code step:

- From the index, click on a {% icon classes="fas fa-plus" /%}.
- Choose Code Steps {% icon classes="fas fa-terminal" /%}

To demonstrate Code Steps, this is an example of how you could use [Custom Login](/support-center/custom-login) on %product%.

This example uses `express` as the backend server.

{% step title="Install JWT library" codeId="code-1" highlightLines="1" %}
First, to generate JWT, it is easier to do it using a library. To install `jsonwebtoken`, run `npm install jsonwebtoken`.
{% /step %}

{% step title="Get API Key" codeId="code-1" highlightLines="3" %}
The JWT would be signed using the API Key. Get your [API Key](/support-center/api-key) and save it in the code.
{% /step %}

{% step title="Set the payload" codeId="code-1" highlightLines="7-15" %}
The payload is the information being sent securely using JWT. The payload for Custom Login is a JSON object and it must have two properties.

`version` must be set to `1`

`vars` contains the [variables](/support-center/variables) to set when the docs load. You could personalise the docs for the user here.
{% /step %}

{% step title="Set Expiry" codeId="code-1" highlightLines="16" %}
Setting a shorter expiry ensures that if a JWT falls into the wrong hands. We recommend a day.
{% /step %}

{% step title="Sign the token" codeId="code-1" highlightLines="18" %}
Sign the token with the API key, setting the expiry.
{% /step %}

{% step title="Generate the URL" codeId="code-1" highlightLines="5-6,20-21" %}
The URL contains the path that the reader tried to access and a query param `jwt` containing the token.
{% /step %}

{% step title="Redirect the user with the token" codeId="enajA" highlightLines="4-6" %}
Finally, redirect the user back to the docs with the signed token.
{% /step %}

```javascript {% id="code-1" title="developerhub.js" %}
const sign = require('jsonwebtoken').sign;

const apiKey = '689c3ce8e7c68b7c7f86acca6a028e6f8656eb792b19a334f8e3f2a56ca8f561';

function getSignedDeveloperHubUrl(url) {
  const docsUrl = url || 'https://docs.pied-piper.com';
  const payload = {
    version: 1,
    vars: {
      user: {
        id: 1234,
        name: "John"
      }
  	}
  };
  const expiresIn = 24 * 60 * 60;

  const token = sign(payload, apiKey, {expiresIn: expiresIn});

  return `${docsUrl}?jwt=${token}`;
}
```

```javascript {% id="enajA" title="server.js" %}
const app = express();
const port = 1234;

app.get('/login', (req, res) => {
  res.redirect(getSignedDeveloperHubUrl(req.query.redirect));
});

app.listen(port, () => {
  console.log(`Reader login app listening at http://localhost:${port}`)
});
```
{% /code-steps %}
