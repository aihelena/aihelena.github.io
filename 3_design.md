---
layout: page
title: Design and crafting
image: /assets/images/logo_sketches.jpg
desc: design
permalink: /design/
nav-menu: true
---

<!-- Main -->
<div id="main" class="alt">

<!-- One -->
<section id="one">
	<div class="inner">
		<header class="major">
			<h1>Design</h1>
		</header>
	</div>

     {% include tiles_landing.html %}
  </section>

<!-- Two -->
<section id="two">
	<div class="inner">
		<header class="major">
			<h1>Cosplay</h1>
		</header>
	</div>
	<section id="one" class="split_tile">
 		{% for post in site.categories[page.desc] limit:site.tiles-count %}
   		 {% if post.show_tile != false and post.sec2 == true %}
  		<article>
    		<span class="image">
      			<img src="{{ post.image }}" alt="" />
    		</span>
    		<a href="{{ post.url  | relative_url }}" class="link">
        	<header class="major">
          		<h3>{{ post.title }}</h3>
          		<p>{{ post.description }}</p>
        	</header>
    		</a>
  		</article>
    	  {% endif %}
  		{% endfor %}
	</section>

  </section>
