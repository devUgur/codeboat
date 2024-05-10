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
  <div class="fixed top-0 h-screen w-full bg-opacity-90 backdrop-blur-sm">
    <div class="flex h-24 place-items-center items-center justify-between lg:justify-center">
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
    <div class="bg-slate-500" :class="{'full-open': dropdownIsOpen}">
      <div id="dropdown" :class="{'open': dropdownIsOpen}" class="bg-red-200">
      {{ dropdownContent }}
    </div>
    <div v-if="dropdownIsOpen" class="h-full bg-red-500"  @mouseenter="dropdownIsOpen = false"></div>
  </div>
</div>
</template>
 

<style scoped>
#dropdown{
  height: 0vh;
  transition: height 0.5s;
  overflow: hidden
}
.full-open{
  @apply h-full;
}
.open{
  height: 50vh !important;
}
</style>
 