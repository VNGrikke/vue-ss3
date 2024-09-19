<template>
  <div>
    <div
      v-bind:style="{ backgroundColor: backgroundColor }"
      class="block"
    >
    </div>
    <button @click="changeColor">Change Color</button>
  </div>
</template>

<script setup>
import { ref } from "vue";

const backgroundColor = ref("blue");


const changeColor = () => {
  backgroundColor.value = backgroundColor.value === "blue" ? "red" : "blue";
};
</script>

<style>
.active {
  color: #fff;
}

.block {
  width: 300px;
  height: 100px;
  justify-content: center;
  text-align: center;
  line-height: 100px;
  font-size: 24px;
}
</style>
