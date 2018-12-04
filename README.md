# helloWorld-js

Extremely simple (node-based) repo to create barebones ``html`` pages for ``js`` dev.

## abstract

This repo holds some ``node`` scripts for generating very simple web pages as a *helloWorld* for javascript development. Arguably, this repo might have been better served just containing the barebones ``html`` page. However, there is some utility to running ``node`` on some server-side scripts to generate the pages -- both as a *cool* factor, and also to show some example self-executing ``node`` scripts.

## requirements

A working ``node`` installation.

### get `npm/node`

One mechanism to install the latest `npm/node` on UNIX type systems is using `nvm`. See [here](https://www.digitalocean.com/community/tutorials/how-to-install-node-js-on-ubuntu-18-04).

Note that there seems to be ill-defined behaviour with the standard FNNDSC `.bashrc` env. Please replace the `nvm` supplied changes to `.bashrc` with:

```bash
export NVM_DIR="$HOME/.nvm"
if [[ -s "$NVM_DIR/nvm.sh" ]] ; then 
    cd $NVM_DIR ;  
    source "./nvm.sh"  # This loads nvm
    cd ~
fi
[ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"  # This loads nvm bash_completion
```
#### Select a version

Now, log out and login again. Simply run

```bash
nvm install 11.3.0  # For example
```

## preconditions

### install deps

```bash
npm i simple-html-index
npm i -S posthtml posthtml-beautify
```

### use nvm

```bash
nvm use 11.3.0 # or whatever
```

## script use

Run ``html.js`` to create a simple html page.

Run ``beautify.mjs`` to prettify the created html page.

## example

```bash
html.js helloWorld helloworld.js > input.html
beautify.mjs input.html index.html
python -m http.server 8090
```

