# Vue handbook :green_apple:
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

```html
// App.js
<template>
  <div id="app">
    <HelloWorld msg="This is a component"/>
  </div>
</template>
```

Then the msg will be used inside the component like below

```html
// HelloWorld.vue
<template>
  <h1>{msg}</h1>
</template>
```

### Data

Data can be set using two ways

```javascript
// 1st way
export default {
  name: 'HelloWorld',
  data: {
    name: 'saahi'
  }
}

// 2nd way
export default {
  name: 'HelloWorld',
  data() {
    return {
      name: 'saahi'
    }
  }
}
```

Where the first way the data is an object used to set common data that can be accessed by all components. But in the second way the data is a function that sets the name unique to each component. i.e the name variable will same even if the instance of the name is changed in another component.


