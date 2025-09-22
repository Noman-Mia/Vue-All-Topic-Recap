
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

4. JavaScript Expressions
```vue
<template>
    {{number1+number2}}
</template>
<script setup>
const number1 = 5;
const number2 = 10;
</script>
```

5. v-bind: Bind an Attribute to an Expression
```vue
<template>
   <img v-bind:src="imgURL">
</template>
<script setup>
  const imgURL = 'https://laravel.com/img/logomark.min.svg';
</script>
```

6. v-model: Two-Way Binding for Form Inputs
```vue
<template>
    <input v-model="name" type="text" placeholder="Enter your name">
    <p>{{name}}</p>
</template>

<script setup>
import {ref} from "vue";
const name = ref('');
</scrip


7. v-if: Conditionally Render Elements
```vue
<template>
    <h1 v-if="isLogin">Welcome back</h1>
</template>
<script setup>
    const isLogin=false
</script>
```

8. v-else: Used with v-if to Display Content
```vue
<template>
    <h1 v-if="isLogin">Welcome back</h1>
    <h1 v-else>Please Login</h1>
</template>

<script setup>
    const isLogin=true
</script>
```

9. v-else-if: Adds Additional Conditional Renderings
```vue
<template>
  <h1 v-if="marks<=100 && marks>=80">A+</h1>
  <h1 v-else-if="marks<80 && marks>=70">A</h1>
  <h1 v-else-if="marks<70 && marks>=60">A</h1>
  <h1 v-else>Please Login</h1>
</template>

<script setup>
  const marks =75
</script>
```

10. v-show: Toggles Element Visibility via CSS Display
```vue
<template>
  <h1 v-show="isVisible">This is text</h1>
</template>

<script setup>
  const isVisible=true
</script>
```


11. v-for: Render a List of Elements by Iterating
```vue
<template>
    <ul>
      <li v-for="(item,index) in fruits">{{item}}</li>
    </ul>
</template>
<script setup>
  const fruits = ['Apple', 'Banana', 'Cherry'];
</script>
```

12. submit 
```vue
<template>
  <form @submit.prevent="handleSubmit">
    <input type="text" v-model="name" placeholder="Enter your name" />
    <button type="submit">Submit</button>
    <br>
    <p>{{ name }}</p>
  </form>
</template>

<script setup>
import { ref } from "vue";
  const name = ref("");

  function handleSubmit(){
    alert(`Submitted Name: ${name.value}`);
  }
</script>
```

13.Declaring Reactive State ref()
```vue
<template>
<button @click="increment">increment</button>
<button @click="decrement">decrement</button>
<p>{{ count}}</p>
</template>

<script setup>
import {ref} from "vue";
const count = ref(0);

function increment() {
  count.value ++
}
function decrement() {
  count.value --
}
</script>
```

14.Declaring Reactive State reactive()
```vue
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
```

15.Computed properties
```vue
<template>
  <p>Computed: {{ fullName }}</p>
  <p>Method: {{ getFullName() }}</p>
</template>

<script setup>
import { ref, computed } from "vue";

const firstName = ref("John");
const lastName = ref("Doe");

// Computed Property (Cache হয়)
const fullName = computed(() => {
  console.log("Computed Property Called");
  return firstName.value + " " + lastName.value;
});

// Method (প্রতিবার নতুনভাবে রান হয়)
const getFullName = () => {
  console.log("Method Called");
  return firstName.value + " " + lastName.value;
};
</script>
```

16.1.Template Syntax
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

4. JavaScript Expressions
```vue
<template>
    {{number1+number2}}
</template>
<script setup>
const number1 = 5;
const number2 = 10;
</script>
```

5. v-bind: Bind an Attribute to an Expression
```vue
<template>
   <img v-bind:src="imgURL">
</template>
<script setup>
  const imgURL = 'https://laravel.com/img/logomark.min.svg';
