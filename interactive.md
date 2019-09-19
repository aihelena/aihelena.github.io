---
layout: page
title: Interactive Art
image: /assets/images/mimsy.jpg
permalink: /interactive/
nav-menu: true
---

<!-- Main -->
<div id="main" class="alt">

<!-- One -->
<section id="one">
	<div class="inner">
		<header class="major">
			<h1>Interactive Art</h1>
		</header>
	</div>
</section>

<section id="two" class="tiles">
  {% for post in site.posts limit:site.tiles-count %}
  {% if site.tiles-source == 'posts' %}
  <article>
    <span class="image">
      <img src="{{ post.image }}" alt="" />
    </span>
    <header class="major">
      <h3><a href="{{ post.url  | relative_url }}" class="link">{{ post.title }}</a></h3>
      <p>{{ post.description }}</p>
    </header>
  </article>
  {% endif %}
  {% endfor %}