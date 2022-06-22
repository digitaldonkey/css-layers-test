# CSS Layers test tool 

To reproduce https://bugs.chromium.org/p/chromium/issues/detail?id=1338543

What steps will reproduce the problem?


Creat basic HTML page with   <style>@layer base, layout, component, state, theme;</style>

1. add `@import url('styles.css') layer(state); to <style>`
2. add  `<link rel="stylesheet" media="all" href="styles.css" layer="theme" />`

Check Dev Tools. 

What is the expected result?

a) Layer button shows up in dev tools. Everything as expected (Described in https://developer.chrome.com/blog/new-in-devtools-101/#layer) 

b) No layer Button shows up. No defined layers in dev tools

Now I see: It's not part of the "supported" implementation :/ 

https://github.com/whatwg/html/issues/7540

Chrome Page on it 

https://developer.chrome.com/blog/new-in-devtools-101/#layer
