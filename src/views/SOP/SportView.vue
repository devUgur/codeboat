<template>
<ScrollFullPageSideIndex :side-list="sideList" :section-contents="sideList" />
  <ABaseHorizontalSection :content="'Home | Sport'" />
</template>

<script setup lang="ts">
import ABaseHorizontalSection from '@/components/atoms/sections/ABaseHorizontalSection.vue';
import ScrollFullPageSideIndex from '@/components/neno/ScrollFullPageSideIndex.vue';
const sideList = ["asdf", "asdf", "asdf", "asdf", "asdf", "asdf"]

</script>

<style scoped></style>
