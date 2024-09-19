<template>
  <div>
    <input
      type="text"
      v-model="inputValue"
      @keydown="handleKeydown"
      ref="inputRef"
    />
  </div>
</template>

<script setup>
import { ref } from "vue";

const inputValue = ref("");
const inputRef = ref(null);

const handleKeydown = (event) => {
  if (event.key === "Enter" && event.shiftKey) {
    alert(inputValue.value);

    inputValue.value = "";

    inputRef.value.focus();
  } else if (event.key === "Enter") {
    alert("Bạn cần nhấn Shift + Enter");
  }
};
</script>

<style>
input {
  padding: 8px;
  font-size: 16px;
  width: 300px;
  margin: 10px 0;
}
</style>
