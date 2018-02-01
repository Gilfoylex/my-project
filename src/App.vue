<template>
  <div id="app">
    <head-layout>
      <head-nav></head-nav>
    </head-layout>
    <main-layout>
    </main-layout>
  </div>
</template>

<script>
import HeadNav from "./components/HeadNav.vue";
import HeadLayout from './layouts/HeadLayout.vue'
import MainLayout from './layouts/MainLayout.vue'

export default {
  name: "App",
  components: {
    HeadNav,
    HeadLayout,
    MainLayout
  }
};
</script>

<style scoped>
</style>
