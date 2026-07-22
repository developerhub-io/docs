---
type: page
title: Logging Out Readers
listed: true
description: 
index_title: Logging Out Readers
hidden: false
keywords: 
tags: 
---

To log out readers, a `logout` function can be called on the `window` object.

For example, if you wish to allow the readers to log out themselves from a secure session, a logout button can be added to the top right corner next to the navigation links. Add the following [Custom JS](../custom-javascript.md):

{% code %}
```html
<script>
  document.addEventListener('onprojectloaded', function () {
    var logoutBtn = document.createElement('DIV');
    logoutBtn.innerHTML = 'Logout';
    logoutBtn.classList.add('logout'); // Style as needed
    logoutBtn.onclick = function() {
      window.logout();
      window.location.href = '/'; // Change this to a useful link
    };
    document.querySelector('.links-container').appendChild(logoutBtn);
  });
</script>
```
{% /code %}
