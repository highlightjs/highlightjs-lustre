`highlight.js` syntax definition for Lustre.

For more about highlight.js, see https://highlightjs.org/

For more about Lustre and reactive languages, see
http://www-verimag.imag.fr/DIST-TOOLS/SYNCHRONE/reactive-toolbox/

### Usage

Simply include the `highlight.js` script package in your webpage or node app, load up this module and apply it to `hljs`.

If you're not using a build system and just want to embed this in your webpage:

```html
<script type="text/javascript" src="/path/to/highlight.pack.js"></script>
<script type="text/javascript" src="/path/to/highlightjs-lustre/lustre.js"></script>
<script type="text/javascript">
    hljs.registerLanguage('lustre', window.hljsDefineLustre);
    hljs.highlightAll();
</script>
```

If you're using webpack / rollup / browserify / node:
   
```javascript
var hljs = require('highlightjs');
var hljsDefineLustre = require('highlightjs-lustre');

hljsDefineLustre(hljs);
hljs.highlightAll();
```

### Advanced

This is a pretty simple package, the only thing you might want to do differently is name the language something other than `lustre`. If you want to do this, simply `import { definer } from 'highlightjs-lustre';` and use it like: `hljs.registerLanguage('othername', definer);`.

