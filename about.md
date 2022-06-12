# About

If you need to find something, search here.

# Site Pages

{% for page in site.pages %}
<section id="{{ page.id }}">
<a href="{{ page.url }}" class="btn"><span class="icon"></span>{{ page.name }}</a>
</section>
{% endfor %}

# Site Posts

<ol>
{% for post in site.posts %}
<li>
<a href="{{ post.url }}">{{ post.title }}</a>
<p>{{ post.description }}</p>
</li>
{% endfor %}
</ol>
