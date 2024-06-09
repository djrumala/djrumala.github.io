---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

<<<<<<< HEAD

<p>You can also find my articles on <a href="https://scholar.google.com/citations?hl=en&user=sjCrkSgAAAAJ" target="_blank">my Google Scholar profile</a>.</p>


{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
=======
{% if site.author.googlescholar %}
  <div class="wordwrap">You can also find my articles on <a href="{{site.author.googlescholar}}">my Google Scholar profile</a>.</div>
>>>>>>> 5dee723c4017b7d297a31daa3950d8eeb6570c61
{% endif %}

{% include base_path %}

{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}
