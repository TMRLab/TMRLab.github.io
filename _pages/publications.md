---
layout: splash
permalink: /publications/
title: "What We’re Writing"
excerpt: "Explore the Discoveries Shaping Our Field"
header:
  overlay_color: "#5e616c"
  overlay_image: /assets/images/home/main_publications.png
---

<p class="page__year-nav" style="margin:0;display:inline;float:right">
{% for group in site.data.publications %}
        <a href="#{{ group.year }}" class="btn btn--info btn--small">{{ group.year }}</a>
{% endfor %}
</p>
<br >

{% for group in site.data.publications %}
## {{ group.year }}
{:#{{ group.year }}}

{% for pub in group.items %}
{% include publication
        authors=pub.authors
        title=pub.title
        journal=pub.journal
        page=pub.page
        pmid=pub.pmid
        doi=pub.doi
        status=pub.status
%}
{% endfor %}

{% endfor %}
