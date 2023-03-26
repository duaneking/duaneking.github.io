## Welcome to duaneking.GitHub.io

<ol>
{% for post in site.posts %}
<li><a href="{{ post.url }}">{{ post.title }}</a><p>{{ post.description }}</p></li>
{% endfor %}
</ol>


Fin.