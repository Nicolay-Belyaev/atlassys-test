<script setup>
  defineProps({
    imgSrc: {
      type: String,
      required: true
    },
    width: {
      type: [Number, String],
    },
    height: {
      type: [Number, String],
    },
  })
</script>

<template>
  <img class="avatar"
       :width="width"
       :height="height"
       :src="imgSrc"
       alt="no image found">
</template>

<style scoped>
  .avatar {
    border-radius: 100%;
  }
</style>