</script>
```

6. v-model: Two-Way Binding for Form Inputs
```vue
<template>
    <input v-model="name" type="text" placeholder="Enter your name">
    <p>{{name}}</p>
</template>

<script setup>
import {ref} from "vue";
const name = ref('');
</scrip


7. v-if: Conditionally Render Elements
```vue
<template>
    <h1 v-if="isLogin">Welcome back</h1>
</template>
<script setup>
    const isLogin=false
</script>
```

8. v-else: Used with v-if to Display Content
```vue
<template>
    <h1 v-if="isLogin">Welcome back</h1>
    <h1 v-else>Please Login</h1>
</template>

<script setup>
    const isLogin=true
</script>
```

9. v-else-if: Adds Additional Conditional Renderings
```vue
<template>
  <h1 v-if="marks<=100 && marks>=80">A+</h1>
  <h1 v-else-if="marks<80 && marks>=70">A</h1>
  <h1 v-else-if="marks<70 && marks>=60">A</h1>
  <h1 v-else>Please Login</h1>
</template>

<script setup>
  const marks =75
</script>
```

10. v-show: Toggles Element Visibility via CSS Display
```vue
<template>
  <h1 v-show="isVisible">This is text</h1>
</template>

<script setup>
  const isVisible=true
</script>
```


11. v-for: Render a List of Elements by Iterating
```vue
<template>
    <ul>
      <li v-for="(item,index) in fruits">{{item}}</li>
    </ul>
</template>
<script setup>
  const fruits = ['Apple', 'Banana', 'Cherry'];
</script>
```

12. submit 
```vue
<template>
  <form @submit.prevent="handleSubmit">
    <input type="text" v-model="name" placeholder="Enter your name" />
    <button type="submit">Submit</button>
    <br>
    <p>{{ name }}</p>
  </form>
</template>

<script setup>
import { ref } from "vue";
  const name = ref("");

  function handleSubmit(){
    alert(`Submitted Name: ${name.value}`);
  }
</script>
```

13.Declaring Reactive State ref()
```vue
<template>
<button @click="increment">increment</button>
<button @click="decrement">decrement</button>
<p>{{ count}}</p>
</template>

<script setup>
import {ref} from "vue";
const count = ref(0);

function increment() {
  count.value ++
}
function decrement() {
  count.value --
}
</script>
```

14.Declaring Reactive State reactive()
```vue
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
```

15.Computed properties
```vue
<template>
  <p>Computed: {{ fullName }}</p>
  <p>Method: {{ getFullName() }}</p>
</template>

<script setup>
import { ref, computed } from "vue";

const firstName = ref("John");
const lastName = ref("Doe");

// Computed Property (Cache হয়)
const fullName = computed(() => {
  console.log("Computed Property Called");
  return firstName.value + " " + lastName.value;
});

// Method (প্রতিবার নতুনভাবে রান হয়)
const getFullName = () => {
  console.log("Method Called");
  return firstName.value + " " + lastName.value;
};
</script>
```


16.Props define
---------------------------------------
---Child Component → UserCard.vue
<script setup>
const props = defineProps({
  name: {
    type: String,
    required: true
  },
  age: {
    type: Number,
    default: 18
  },
  skills: {
    type: Array,
    default: () => []
  }
});
</script>

<template>
  <div class="p-4 border rounded">
    <h2>{{ props.name }}</h2>
    <p>Age: {{ props.age }}</p>
    <h3>Skills:</h3>
    <ul>
      <li v-for="(skill, i) in props.skills" :key="i">{{ skill }}</li>
    </ul>
  </div>
</template>

----Parent Component → App.vue
<script setup>
import UserCard from './UserCard.vue';

const user = {
  name: "Noman",
  age: 21,
  skills: ["Vue.js", "Laravel", "Tailwind CSS"]
};
</script>

<template>
  <UserCard :name="user.name" :age="user.age" :skills="user.skills" />
</template>
------------------------------------------------------------------------------
