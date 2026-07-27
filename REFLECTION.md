## Reflection

### What did you repeat by hand?

For me, the biggest repetition was the `<head>` block: four `<link rel="stylesheet">` lines, copied into all nine HTML files without exception. Inside `guide/`, every one of those links — plus the shared `<header>`, `<nav>`, and
`<footer>` — needed an extra `../` prepended, by hand, with no tooling to catch a missed one before the browser silently failed to load something.
 
Second, the shared skeleton itself was the worst offender: the logo-and-site-name `<header>`, the four-link `<nav>`, and the copyright `<footer>` had to be pasted into every single page, character-for-character identical, because
any drift would break the "same markup everywhere" requirement the assignment grades on. By the fifth paste it stopped feeling like writing HTML and started feeling like manual synchronization work — the exact kind
of tedious, error-prone task a computer should be doing instead of a person.
 
Finally, The four cheese family pages made this most obvious: `fresh.html`, `soft.html`, `blue.html`, and `hard.html` are roughly 90% identical files. Only the `<title>`, `<meta description>`, the family's own text pulled from
`families.txt`, and the previous/next links actually differ from page to page. Everything else — header, nav, footer, the grid wrapper, the hero image markup pattern — is duplicated boilerplate.

### What broke when you moved a file?

Every relative path inside `guide/` depends on correctly counting folder
depth. `images/logo.svg` becomes `../images/logo.svg`; `index.html` becomes
`../index.html`. Get the count wrong just once and the browser doesn't warn
you at all — the image or link just quietly 404s, and you only notice by
staring at the rendered page and wondering why the logo disappeared.

### What would you want a tool to generate for you?

I'd like a way to write the shared header, navigation, and footer once and reuse them on every page. That would make updates much easier.

I'd also like a tool that automatically handles relative paths. Counting `../` by hand is easy to mess up, and it gets repetitive. After this project, I understand why people use web components or static site generators.