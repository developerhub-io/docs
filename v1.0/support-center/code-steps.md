---
type: page
title: Code Steps
listed: true
slug: code-steps
description: 
index_title: Code Steps
hidden: 
keywords: 
tags: 
---

{% code-steps title="Code Steps" description="Code steps are pages just like this one, where you can show the steps to achieving something in code. This is an example of how you could use [auto$](/support-center/custom-login) on %product%. Our example uses `express` as the backend server." %}
{% step title="Install JWT library" description="First, to generate JWT, it is easier to do it using a library. To install `jsonwebtoken`, run `npm install jsonwebtoken`." codeId="code-1" highlightLines="3" %}
{% /step %}
{% step title="Get API Key" description="The JWT would be signed using the API Key. Get your [auto$](/support-center/api-key) and save it in the code." codeId="code-1" highlightLines="3" %}
{% /step %}
{% step title="Set the payload" description="The payload is the information being sent securely using JWT. The payload for Custom Login is a JSON object and it must have two properties.

`version` must be set to `1` 

`vars` contains the [variables](/support-center/variables) to set when the docs load. You could personalise the docs for the user here." codeId="code-1" highlightLines="7-15" %}
{% /step %}
{% step title="Set Expiry" description="Setting a shorter expiry ensures that if a JWT falls into the wrong hands. We recommend a day." codeId="code-1" highlightLines="16" %}
{% /step %}
{% step title="Sign the token" description="Sign the token with the API key, setting the expiry." codeId="code-1" highlightLines="18" %}
{% /step %}
{% step title="Generate the URL" description="The URL contains the path that the reader tried to access and a query param `jwt` containing the token." codeId="code-1" highlightLines="5-6,20-21" %}
{% /step %}
{% step title="Redirect the user with the token" description="Finally, redirect the user back to the docs with the signed token." codeId="enajA" highlightLines="4-6" %}
{% /step %}
{% code id="code-1" language="javascript" title="developerhub.js" %}
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
{% /code %}
{% code id="enajA" language="javascript" title="server.js" %}
const app = express();
const port = 1234;

app.get('/login', (req, res) => {
  res.redirect(getSignedDeveloperHubUrl(req.query.redirect));
});

app.listen(port, () => {
  console.log(`Reader login app listening at http://localhost:${port}`)
});
{% /code %}
{% /code-steps %}
