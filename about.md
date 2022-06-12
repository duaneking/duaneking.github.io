# About

If you need to find something, search here.

# Docs

{% assign mydocs = site.docs | group_by: 'category' %}
{% for cat in mydocs %}
<h2> {{ cat.name | capitalize }} </h2>
<ul>
{% assign items = cat.items | sort: 'order' %}
{% for item in items %}
<li><a href="{{ item.url }}">{{ item.title }}</a></li>
{% endfor %}
</ul>
{% endfor %}


# Site Pages by category.

{% assign mydocs = site.pages | group_by: 'category' %}
{% for cat in mydocs %}
<h2>{{ cat.name | capitalize }}</h2>
<ul>
{% assign items = cat.items | sort: 'order' %}
{% for item in items %}
<li><a href="{{ item.url }}">{{ item.title }}</a></li>
{% endfor %}
</ul>
{% endfor %}


# Site Pages

{% for post in site.pages %}
<a href="{{ page.permalink }}">{{ page.title }}</a>
<p>{{ page.description }}</p>
<section id="{{ post.id }}">
<a href="{{ page.permalink }}" class="btn"><span class="icon"></span>{{ site.name }}</a>
</section>
{% endfor %}

# Site Posts

<ul>
{% for post in site.posts %}
<li>
<a href="{{ post.url }}">{{ post.title }}</a>
<p>{{ post.description }}</p>
</li>
{% endfor %}
</ul>
