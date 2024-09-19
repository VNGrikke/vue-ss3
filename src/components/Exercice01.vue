<template>
  <div>
    <img v-bind:src="urlImage" v-bind:class="{ widthImage }" alt="anh cam" />
  </div>
</template>

<script setup>
const urlImage =
  "https://img.meta.com.vn/Data/image/2021/09/22/anh-meo-cute-de-thuong-dang-yeu-42.jpg";
const widthImage = "widthImage";
</script>

<style>
.widthImage {
  width: 100px;
}
</style>
