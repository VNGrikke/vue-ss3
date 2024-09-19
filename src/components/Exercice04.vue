<template>
  <div>
    <div
      v-bind:class="{ active: isActive }"
      v-bind:style="{ backgroundColor: backgroundColor }"
      class="block"
    >
      Block
    </div>
    <p>isActive = {{ isActive }}</p>
    <button @click="toggleActive">Toggle Active</button>
    <button @click="changeColor">Change Color</button>
  </div>
</template>

<script setup>
import { ref } from "vue";

const isActive = ref(true);
const backgroundColor = ref("blue");

const toggleActive = () => {
  isActive.value = !isActive.value;
};

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
