<script setup lang="ts">
import { ref } from 'vue';
const props = defineProps(["links", ""]);

import MainLinks from "@/assets/json/MainLinks.json"


const dropdownIsOpen = ref(false);
const dropdownContent = ref<any>()
const handleDropdown = function(dropdown: any){
  dropdownIsOpen.value = true;
  dropdownContent.value = dropdown;
  console.log(dropdown);
}
</script>


<template>
  <div class="fixed top-0  w-full bg-opacity-90" :class="{'full-open':dropdownIsOpen}" @mouseleave="dropdownIsOpen = false">
    <div class="flex bg-white h-24 place-items-center items-center justify-between lg:justify-center">
      <div class="mr-6 text-xl"> Logo </div>
         <div class="hidden lg:flex space-x-10 text-xs text-black">
           <div v-for="link in MainLinks" :key="link.name" @mouseenter="handleDropdown(link)" class="">{{ link.name }}</div>
         </div>
         <div class="ml-6 flex space-x-0 lg:space-x-2">
           <div class='flex lg:hidden'>
            hello
           </div>
         </div>
    </div>
    <div class="" :class="{'full-open': dropdownIsOpen}">
      <div id="dropdown" :class="{'open': dropdownIsOpen}" class="bg-white">
      {{ dropdownContent }}
    </div>
    <div v-if="dropdownIsOpen" class="h-full backdrop-blur-sm"  @mouseenter="dropdownIsOpen = false"></div>
  </div>
</div>
</template>
 

<style scoped>
#dropdown{
  height: 0vh;
  transition: height 0.3s;
  overflow: hidden
}
.full-open{
  @apply h-full;
}
.open{
  height: 50vh !important;
}
</style>
 