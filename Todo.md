1.Template Syntax
```vue
<script setup>
const name = "rahim";
</script>

<template>
  <p>Name: {{ name }}</p>
</template>
```

2. Raw HTML
```vue
<template>
  <p> this is not work :{{ rawHtml }}</p>
  <div v-html="rawHtml"></div>
</template>

<script setup>
const rawHtml = '<span style="color: red;">This is red text</span>';
</script>
```

3. Attribute Bindings
```vue
<template>
   <img v-bind:src="imgURL">
</template>
<script setup>
  const imgURL = 'https://laravel.com/img/logomark.min.svg';
</script>
```