<template>
  <div>
    <a href="https://www.google.com" @click.prevent="checkLink">Go to Google</a>
    <br>
    <a href="ht://www.google.com" @click.prevent="checkLink">Go to Google</a>
  </div>
</template>

<script setup>
const checkLink = (event) => {
  const url = event.target.href;
  
  if (!url.startsWith('https://')) {
    alert('Đường dẫn không hợp lệ');
  } else {
    window.location.href = url;
  }
};
</script>

<style>
</style>
