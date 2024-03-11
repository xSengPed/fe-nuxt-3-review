<template>
  <div>
    <p>REF With Value</p>
    <p>Count is: {{ countRef }}</p>
    <button @click="increment">Increment</button>
    <p>
      {{ person.name }}
      {{ person.age }}
      <button class="btn" @click="ageUp">Age Up</button>
    </p>
  </div>
</template>

<script lang="ts" setup>

// Example 
// Ref : Use with value 
// Reactive : Use with object to emit the state change

interface Person {
  name: string
  age: number

}

const countRef = ref(0)
const person = reactive<Person>({ age: 0, name: 'John' })


const ageUp = () => {
  person.age++
}
const increment = () => {
  countRef.value++
}
</script>

<style></style>