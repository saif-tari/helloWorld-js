# helloWorld-js

Extremely simple (node-based) repo to create barebones ``html`` pages for ``js`` dev.

# preconditions:

## install deps:

        npm i simple-html-index
        npm i -S posthtml posthtml-beautify

## use nvm:

	nvm use 11.3.0 # or whatever

# purpose:

        Run 'html.js' to create a simple html page.
        Run 'beautify.mjs' to prettify the created html page.

# example:

        html.js helloWorld helloworld.js > input.html
        beautify.mjs input.html index.html
        python -m http.server 8090

