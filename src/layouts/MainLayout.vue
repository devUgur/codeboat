<script setup lang="ts">
import  { RouterView } from "vue-router";
import MainTopnavComponent from "@/components/navs/MainTopnavComponent.vue";

</script>

<template>
    <div id="main-layout">
        <MainTopnavComponent></MainTopnavComponent>
        <RouterView></RouterView>
    </div>
</template>

<style scoped>

</style>