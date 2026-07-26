## Reflection

### What did you repeat by hand?

The biggest thing I repeated was the `<head>` section. I copied the same four CSS `<link>` tags into all nine HTML files. For the pages inside the `guide/` folder, I also had to change every path by adding `../`, including the CSS files, logo, and navigation links.

I also copied the same `<header>`, `<nav>`, and `<footer>` into every page. If I wanted to change one navigation link, I had to edit every HTML file manually.

The four cheese pages (`fresh.html`, `soft.html`, `blue.html`, and `hard.html`) were almost identical. The only differences were the page title, meta description, main content, and the previous/next navigation links.

### What broke when you moved a file?

The biggest issue was the relative paths. Files inside the `guide/` folder needed `../` before paths like `images/logo.svg` and `index.html`. If I counted the folders wrong, images or links would stop working. The browser didn't really tell me what was wrong, so I had to check everything myself.

### What would you want a tool to generate for you?

I'd like a way to write the shared header, navigation, and footer once and reuse them on every page. That would make updates much easier.

I'd also like a tool that automatically handles relative paths. Counting `../` by hand is easy to mess up, and it gets repetitive. After this project, I understand why people use web components or static site generators.