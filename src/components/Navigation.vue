<script setup>

import BaseButton from "@/shared/BaseButton.vue";
import BaseIcon from "@/shared/BaseIcon.vue";
import Home from "@/assets/icons/navigation/home.vue";
import Accounts from "@/assets/icons/navigation/accounts.vue";
import Investments from "@/assets/icons/navigation/investments.vue";
import Cards from "@/assets/icons/navigation/cards.vue";
import Loans from "@/assets/icons/navigation/loans.vue";
import Services from "@/assets/icons/navigation/services.vue";
import Privileges from "@/assets/icons/navigation/privileges.vue";
import Transactions from "@/assets/icons/navigation/transactions.vue";
import Settings from "@/assets/icons/navigation/settings.vue";
import Logo from "@/assets/icons/navigation/logo.vue";
</script>

<template>
<!--  По хорошему, кнопки должны рисоваться отдельным компонентом, получающим через пропсы список названий и иконок.-->
<!--  Такой компонент знает, в частности, какая кнопка нажата и соответственно управляет стилями.-->
<!--  Времени нет написать, на рефакторинге переделаю =).-->
  <section class="navigation">
    <div class="nav-logo">
      <BaseIcon width="36" height="36>">
        <logo/>
      </BaseIcon>
      <span class="logo_text">BankDash.</span>
    </div>
    <div class="nav-buttons">
      <BaseButton form="nav-form" color="nav-color_grey">
        <div class="nav-button_content">
          <BaseIcon width="25" height="25"><home/></BaseIcon>
          Dashboard
        </div>
      </BaseButton>

      <BaseButton form="nav-form" color="nav-color_grey">
        <div class="nav-button_content">
          <BaseIcon width="25" height="25"><transactions/></BaseIcon>
          Transactions
        </div>
      </BaseButton>

      <BaseButton form="nav-form" color="nav-color_grey">
        <div class="nav-button_content">
          <BaseIcon width="25" height="25"><accounts/></BaseIcon>
          Accounts
        </div>
      </BaseButton>

      <BaseButton form="nav-form" color="nav-color_grey">
        <div class="nav-button_content">
          <BaseIcon width="25" height="25"><investments/></BaseIcon>
          Investments
        </div>
      </BaseButton>

      <BaseButton form="nav-form" color="nav-color_grey">
        <div class="nav-button_content">
          <BaseIcon width="25" height="25"><cards/></BaseIcon>
          Credit Cards
        </div>
      </BaseButton>

      <BaseButton form="nav-form" color="nav-color_grey">
        <div class="nav-button_content">
          <BaseIcon width="25" height="25"><loans/></BaseIcon>
          Loans
        </div>
      </BaseButton>

      <BaseButton form="nav-form" color="nav-color_grey">
        <div class="nav-button_content">
          <BaseIcon width="25" height="25"><services/></BaseIcon>
          Services
        </div>
      </BaseButton>

      <BaseButton form="nav-form" color="nav-color_grey">
        <div class="nav-button_content">
          <BaseIcon width="25" height="25"><privileges/></BaseIcon>
          My Privileges
        </div>
      </BaseButton>

      <BaseButton form="nav-form" color="nav-color_blue">
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
  width: 300px;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 60px;
}
.nav-logo {
  font-family: Mont,serif;
  font-size: 25px;
  font-weight: 900;
  line-height: 32px;
  text-align: left;
  color: #343C6A;

  height: 36px;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 9px;
}

.nav-buttons {
  width: 270px;
  display: flex;
  flex-direction: column;
  gap: 40px;
}

.nav-button_content {
  width: 60%;
  display: flex;
  align-items: center;
  justify-content: flex-start;
  gap: 26px;
}
.button__nav-form {
  height: 32px;
  font-family: Inter,serif;
  font-size: 18px;
  font-weight: 500;
  line-height: 22px;
  justify-content: center;

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
