---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---
<body>
<p>You can also find my articles on <a href="https://scholar.google.com/citations?hl=en&user=sjCrkSgAAAAJ">my Google Scholar profile</a>.</p>
</body>
<!-- <head>
<script src="https://kit.fontawesome.com/61ebb60581.js" crossorigin="anonymous"></script>
</head>
<p><strong>Paper 1</strong>
<br>Author
<br>arXiv 2023
<br>
<a href="https://arxiv.org/abs/><i class="fas fa-file-pdf"> PDF</i></a>
<a href="https://github.com/"><i class="fab fa-github"> Code</i></a>
<a href="/publication/paper1"><i class="fas fa-link"> Read more</i></a> <!-- Link to the publication/paper1 page -->
<!-- </p>


<p>You can also find my articles on <a href="https://scholar.google.com/citations?hl=en&user=sjCrkSgAAAAJ">my Google Scholar profile</a>.</p>

</body> --> 

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}
