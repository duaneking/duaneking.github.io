## Welcome

<dl>
  {% for post in site.posts %}
  <dt>{{ post.date | date: "%B %-d, %Y"}} - <a href="{{ post.url }}">{{ post.title }}</a></dt>
  <dd><p>{{ post.excerpt }}</p></dd>
  {% endfor %}
</dl>

Fin.