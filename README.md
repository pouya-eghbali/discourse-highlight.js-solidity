# discourse-highlight.js-solidity

This is a Discourse theme component that enables the Solidity language for Highlight.js. 

# How I made this

- Took the JS code from https://github.com/highlightjs/highlightjs-solidity and saved it on a solidity.js file in the highlight.js `src/languages` folder. 
- Modified the JS file to have it have only an anonymous JS function: 

```
function(hljs) {
...
}
```

- Ran `node tools/build.js -t cdn none` to generate the minimized lang file for Solidity. 
- Took that minimized function and fed it to Discourse's `api.registerHighlightJSLanguage`. 
