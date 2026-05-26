---
layout: splash
permalink: /team/
title: "Meet our team"
excerpt: "Meet the People Behind the Work"
header:
  overlay_color: "#5e616c"
  overlay_image: /assets/images/home/main_team.png
---

<p class="page__year-nav" style="text-align: right;">
<a href="#current-members" class="btn btn--info btn--small">Current members</a>
<a href="#past-members" class="btn btn--info btn--small">Past members</a>
</p>

## Current Members

<table class="team-table" border="0" width="100%">
{% for member in site.data.members %}
  <tr valign="top">
    <td width="23%">
      <div class="author__avatar">
        <center><img src="{{ member.avatar | relative_url }}" alt="{{ member.name }}" itemprop="image" class="u-photo"></center>
      </div>
      <br />
      <div class="member-links">{% if member.email %}<a href="mailto:{{ member.email }}" rel="me" class="u-email u-link-plain"><meta itemprop="email" content="{{ member.email }}" /><i class="fas fa-fw fa-envelope-square" aria-hidden="true"></i><span class="label">{{ site.data.ui-text[site.locale].email_label | default: "Email" }}</span></a>{% endif %}{% if member.linkedin %}<a class="u-link-plain" href="https://www.linkedin.com/in/{{ member.linkedin }}" itemprop="sameAs" rel="nofollow noopener noreferrer me" target="_blank"><i class="fab fa-fw fa-linkedin" aria-hidden="true"></i><span class="label">LinkedIn</span></a>{% endif %}{% if member.website %}<a class="u-link-plain" href="{{ member.website }}" itemprop="url" rel="me" target="_blank"><i class="fas fa-fw fa-link" aria-hidden="true"></i><span class="label">Website</span></a>{% endif %}</div>
    </td>
    <td width="77%">
      <div class="author__content">
        <h3 class="author__name p-name" itemprop="name">{{ member.name }}{% if member.suffix %}, {{ member.suffix }}{% endif %}</h3>
        <div class="author__role p-note" itemprop="description">
        <i>{{ member.role }}</i>
        </div>
      </div>
      <div class="author__bio p-note" itemprop="description">
        {{ member.bio }}
      </div>
    </td>
  </tr>
{% endfor %}
</table>

## Past Members
