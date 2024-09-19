<template>
  <div>
    <img v-bind:src="urlImage" v-bind:class="{ widthImage }" alt="anh meo" />
    <button @click="changeImage">Thay ảnh</button>
  </div>
</template>

<script setup>
import { ref } from "vue";
const urlImages = [
  "https://demoda.vn/wp-content/uploads/2022/01/anh-meme-meo.jpg",
  "https://khoinguonsangtao.vn/wp-content/uploads/2022/08/anh-meme-meo-cute-trai-tim.jpg",
  "https://i.pinimg.com/originals/68/54/1d/68541d965a060d7a6c2e8957f999cc17.jpg",
  "https://tse3.mm.bing.net/th?id=OIP.F9sw9swPs1VRLO9316OEsQHaGP&pid=Api&P=0&h=220",
];

const urlImage = ref(
  "https://demoda.vn/wp-content/uploads/2022/01/anh-meme-meo.jpg"
);

const changeImage = () => {
  urlImage.value = urlImages[Math.floor(Math.random() * urlImages.length)];
};

const widthImage = "widthImage";
</script>

<style>
.widthImage {
  width: 100px;
}
</style>