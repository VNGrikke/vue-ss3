<template>
  <div>
    <input type="text" :disabled="isDisabled">
    <button @click="handleClick">disabled = {{ isDisabled }}</button>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const isDisabled = ref(true);

const handleClick = () => {
  isDisabled.value = !isDisabled.value;
};
</script>

<style>
</style>
