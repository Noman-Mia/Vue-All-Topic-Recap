3. Attribute Bindings
```vue
<template>
   <img v-bind:src="imgURL">
</template>
<script setup>
  const imgURL = 'https://laravel.com/img/logomark.min.svg';
</script>
```