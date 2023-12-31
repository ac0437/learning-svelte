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

## Events

Use the `on:<event>` syntax i.e. `<button on:click={clickEvent}>`

Can use callbacks directly on element i.e.
`<button on:click={() => {console.log("event")}}>`

Can add event modifiers and options with pipe i.e.
`<button on:click={clickEvent}|preventDefault>`

see more on [Svelte element directive docs](https://svelte.dev/docs/element-directives#on-eventname)

## Reactive Declerations and Statements

Use `$` which is similar to a [JS label](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/label)
Reactive decleration example: `$: fullname = firstname + ' ' + lastname`
Reactive statement example: `$: console.log(fullname)`

Rules

1. Reactive Declerations and Statements are async meaning that Svelte updates before the DOM changes
2. Order matters
3. Are declared at the top level
