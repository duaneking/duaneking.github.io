## Welcome

<dl>
  {% for post in site.posts %}
  <dt><b><a href="{{ post.url }}">{{ post.title }} - {{ post.description }}</a></b></dt>
  <dd><p>{{ post.excerpt }}</p></dd>
  {% endfor %}
</dl>

Fin.