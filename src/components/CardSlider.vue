<template>
    <div id="card-slider" class="p-10 bg-black w-full h-screen">
       <div class="bg-white h-[] p-10 flex flex-col md:flex-row ">
        <ABaseContactCard :full-name="'Nenad Kalicanin'" :title="'Title'" :img-src="image" />
        <ABaseContactCard :full-name="'Nenad Kalicanin'" :title="'Title'" :img-src="image" />
        <ABaseContactCard :full-name="'Nenad Kalicanin'" :title="'Title'" :img-src="image" />
        <ABaseContactCard :full-name="'Nenad Kalicanin'" :title="'Title'" :img-src="image" />
       </div> 
    </div>
</template>

<script setup lang="ts">
import image from "@/assets/SOP/milan_web.jpg"
import ABaseContactCard from '@/components/neno/atoms/cards/ABaseContactCard.vue';
import HomeIntroComponent from '@/components/home/HomeIntroComponent.vue'
</script>

<style  scoped>
 </style>