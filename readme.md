# Vue handbook 
## by Saahiththiyan Mathivathanan

All html should be written inside a `template` tag.

```html
<template>
    <h1>Hello World</h1>
</template>
```

### Component
This is how the app.js file is made

```javascript
// App.js
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'app',
  components: {
    HelloWorld
  }
}
```

And all other components are made in seperate something.vue file inside a special folder named `components`. 

```javascript
// HelloWorld.vue
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
```

This component takes a prop called msg which is a string. This component can be added in the app.js file as below

```javascript
// App.js
<template>
  <div id="app">
    <HelloWorld msg="This is a component"/>
  </div>
</template>
```

Then the msg will be used inside the component like below

```javascript
// HelloWorld.vue
<template>
  <h1>{msg}</h1>
</template>
```