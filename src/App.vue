<script setup>
import { ref } from "vue";
  const images =[
    "https://images.pexels.com/photos/18840507/pexels-photo-18840507/free-photo-of-vasco-da-gama-bridge-at-sunset.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1",
    "https://images.pexels.com/photos/14298131/pexels-photo-14298131.jpeg?auto=compress&cs=tinysrgb&w=600&lazy=load",
    "https://images.pexels.com/photos/13919952/pexels-photo-13919952.jpeg?auto=compress&cs=tinysrgb&w=600&lazy=load",
    "https://images.pexels.com/photos/19737002/pexels-photo-19737002/free-photo-of-stairs.jpeg?auto=compress&cs=tinysrgb&w=600&lazy=load",
    "https://images.pexels.com/photos/18111144/pexels-photo-18111144/free-photo-of-equipment-of-a-painter.jpeg?auto=compress&cs=tinysrgb&w=600&lazy=load"
  ]
  const fullImage = ref(0);
</script>

<template>
  <section class="container mx-auto flex items-center flex-col">
    <h1 class="text-center text-2xl py-10">Events & Reactivity</h1>
    <div>
      <div class="flex space-x-2">
        <template v-for="(image, index) in images" :key="index">
        <img class="cursor-pointer w-40" :src="image" @click="fullImage = index">
      </template>
      </div>
      <div class="mt-10">
        <img class="cursor-pointer w-full" :src="images[fullImage]">
      </div>
    </div>
  </section>
</template>

<style scoped>

</style>
