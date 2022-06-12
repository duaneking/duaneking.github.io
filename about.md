# About

If you need to find something, search here.

# Site Pages by category.

{% assign mydocs = site.pages | where_exp: "page", "page.categories" | group_by: 'category' %}
{% for cat in mydocs | where_exp: "cat", "cat.name" %}
<h2>Category: {{ cat.name | capitalize }}</h2>
<ol>
{% assign items = cat.items | sort: 'order' %}
{% for item in items | where_exp: "item", "item.title" | where_exp: "item", "item.title" | %}
<li><a href="{{ item.url }}">Item: {{ item.title }}</a></li>
{% endfor %}
</ol>
{% endfor %}


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
