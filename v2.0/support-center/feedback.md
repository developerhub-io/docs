---
type: page
title: Feedback
listed: true
slug: feedback
description: 
index_title: Feedback
hidden: 
keywords: 
tags: 
---

Gather feedback from your readers right away from the pages.

To ensure that your documentation is of high quality, up-to-date, and brings the needed information to your readers, then gathering feedback from your readers is of high importance. %product% brings feedback to your readers on the pages, and crunches the data out for you in the dashboard, so you can iterate on the docs and have happier readers.

## How does Feedback work for readers?

When enabled, a question at the bottom of each page would show asking if the page was helpful. The reader may respond with a {% icon classes="far fa-thumbs-up" /%} Yes or a {% icon classes="far fa-thumbs-down" /%} No, which may be followed by a prompt to add a message to explain their feedback.

{% image url="https://res.cloudinary.com/developerhub/image/upload/v1619385559/v2_1/no1zhgofia3ampndzvas.jpg" caption="Feedback prompt" mode="responsive" height="504" width="1016" %}
{% /image %}

## Where can I find the received Feedback?

Feedback can be observed on two levels: Page and project. When a page is liked or disliked, you can view the average sentiment of the page on the right sidebar. You can also see the sentiment log over time, as well as the messages that you received for that page. You may mark the message as read.

{% image url="https://res.cloudinary.com/developerhub/image/upload/v1619735382/v2_1/pewivgxetdeaq1cqmwkk.jpg" mode="responsive" height="676" width="783" %}
{% /image %}

Also, in the [dashboard](/support-center/dashboard), you are also able to see the sentiment for the project against time, as well as all the unread messages. Furthermore, you will find in the dashboard a list of the most liked pages as well as the least liked pages. You can use this information to apply the good documentation style applied in most likes pages into the least liked pages, and analyse the messages to learn how to make the pages better.

{% image url="https://res.cloudinary.com/developerhub/image/upload/v1619735374/v2_1/a5abqfsjuvjvqpoytnms.jpg" mode="responsive" height="969" width="993" %}
{% /image %}

Feedback can be marked as spam by anyone on the team. Feedback marked as spam would be minimised in the feedback dashboard. Spam feedback would not show up under the feedback sidebar of a page. Spam feedback does not count into any statistics nor would they be sent through our notification channels. You could also use [an automatic spam filter](/support-center/feedback#feedback-spam-filter).

## Feedback Notifications

If you have a [Slack](/support-center/slack) channel connected to your project, then we will notify you on the Slack channel of the feedback that you have received.

We send out the notifications every hour.

{% image url="https://res.cloudinary.com/developerhub/image/upload/v1619735477/v2_1/uhqm7he9lhdqd8qt4vxb.jpg" mode="responsive" height="200" width="391" %}
{% /image %}

## Feedback Spam Filter

Feedback spam filter is disabled by default and can be enabled from [Feedback Settings](/support-center/feedback#feedback-settings).

The spam filter flags any newly submitted feedback which has a message that looks useless, suspicious, spammy, too short, malicious or offensive as spam.

When the setting is enabled, any new feedback that contains a message would be sent to OpenAI for spam filtering.

Feedback controls can also be shown or disabled according to the referrer site (the site from which the reader has visited the docs). This can be useful if readers are mistaking your site for the support site of your own B2B customer. As an example, feedback controls can disabled according to referrer by adding the following [Custom JS](/support-center/custom-javascript) :

{% code %}
{% tab language="html" %}
<script>
  var referrer = document.referrer;
  if (!referrer) {
    return;
  }
	var allowedReferrerSites = [
	  window.location.host, // Docs site
	  'example.com'
	];
	var disableFeedback = !allowedReferrerSites.reduce((acc, site) => acc || referrer.includes(site), false);
  
  window.settings.apply({
    feedback: {
      disable: disableFeedback
    }
  });
</script>
{% /tab %}
{% /code %}

The same can be done to set up a referrer deny list.

## Redact PII from Feedback

Personal identifiable information (PII) can be redacted from feedback automatically. It is disable by default and can be enabled from [Feedback Settings](/support-center/feedback#feedback-settings).

The PII filter would redact any information that looks personal from feedback messages as they are submitted, such as names, phone numbers, email addresses, physical addresses, etc...

The PII cannot be recovered after it has been redacted.

When the setting is enabled, any new feedback that contains a message would be sent to OpenAI for PII redaction.

## Feedback Settings

Feedback by default is enabled for all projects if you project was created after April 2021. You may enable or disable Feedback as such:

- From the left sidebar, choose **Project Settings** {% icon classes="fas fa-layer-group inv-icon" /%}.
- Under Feedback, check or uncheck **Allow liking/disliking page .**

Projects on a plan that has Feedback Messages feature (Grow and above) can enable Feedback messages as such:

- From the left sidebar, choose **Project Settings** {% icon classes="fas fa-layer-group inv-icon" /%}.
- Under Feedback, check **Allow adding message.**

To enable or disable spam filtering:

- Under Feedback, check or uncheck **Filter spam**.

To enable or disable redacting personal identifiable information:

- Under Feedback, check or uncheck **Redact personal information**.

## Javascript Hook for Feedback

If you wish to send search analytics to third party services, you can use the `onfeedback` javascript event to listen to feedback events. See [On Feedback](/support-center/developer-tools#on-feedback).