## Welcome to duaneking.GitHub.io

## It Works.
I got MermaidJS working.  Now I'm working on optimizing things.

My only option with the default pipeline for GitHub Pages is to allow GitHub to corrupt my input data, render it slightly incorrectly, and then in your browser fix it by hand-patching the DOM via JS.  That works.

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