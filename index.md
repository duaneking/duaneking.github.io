## Welcome to duaneking.GitHub.io

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>

## It Works.
I got MermaidJS working.

My only option with the default pipeline for GitHub Pages is to allow GitHub to corrupt my input data, render it slightly incorrectly, and then in your browser fix it by hand-patching the DOM via JS.

In fact on this page the client is what checks for mermaid diagrams, and if mermaids exist on the page they are rendered after the JS library they need is injected into the DOM. It really should be a server side thing as part of the default GitHub pages rendering pipeline.  I should not have to make a template specific override.

I'm just not happy with my solution because I know its sub-optimal and does not support accessibility in the way I really want to; I just don't know of a way to add this support if GitHub itself wont commit to it.

### Mermaid?

I just want this mermaidjs to render without me needing to edit .md files in a special way. I just want .md files to render mermaidJS on gh-pages just like it does on GH without having to make any modifications to the file for either. That to me is the most accessible.

I just want the following to render correctly on GitHub Pages with no changes to this index.md file itself. That's it. That is the use case.

```mermaid
  graph TD;
      A-->B;
      A-->C;
      B-->D;
      C-->D;
```
Bottom of index.md