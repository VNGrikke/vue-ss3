<template>
  <div>
    <h1 :id="elementId" :class="elementClass">Heading</h1>
  </div>
</template>

<script setup>
  const elementId = 'heading-id';      
  const elementClass = 'heading main';  
</script>

<style>
  #heading-id {
    color: red;
  }

  .heading {
    font-size: 24px;
  }

  .main {
    text-transform: uppercase;
  }
</style>
