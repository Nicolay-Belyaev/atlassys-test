<script setup>
  defineProps({
    width: {
      type: [Number, String],
    },
    height: {
      type: [Number, String],
    },
  })
</script>

<template>
<!--  div работает якорем для картинки с на страничке Edit Profile у которой relative позиция-->
  <div :style="{width: width, height: height}">
    <img class="avatar"
         :width="width"
         :height="height"
         src="@/assets/images/photo.png"
         alt="no image found">
    <slot/>
  </div>

</template>

<style scoped>
  .avatar {
    border-radius: 100%;
  }
</style>
