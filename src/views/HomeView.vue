<script setup lang="ts">
import img from '../assets/store-card-40-ipad-air-202405.jpeg'
const images = [img, img, img]

</script>
<template>
  <div id="home-view">
    <div class="px-7">
      <h1 class="font-bold text-2xl">Gerade erst vorgestellt</h1>
      <h1 class="text-gray-600 text-opacity-50 text-xl">Sieh dir jetzt an, was es Neues gibt.</h1>
    </div>
    <div id="image-card">
      <div class="flex flex-row px-6 py-2 gap-4 rounded">
          <img v-for="img in images" class="rounded-xl shadow-xl" :src="img" alt="img" :key="img" />
          <div class="slideButton bg-black w-[100px] h-[100px] rounded-full">
            >asdfasdf
          </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
* {
  margin: 0.5rem auto;
}
h1 {
  margin: 0;
}
#home-view {
  height: 200vh;
}
.slideButton {
    position:inherit;
    right:0;
}
</style>
