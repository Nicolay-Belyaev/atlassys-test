<script setup>

import BaseButton from "@/shared/BaseButton.vue";
import BaseIcon from "@/shared/BaseIcon.vue";
import Home from "@/assets/icons/navigation/home-icon.vue";
import Accounts from "@/assets/icons/navigation/accounts-icon.vue";
import Investments from "@/assets/icons/navigation/investments-icon.vue";
import Cards from "@/assets/icons/navigation/cards-icon.vue";
import Loans from "@/assets/icons/navigation/loans-icon.vue";
import Services from "@/assets/icons/navigation/services-icon.vue";
import Privileges from "@/assets/icons/navigation/privileges-icon.vue";
import Transactions from "@/assets/icons/navigation/transactions-icon.vue";
import Settings from "@/assets/icons/navigation/settings-icon.vue";
</script>

<template>
<!--  TODO: Кнопки должны рисоваться отдельным компонентом, получающим через пропсы список названий и иконок. Такой компонент знает, в частности, какая кнопка нажата и соответственно управляет стилями.-->
  <section class="navigation">
    <div class="nav-logo">
      <img width="36" height="36" src="../assets/images/logo.png" alt="no logo pic found">
      <span class="logo_text">BankDash.</span>
    </div>
    <div class="nav-buttons">
      <BaseButton form="nav-form" color="nav-color_grey">
        <div class="nav-button-marker"></div>
        <div class="nav-button_content">
          <BaseIcon width="25" height="25"><home/></BaseIcon>
          Dashboard
        </div>
      </BaseButton>

      <BaseButton form="nav-form" color="nav-color_grey">
        <div class="nav-button-marker"></div>
        <div class="nav-button_content">
          <BaseIcon width="25" height="25"><transactions/></BaseIcon>
          Transactions
        </div>
      </BaseButton>

      <BaseButton form="nav-form" color="nav-color_grey">
        <div class="nav-button-marker"></div>
        <div class="nav-button_content">
          <BaseIcon width="25" height="25"><accounts/></BaseIcon>
          Accounts
        </div>
      </BaseButton>

      <BaseButton form="nav-form" color="nav-color_grey">
        <div class="nav-button-marker"></div>
        <div class="nav-button_content">
          <BaseIcon width="25" height="25"><investments/></BaseIcon>
          Investments
        </div>
      </BaseButton>

      <BaseButton form="nav-form" color="nav-color_grey">
        <div class="nav-button-marker"></div>
        <div class="nav-button_content">
          <BaseIcon width="25" height="25"><cards/></BaseIcon>
          Credit Cards
        </div>
      </BaseButton>

      <BaseButton form="nav-form" color="nav-color_grey">
        <div class="nav-button-marker"></div>
        <div class="nav-button_content">
          <BaseIcon width="25" height="25"><loans/></BaseIcon>
          Loans
        </div>
      </BaseButton>

      <BaseButton form="nav-form" color="nav-color_grey">
        <div class="nav-button-marker"></div>
        <div class="nav-button_content">
          <BaseIcon width="25" height="25"><services/></BaseIcon>
          Services
        </div>
      </BaseButton>

      <BaseButton form="nav-form" color="nav-color_grey">
        <div class="nav-button-marker"></div>
        <div class="nav-button_content">
          <BaseIcon width="25" height="25"><privileges/></BaseIcon>
          My Privileges
        </div>
      </BaseButton>

      <BaseButton form="nav-form" color="nav-color_blue">
        <div class="nav-button-marker make_blue"></div>
        <div class="nav-button_content">
          <BaseIcon width="25" height="25"><settings/></BaseIcon>
          Setting
        </div>
      </BaseButton>
    </div>
  </section>
</template>

<style scoped>
.navigation {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 31px;
  border-right: 1px solid #E6EFF5;
  height: 100vh;
  background: #FFF;
}
.nav-logo {
  font-family: Mont,serif;
  font-size: 25px;
  font-weight: 900;
  line-height: 32px;
  text-align: left;
  color: #343C6A;

  height: 100px;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 9px;
}

.nav-buttons {
  width: 219px;
  display: flex;
  flex-direction: column;
}

.nav-button_content {
  width: 80%;
  display: flex;
  align-items: center;
  justify-content: flex-start;
  gap: 26px;
}

.nav-button-marker {
  height: 60px;
  width: 6px;
  border-top-right-radius: 10px;
  border-bottom-right-radius: 10px;
}

.make_blue {
  background: #1814F3;
}

.button__nav-form {
  height: 60px;
  font-family: Inter,serif;
  font-size: 18px;
  font-weight: 500;
  line-height: 22px;
  justify-content: left;
  gap: 22px;

  display: flex;
  align-items: center;
  border: none;
}

.button__nav-color_grey {
  color: #B1B1B1;
  background: white;
}

.button__nav-color_blue {
  color: #1814F3;
  background: white;
}
</style>
