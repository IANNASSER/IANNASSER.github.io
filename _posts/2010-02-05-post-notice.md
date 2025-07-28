---
title: "Post: Notice"
categories:
  - Blog
tags:
  - Cybersecurity
  - Post Formats
  - Notice
---

A notice displays information that explains nearby content. Often used to call attention to a particular detail—especially important in cybersecurity and digital communications.

When using Kramdown `{: .notice}` can be added after a sentence to assign the `.notice` to the `<p></p>` element.

**Changes in Service:** We have recently updated our [privacy policy](#) to further protect our users' data and privacy. Please review the changes for your awareness.
{: .notice}

**Cybersecurity Tip:** Always use strong, unique passwords and enable multi-factor authentication for your accounts.
{: .notice--primary}

**Info Notice:** New blog posts on AI in cybersecurity and digital forensics are now available. [Check them out here](#).
{: .notice--info}

**Warning Notice:** Suspicious activity detected—please ensure your systems are patched and up-to-date to avoid vulnerabilities.
{: .notice--warning}

**Danger Notice:** Recent reports of phishing and ransomware attacks targeting Nairobi organizations. Stay vigilant and verify any unexpected messages.
{: .notice--danger}

**Success Notice:** Congratulations to our cybersecurity students for completing the latest round of hands-on AI training!
{: .notice--success}

Want to wrap several paragraphs or other elements in a notice? Using Liquid to capture the content and then filter it with `markdownify` is a good way to go.

```html
{% raw %}{% capture notice-2 %}
#### New Site Features

* Cover images now supported on blog pages
* Auto-save for drafts while writing
* New cybersecurity resources section live
{% endcapture %}{% endraw %}

<div class="notice">{% raw %}{{ notice-2 | markdownify }}{% endraw %}</div>
```

{% capture notice-2 %}
#### New Site Features

* Cover images now supported on blog pages
* Auto-save for drafts while writing
* New cybersecurity resources section live
{% endcapture %}

<div class="notice">
  {{ notice-2 | markdownify }}
</div>

Or you could skip the capture and stick with straight HTML.

```html
<div class="notice">
  <h4>Message</h4>
  <p>A basic message.</p>
</div>
```

<div class="notice">
  <h4>Message</h4>
  <p>A basic message.</p>
</div>
