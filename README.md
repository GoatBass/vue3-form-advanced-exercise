# vue3-form-advanced-exercise

## Exercise N°7

1. Create a `RatingControl.vue` file into `src/components` folder. 
This component should contain 3 buttons (`Poor`, `Average`, `Great`).
On each button click you have to call a method which will emit a `update:modelValue` event.
Declare the props `modelValue` and bind the `v-model` parent value with a css class `.active`, if the value match with your button.
Add a `question` props to customize the question label.

2. Create a component `TheForm.vue` into the `src/components` folder. 
Add following data object `{ rating: null }`.
Add a form tag, with a submit event listener.
Use the `RatingControl` component inside your form and use `v-model` on rating property.
Add a submit button.
The submit method will display a `console.log(this.rating)`

3. Use `TheForm` component in `App.vue`.

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
