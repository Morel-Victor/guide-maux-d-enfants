<template>
  <q-layout view="hHh lpR fFf">

    <NavBar />

    <q-page-container class="no-padding absolute-full">
      <router-view v-slot="{ Component }">
         <component :is="Component" />
      </router-view>
    </q-page-container>
  </q-layout>
</template>

<script>
export default {
  name: 'main-layout',
};
</script>
<script setup>
import NavBar from 'components/NavBar.vue';
// function goTop() {
//  window.scrollTo({ top: 0, behavior: 'smooth' });
// }
</script>

<style scoped>
</style>
