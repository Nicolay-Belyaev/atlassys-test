<script setup>

import Headline from "@/components/Headline.vue";
import Navigation from "@/components/Navigation.vue";
import Settings from "@/components/Settings.vue";
</script>

<template>
  <Headline header="Setting" class="header" avatar="src/assets/images/photo.jpeg"/>
  <Navigation class="nav"/>
  <Settings class="content"/>

</template>

<style scoped>
  .header {
    grid-area: header;
  }
  .nav {
    grid-area: navigation;
  }
  .content {
    grid-area: content
  }
</style>
