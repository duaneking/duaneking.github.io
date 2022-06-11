---
mermaid: true
---

## Welcome to duaneking.github.io

Earlier in the year I rediscovered this thing and hoped to make updates as I could with mermaidJS supported, as that for me is the killer blogging and education app.  Thing is, Mermaid does not work on GH-Pages like it very publicly does with the rest of the website and so I can't help but feel lied to by GH because from my perspective, GH is simply refusing to enable this when it would be less than a days worth of work to enable millions of people, when it would be so easy for them to do so, but very diffcult for others. I see this work from thier perspective as being simple and easy, but they want people to have to fight a broken system instead, and they are forcing people to reinvent the wheel, and based on my conversation with people, they just seem to want to make it impossible for people and wont explain why.

Thing is, From my perspective, MermaidJS is just not a visual tool.. Its a tool to communicate visual ideas using unsighted means. This means that its not just about MermaidJS, its abvout rendering tags and rendering pipelines in the service of people needing to communicate visual ideas in a non-visual way.. such as the blind. Rendering tags MUST be standardized for the dream of a file using mermaidJS to render in multiple locations for a blind person.. but they are not set up as a standard.

GitGub, the mermaidJS community, etc, is absolutly FAILING at this.

Every rendering pipeline wants a different rendering tag, because they are dumb and egotistical and not at all thinking about the users.

Github wants ```mermaid.

Github Pages forces <code-lang="mermaid"> and thats so broken on its own.

Every plugin I have seen wants something different, because they are dumb, and dont undersand that a universal tag is critical.

So the segmentation of rendering is terrible and activly violates its possible future.  But every plugin wants its own rendering tag, because they all have FOMO and want to claim mermaidJS as something they own or claim to be involved in instead of allowing it to be a universal format and truely supporting the projects goals as I understand them.

What I want as a MermaidJS User is the ability to create a github mermaidJS markdown file, and have it be rendered just like on github like this one does, but still render on github pages. Thats it. I want the same content I create to simply render in multiple places without edits being needed. I want to treat a github mermaidJS enabled text file like a jpeg and be able to download and rendering it wherever.  To me, that is better than just HTML.  And I want this by default, using the default github rendering pipeline. But GitHub intentionally broke it. I envisioned just checking in my github flavored markdown files and then having them render MermaidJS on both without being modifed to render correctly. I envisioned writting educational work and books and other content this way. I was excited because I could finallly write and communicte all the ideas that are trapped in my head. Nope.  I'm angry typing this, and I have stayed away from this project becsause I get angry every time I think about its wasted potential.

This is made impossible by the fact that the default GitHub flow activly goes out of is way to break mermaidJS rendering.  This is further made impossible by the fact that the default plugins used for GHPages are limited by safe=true, making it impossible to add new plugins that could correct the problems blocking this.

So I reported it to GitHubSupport; they closed the defect and said to use a plugin that makes you do EVEN MORE WORK, that currupts your file formats even more, making it even harder to get this working, and STILL would require edits to pages based in the platform.

WTF. Its like GutHub is being hostile to accessability. I dont understand why when they could fix this for everybody instead of everybody having to recreate the wheel.

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