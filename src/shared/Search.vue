<script setup xmlns="http://www.w3.org/1999/html">

import BaseIcon from "@/shared/BaseIcon.vue";
import Magglass from "@/assets/icons/header/magglass.vue";
</script>

<template>
  <div class="search__wrapper">
    <BaseIcon icon-color="red" width="20" height="20" icon-name="magglass">
      <magglass/>
    </BaseIcon>
    <input class="search__input" placeholder="Search for something">
  </div>
</template>

<style scoped>
  .search__wrapper {
    width: 235px;
    height: 50px;
    background: #F5F7FA;
    border-radius: 40px;
    display: flex;
    align-items: center;
    padding-left: 20px;
    gap: 20px;
    @media screen and (max-width: 375px){
      width: 375px;
      margin-bottom: 20px;
    }
  }
  .search__input {
    border:none;
    background:none;
    outline:none;
    padding:0;

    font-family: Inter,serif;
    font-size: 15px;
    font-weight: 400;
    line-height: 18px;
    text-align: left;
    color: #8BA3CB;

    ::placeholder {
      color: #8BA3CB;
    }
  }
</style>
