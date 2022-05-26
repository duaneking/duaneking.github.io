---
mermaid: true
---

## Welcome to duaneking.github.io

I just rediscovered this thing and hoped  to make updates as I can if mermaid is supported as that for me is the killer app.  Thing is, Mermaid does not work and I feel lied to by gh.

### Mermaid?

Lets test if this renders.

```mermaid
  graph TD;
      A-->B;
      A-->C;
      B-->D;
      C-->D;
```

{% if page.mermaid %}
  {% include mermaid.html %}
{% endif %}
