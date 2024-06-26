# Typescript Project Setup

- Following a really basic guide to bootstrap a typescript project
- I have been helping some friends with a typescript side 
project so I am been teaching myself the build tools 
- This document is to familarize myself with them.


[Using Fireships 2023 guide](https://www.youtube.com/watch?v=H91aqUHn8sE)

# Setting up local Env
- I am using `asdf`
- so in a directory set your nodejs version to 20.12.2
`asdf install nodejs 20.12.2`
`asdf local nodejs 20.12.2`

# Setting up node & typescript
1. Setting up a new project `npm init -y`
2. create an index.js `touch index.js`

    commonjs --> `const fs = require('fs');`

    similar to python/go
    esmodule --> `import fs from 'fs';

    running `node .` with the import fs code will give us an error

3. Adjust the `type` in the package.json

```
...
"main": "index.js",
"type": "module"

```

now `node .` will work! 

4. Adding typescript
- `npm install typescript --save-dev`


`--save` will route it to a core dependency
`--save-dev` will route it a dev depencney 

A good explaintion I've heard is what needs to be part 
of the core project to work. 

ex. you dont need a test suite to run the core app 

5. Adding the build method `tsc`

in the `package.json` add the following

we want to be able to build the project using the `tsc`

```
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
    "build": "tsc"
  },

```

5.  Adding types declaration for errors
- `npm i -D@types/node`

6. Create  Source Directory 
7. Create tsconfig.js
- module the define system of the program (commonjs good for require)
- nodenext is newer
moduleResoluton is how code will be found if you import
- ES2020 if is a modern version of node.
- sourcemap to the comon
- outdir where the file js code will go.

- include will have the source directory.
