<template>
<button @click="clickButton">click : {{count}} lần</button>
  
</template>

<script setup>
import {ref} from 'vue'

const count = ref(0)

const clickButton = () => {
  count.value++
}

</script>

<style>

</style>