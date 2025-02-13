<template>
  <div v-for="(member, index) in members" :key="index">
    <p>Name: {{ member.name }} And Age:{{ member.age }}</p>
  </div>

    <h1>simple way</h1>
  <p>Name: {{ members[1].name }} And Age: {{ members[1].age }}</p>
</template>

<script setup>
import { reactive } from "vue";

const members = reactive([
  { name: "John", age: 23 },
  { name: "Khan", age: 22 },
  { name: "Joh", age: 20 }
]);
</script>

