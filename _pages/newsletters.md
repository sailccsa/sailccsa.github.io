---
title: Newsletters
permalink: /newsletters/
---
Read past issues of the FairWinds newsletter.

{% assign newsletters = site.static_files | where: "collection", "newsletters" | where: "extname", ".pdf" | sort: "basename" %}
<ul>
{% for pdf in newsletters %}
  <li><a href="{{ pdf.path | split: '_newsletters/' | last | prepend: '/newsletters/' | uri_escape | relative_url }}">{{ pdf.basename | replace: '-', ' ' | replace: '_', ' ' }}</a></li>
{% endfor %}
</ul>
