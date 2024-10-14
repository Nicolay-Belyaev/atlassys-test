<script setup>

import Headline from "@/components/Headline.vue";
import Navigation from "@/components/Navigation.vue";
import EditProfile from "@/components/EditProfile.vue";
</script>

<template>
  <section class="setting">
    <Headline header="Setting" class="header" avatar="src/assets/images/photo.jpeg"/>
    <Navigation class="nav"/>
    <EditProfile class="content" avatar="src/assets/images/photo.jpeg"/>
  </section>

</template>

<style scoped>
  .setting {
    display: grid;
    grid-template-columns: 220px 1fr ;
    grid-template-rows: 100px 1fr;
    grid-template-areas:
            "navigation header"
            "navigation content";
    @media screen and (max-width: 375px){
      grid-template-areas:
            "header"
            "content";
      grid-template-columns: 1fr;
      grid-template-rows: 140px 1fr;
    }

  }
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
