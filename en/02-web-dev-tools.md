# Development tools and environmnent

## Code editor or IDE

Ultimately, it's your choice. VSCode is used by teacher.

### [Visual Studio Code (VSCode)](https://code.visualstudio.com/download)

- free & open source code editor by Microsoft (**!=** Visual Studio IDE)
- wide extension support
- lightweight, multiplatform support
- good [docs & instructions](https://code.visualstudio.com/docs/editor/codebasics)
- choice of many Web developers

#### Install Extensions

Press _ctrl-shift-x_ or click extensions icon on the left panel.

Search and install:

- Prettier
- Live Server (by Ritwick Dey)

#### VSCode - Basic Usage

Check: [Visual Studio Code tips and tricks](https://code.visualstudio.com/docs/getstarted/tips-and-tricks)

Active **project** is the folder open on the left side panel (_File -> Open folder..._)

Handy keyboard shortcuts (finnish layout, check _File -> Preferences -> Keyboard shortcuts_ for more)

- Multiline comment: _ctrl-'_
- Delete line: _ctrl-shift-k_
- Move line(s): _alt-up/down_
- Copy line(s): _alt-shift-up/down_
- Auto format code: _alt-shift-f_
- Open integrated console: _ctrl-ö_
- Quick find/open files: _ctrl-p_
- Split editor: _ctrl-§_

### WebStorm/PyCharm (optional)

- free for Metropolia students. [Apply for license here](https://www.jetbrains.com/student/)
  - _@metropolia.fi_ email address needed for a free license
  - then install [ToolBox app](https://www.jetbrains.com/toolbox-app/)
- full-featured IDE
- quite ready out of the box. No need for plugins.
- based on IntelliJ IDEA, just like PyCharm

## Web browser & debugging

- Chrome & [Chrome DevTools](https://developers.google.com/web/tools/chrome-devtools/)
- Browser renders the page based on HTML and CSS and runs the JavaScript code.
- DevTools allows you to inspect the page and see how it is rendered, debug JavaScript code, check network requests etc.
- Keep DevTools _always_ open while developing to see the changes in real time and debug any issues.

## Local web server

- Code works the same as if it was published on the internet, but the page is only visible locally on your own computer
- Live Server by Ritwick Dey is a popular extension for VSCode that you can install directly from the editor's extensions tab
- Then the site opens in the browser at <http(s)://localhost:[PORT]>

## Public web server

- To publish your site on the internet, you need a web server
- Metropolia provides a free web hosting service for students. You can use it to publish your assignments and portfolio.
- You can also use other free hosting services like GitHub Pages, Netlify, Vercel etc.
- We will go through the process of publishing your site on Metropolia's web hosting service in the following weeks.

---

<!-- add mermaid support for gh pages -->
<script type="module">
    Array.from(document.getElementsByClassName("language-mermaid")).forEach(element => {
      element.classList.add("mermaid");
    });
    import mermaid from 'https://cdn.jsdelivr.net/npm/mermaid@11/dist/mermaid.esm.min.mjs';
    mermaid.initialize({startOnLoad: true});
</script>
