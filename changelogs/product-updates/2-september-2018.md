---
title: '2 September 2018'
date: '2018-09-02 10:28:53'
published: true
---

- {% badge text="New" type="success" /%} **Tables**: Organise your data in tabular format in responsive [tables](https://docs.developerhub.io/v1/support-center/tables). Here is how it looks like:

{% table layout="auto" %}
{% row %}
{% cell header=true %}
Parameter
{% /cell %}
{% cell header=true %}
Type
{% /cell %}
{% cell header=true %}
Default
{% /cell %}
{% /row %}
{% row %}
{% cell %}
user\_id
{% /cell %}
{% cell %}
int
{% /cell %}
{% cell %}
Auto-generated
{% /cell %}
{% /row %}
{% row %}
{% cell %}
user\_name
{% /cell %}
{% cell %}
string
{% /cell %}
{% cell %}
John Doe
{% /cell %}
{% /row %}
{% row %}
{% cell %}
user\_age
{% /cell %}
{% cell %}
int
{% /cell %}
{% cell %}
25
{% /cell %}
{% /row %}
{% /table %}
