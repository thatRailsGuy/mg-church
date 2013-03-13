---
layout: default
title: This is the index page
---

##Recent Posts
<ul>
  {% for post in site.posts do %}
  <li>
    {{ post.date | date_to_string }} <a href="{{ post.url }}">{{ post.title }}</a>
  </li>
  {% endfor %}
</ul>

##prayers

<ul>
  {% for post in site.categories.prayer %}
  <li>
    {{ post.date | date_to_string }} <a href="{{ post.url }}">{{ post.title }}</a>
  </li>
  {% endfor %}
</ul>

<dl>
	{% for cat in site.categories %}
    <dt>{{ cat[0] }}</dt>
		{% for post in cat[1] %}
			<dd> {{ post.date | date_to_string }} <a href="{{ post.url }}">{{ post.title }}</a> </dd>
		{% endfor %}
	{% endfor %}
</dl>