<script setup>
  import BaseButton from "@/shared/BaseButton.vue";
  import Search from "@/shared/Search.vue";
  import Avatar from "@/shared/Avatar.vue";
  import Gear from "@/assets/icons/header/gear.vue";
  import BaseIcon from "@/shared/BaseIcon.vue";
  import Bell from "@/assets/icons/header/bell.vue";

  defineProps({
    header: {
      type: String,
      default: "Check Header Props",
      required: true
    },
    avatar: {
      type: String,
      default: '@/assets/images/photo.jpeg',
      required: true
    }
  })

</script>

<template>
  <div class="header">
    <span class="header-name">{{ header }}</span>
    <div class="header-controls">

      <Search/>
      <BaseButton form="header-form" color="header-color">
        <BaseIcon height="25" width="25" icon-name="gear">
          <gear/>
        </BaseIcon>
      </BaseButton>
      <BaseButton form="header-form" color="header-color">
        <BaseIcon height="25" width="25" icon-name="bell">
          <bell/>
        </BaseIcon>
      </BaseButton>
      <Avatar class="header-avatar" width="60" height="60" :img-src="avatar"/>
    </div>
  </div>

</template>

<style scoped>
.header {
  display: flex;
  align-items: center;
  gap: 30px;
  justify-content: space-between;
  border-bottom: 1px solid #E6EFF5;
  padding: 0 20px 0 20px;
  background: #FFF;
  @media screen and (max-width: 375px){
    flex-direction: column;
    gap: 0;
  }
}
.header-name {
  font-family: Inter,serif;
  font-size: 28px;
  font-weight: 600;
  line-height: 34px;
  text-align: left;
  color: #343C6A;
  @media screen and (max-width: 375px){
    margin-top: 19px;
  }
}
.header-controls {
  display: flex;
  align-items: center;
  gap: 30px;
}
.header-avatar {
  @media screen and (max-width: 375px){
    position: absolute;
    zoom: 0.6;
    top: 30px;
    left: 650px;
  }
}

.button__header-form {
  height: 50px;
  width: 50px;
  border-radius: 50px;

  display: flex;
  align-items: center;
  justify-content: center;
  border: none;
  @media screen and (max-width: 375px){
    display: none;
  }
}

.button__header-color {
  background: #F5F7FA;
}

</style>
