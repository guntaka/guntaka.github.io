---
layout: default
permalink: /news/
---

# All Posts
<ul>
	{% for post in site.posts %}
	<li>
		<a href="{{ post.url }}">{{ post.title }}</a>
		<p>{{ post.meta }}</p>
	</li>
	{% endfor %}
</ul>
