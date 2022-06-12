## Welcome to duaneking.github.io

Earlier in the year I rediscovered this thing and wanted to make updates with mermaidJS supported as part of the default pipeline, as that for me is the killer blogging and education app that would let me really explore my writing.

Problem: Mermaid does not work on GH-Pages like it very publicly does with the rest of the website by default.  This is intentional, as confirmed by GH Support, who did not care about the accessability issues this creates. My perspective is that GH is simply refusing to enable this when it would be less than a days worth of work to enable millions of people this access, as shown by the timestamps in this repo and my own work, when it would be so easy for them to do so and very diffcult for many others.

I also don't see this solution as optimal; Its a hack that needed to be done to get it working because the server side rendering pipeine of GitHub Pages is utterly broken by design.

I see this work from thier perspective as being simple and easy. I have done it here.  They are forcing people to reinvent the wheel, and wont explain why despite the many bugs tracking thsi issue filed by the community.

Thing is, From my perspective, MermaidJS is just not a visual tool.. Its a tool to communicate visual ideas using unsighted means. This means that its not just about MermaidJS, its about rendering tags and rendering pipelines in the service of people needing to communicate visual ideas in a non-visual way.. such as the blind. MermaidJS is the perfect tool for a blind person to communicate visual ideas to a sighted person. This makes this access so much more important. Rendering tags MUST be standardized for the dream of a file using mermaidJS to render in multiple locations for a blind person.. but they are not set up as a standard.

Every rendering pipeline wants a different rendering tag, because they not at all thinking about the users.

Github wants ```mermaid and IMHO thats simple and works here as you can see below.

But Github Pages forces &#60;pre&#62;&#60;code class="language-mermaid"&#62; and thats so broken on its own becouse it activly currupts whats displayed there first and then activly tells the browser not to try, so its not even real mermaidJS by that point, its currupted and clearly intentionally non-functional from my perspective. I shouldnt have to manually update the DOM to get it to render.

Worse, Every plugin I have seen wants something different, and does not undersand that a universal tag is critical as an entrypoint into rendering.

So the segmentation of rendering is terrible and activly violates its possible future.  But every plugin wants its own rendering tag, instead of allowing a universal format, and truely supporting the projects goals as I understand them by having more community focus on standards that can be reused.

What I wanted as a MermaidJS User is the ability to create a github standard format mermaidJS included markdown file, and have it be rendered just like on github like this one does, but still render on github pages without Jekyll specific edits for formatting or setting values. Thats it. I wanted to FULLY Remove Jekyll from the dependencies map of things I touch or consider or think about or work with. I should not need it installed. I should not care about it. I wanted the same content I create to simply render in multiple places without edits being needed. I wanted to treat a github mermaidJS enabled text file like a jpeg, and be able to download and rendering it wherever.  To me, that is better than just HTML. Thats a Text File that includes both text and images. Its a format that light but can create context.

And I want this by default, using the default github rendering pipeline. But GitHub intentionally broke the default GitHub pages renderign pipeline and it does not include Mermaid support. I thought just checking in my github flavored markdown files would have them render MermaidJS on both without being modifed to render correctly would be the default, but that was not the case. The non-workaround I have here requires I manage this as part of my template and that requires that I either update the files to a new format, or find a way to manage rendering and loading of the mermaidJS library in a way that respects speed and perf so its not loaded on every page that does not have a mermaid diagram on it.

I envisioned creating educational work and books and other content this way. I was excited because I could finallly write and communicate all the ideas that are trapped in my head. Nope.  I'm actually really angry typing this, despite the fact I have a very sub-optimal solution, and I have stayed away from this project because I get angry every time I think about its wasted potential.

This is made impossible by default as the default GitHub flow goes out of is way to intentionally break mermaidJS rendering.  This is further made impossible by the fact that the default plugins used for GHPages are limited by a strict configuration that includes safe=true, making it impossible to add new plugins that could correct the problems blocking this.

My only option with the default pipeline is to allow GH to currupt my data, render it incorrectly, and then in your browser fix it by hand-patching the DOM via JS.

In fact on this page the client is what checks for mermaid diagrams, and if mermaids exist on the page they are rendered after the JS library they need is injected into the DOM. It really should be a server side thing as part of the default github pages rendering pipeline.  I should nbot have to make a template specific overide.

So I reported it to GitHub Support; they ignored the bug for a week, then closed the defect after saying to use a plugin that makes you do EVEN MORE WORK, that further currupts your file formats even more, making it even harder to get this working, and STILL would require edits to pages based in the platform.. because its not supported and uses a different tag syntax than the default github syntax.

I'm just not happy with my solution because I know its sub-optimal and does not support accessability in the way I really want to; I just dont know of a way to add this support if GH itself wont commit to it.

### Mermaid?

I just want this mermaidjs to render without me needing to edit *.md files in a special way. I just want *.md files to render mermaidJS on gh-pages just like it should on gh without having to make any modifications to the file for either. That to me is the most accessable.

I just want the following to render correctly on github Pages with no changes to this index.md file iself. Thats it. That is the use case.

```mermaid
  graph TD;
      A-->B;
      A-->C;
      B-->D;
      C-->D;
```
Bottom of index.md