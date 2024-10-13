<script setup>

import ProfileEditForm from "@/components/ProfileEditForm.vue";
import Avatar from "@/shared/Avatar.vue";
import BaseButton from "@/shared/BaseButton.vue";

defineProps({
  avatar: {
    type: String,
    default: '@/assets/images/photo.jpeg',
    required: true
  }
})
</script>

<template>
  <section class="profile-wrapper">
    <div class="profile-buttons">
<!--  TODO: Как и в навигации, набор кнопок нужно вынести в отдельный компонент, управляющий стилями и, собственно, переключающий вкладки-->
      <BaseButton form="profile-form" color="profile-color">
        <span class="profile-button-content_blue">Edit Profile</span>
        <div class="profile-button-marker profile-button-marker_blue"></div>
      </BaseButton >
      <BaseButton form="profile-form" color="profile-color">
        <span class="profile-button-content">Preferences</span>
        <div class="profile-button-marker"></div>
      </BaseButton>
      <BaseButton form="profile-form" color="profile-color">
        <span class="profile-button-content">Security</span>
        <div class="profile-button-marker"></div>
      </BaseButton>
    </div>
    <Avatar width="130" height="130" :img-src="avatar">
      <img src="@/assets/images/pen.png" alt="pen" class="profile-change-photo">
    </Avatar>
    <ProfileEditForm class="profile-form"/>
  </section>
</template>

<style scoped lang="scss">
 .profile-wrapper {
   background: #FFF;
   height: 717px;
   @media screen and (max-width: 1330px){
     height: 1180px;
   }
   margin: 31px 40px 0 40px;
   padding: 37px 30px;
   border-radius: 25px;

   display: grid;
   grid-template-columns: 185px 1fr;
   grid-template-rows: 85px 1fr;
   grid-template-areas:
      "controls controls"
      "avatar form";
 }
 .profile-form {
   grid-area: form;
 }
 .profile-buttons {
   grid-area: controls;
   height: 30px;
   border-bottom: 1px solid #F4F5F7;
   display: flex;
   gap: 20px;
 }

 .profile-button-content {
   font-family: Inter,serif;
   font-size: 16px;
   font-weight: 500;
   line-height: 20px;
   text-align: center;
   color: #718EBF;

   &_blue {
     color: #1814F3;
   }
 }

 .profile-button-marker {
   width: 114px;
   height: 3px;
   top: 2px;
   &_blue {
     background: #1814F3;
     border-top-left-radius: 10px;
     border-top-right-radius: 10px;
     position: relative;
   }
 }

 .profile-change-photo {
   height: 32px;
   width: 32px;
   position: relative;
   right: 30px;
   bottom: 10px;
 }

.button__profile-form {
  width: 114px;
  border: none;
  height: 30px;

  font-family: Inter,serif;
  font-size: 16px;
  font-weight: 500;
  line-height: 20px;
  text-align: center;

  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: flex-end;
  gap: 3px;
}

 .button__profile-color {
   background: white;
 }
</style>
