<!-- @format -->

# learning-svelte

Following: https://youtu.be/UGBJHYpHPvA

## [Create Svelte Project](https://kit.svelte.dev/docs/creating-a-project)

npm create svelte@latest my-app
cd my-app
npm install
npm run dev

## Databinding

Use {} to a element attribute i.e. `<img src={imageURL}/>`
We can use shorthand if data has the same name of the element attribute `{src}/>`

## Reactivity

Svelte can update anything it considers a state.
We can see this is the compiled JS output by the $$invalidate wrapper.

### States the get updated

1. Assignment

```js
let counter = 0;
count = 10;
```

2. Update statement

```js
let counter = 0;
count++;
```

3. Object update or assignment

```js
let obj = {};
obj['foo'] = 10;
```

## State that does not get updated

1. An object that is passed by reference

```js
let obj = {};
let refObj = obj;
refObj['foo'] = 10;
```

2. Calling a method

```js
let arr = [];
arr.push(1);
```
