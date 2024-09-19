<template>
  <div>
    <form @submit.prevent="handleSubmit">
      <input type="text" v-model="inputValue" />
      <button type="submit">Submit</button>
    </form>
  </div>
</template>

<script setup>
import { ref } from 'vue';
const inputValue = ref('');

const handleSubmit = () => {
  console.log('Form submission prevented!');
};
</script>

<style>

</style>
