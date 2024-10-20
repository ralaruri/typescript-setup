# Typescript Project Setup

- Following a really basic guide to bootstrap a typescript project
- I have been helping some friends with a typescript side 
project so I am been teaching myself the build tools 
- This document is to familarize myself with them.

# Setting up local Env
- I am using `asdf`
- so in a directory set your nodejs version to 20.12.2
`asdf install nodejs 20.12.2`
`asdf local nodejs 20.12.2`


# Difference between npm & npx?

- NPM is package manager for installing deleting and updating javascript packages.
- NPX is a package executor that lets you execute a package without installing them.
- In this case we are using `npm` to install and init some packages
- NPX is used in this case sometimes to run a typescript file
example
```
npm i -D tsx
npx tsx src/index.ts
```

# About tsx
I found the eaiest way to run typescript code is through tsx

[https://www.npmjs.com/package/tsx#how-is-tsx-different-from-ts-node
](https://tsx.is/)

So when you run `node file.js` for javascript in typescript you'd run 

`tsx file.ts` 

It really helps simplify the workflow needed to get up and running on a typescript project.

# Setting up node & typescript
1. mkdir `my-typescript-app`
2. `git init`
3. Setting up a new project `npm init -y`
4. install dev dependencies `npm i -D typescript ts-node @types/node`
5. npm i -D tsx
6. create an index.ts `touch index.ts`
5. Adding typescript
- `cd .`


`--save` will route it to a core dependency
`--save-dev` will route it a dev depencney 

A good explaintion I've heard is what needs to be part 
of the core project to work. 

ex. you dont need a test suite to run the core app 

in the `package.json` add the following


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
