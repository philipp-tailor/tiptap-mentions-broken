# What this repo contains

A combination of the [Tiptap Vue 2 installation guide](https://tiptap.dev/installation/vue2) and the [mentions starter guide](https://tiptap.dev/api/nodes/mention), in a basic Vue 2 + Vite repository.

Mentions work in development (`yarn dev`), but not in builds (`yarn build`).

# How to trigger issue

1. ```yarn build```
1. serve the `dist` folder
1. type `@` 

## Expected result

The mention suggestion list renders.

## Actual result

```
vue.runtime.esm.js:3737 Uncaught (in promise) TypeError: Cannot read properties of undefined (reading 'abstract')
    at og (vue.runtime.esm.js:3737:32)
    at t._init (vue.runtime.esm.js:5686:9)
    at new a (vue.runtime.esm.js:5826:18)
    at new TO (index.js:213:20)
    at Object.onStart (suggestion.js:19:21)
    at Object.update (index.js:124:141)
og	@	vue.runtime.esm.js:3737
t._init	@	vue.runtime.esm.js:5686
a	@	vue.runtime.esm.js:5826
TO	@	index.js:213
onStart	@	suggestion.js:19
update	@	index.js:124
await in update (async)		
updatePluginViews	@	index.js:5322
updateStateInner	@	index.js:5269
updateState	@	index.js:5199
dispatchTransaction	@	index.js:3653
dispatch	@	index.js:5551
I0	@	index.js:4952
(anonymous)	@	index.js:5141
flush	@	index.js:4581
E0.observer	@	index.js:4433
```

Further typing creates follow-up exceptions:

```
suggestion.js:64 Uncaught TypeError: Cannot read properties of undefined (reading 'ref')
    at Object.onKeyDown (suggestion.js:64:26)
    at Ue.handleKeyDown (index.js:209:143)
    at index.js:3059:50
    at B0.someProp (index.js:5352:50)
    at Le.keydown (index.js:3059:19)
    at t.dom.addEventListener.t.input.eventHandlers.<computed> (index.js:2981:17)
onKeyDown	@	suggestion.js:64
handleKeyDown	@	index.js:209
(anonymous)	@	index.js:3059
someProp	@	index.js:5352
Le.keydown	@	index.js:3059
t.dom.addEventListener.t.input.eventHandlers.<computed>	@	index.js:2981
```

and

```
suggestion.js:46 Uncaught (in promise) TypeError: Cannot read properties of undefined (reading 'updateProps')
    at Object.onUpdate (suggestion.js:46:19)
    at Object.update (index.js:121:142)
onUpdate	@	suggestion.js:46
update	@	index.js:121
await in update (async)		
updatePluginViews	@	index.js:5322
updateStateInner	@	index.js:5269
updateState	@	index.js:5199
dispatchTransaction	@	index.js:3653
dispatch	@	index.js:5551
I0	@	index.js:4952
(anonymous)	@	index.js:5141
flush	@	index.js:4581
E0.observer	@	index.js:4433
```
