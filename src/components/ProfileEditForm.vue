<script setup>
import BaseButton from "@/shared/BaseButton.vue";
</script>

<template>
<!--  Плейсхолдеры в форме должны заполняется данными пользователя, которые мы получаем по API, по самбмиту неизмененные
      поля подтянули бы значения плейсхолдеров для отправки данных на бэк.-->
<!--  Но API у нас нет, и фейкать его я не хочу, задание так-то на верстку было. Мне просто удобнее верстать компонентами.-->
<!--  Поэтому тут я  захардкочу значения. По той же причине на форме нет функции сабмита.-->
<form class="edit-profile-form">
<!--  Если бы это было более "серьезное" приложения, то я вынес бы инпуты в отдельный компонент. Для этого есть 3 причины:
      1. это больше соответствует компонентному подходу;
      2. в "боевом" приложении на инпутах скорее всего будет висеть функция, которая запоминает последние введенные
      пользователем данные и сохраняет их на бэке (зачем это нужно, можно обсудить на собеседовании =).
      3. их было бы попроще настраивать. Хотя с учетом интересного инпута даты, для мня задачка все равно "на подумать".
      -->

  <div class="edit-profile-input-wrapper">
    <label for="name" class="edit-profile-label">Your Name</label>
    <input class="edit-profile-input" id="name" type="text" placeholder="Charlene Reed">
  </div>

  <div class="edit-profile-input-wrapper">
    <label for="email" class="edit-profile-label">Email</label>
    <input class="edit-profile-input" id="email" type="text" placeholder="charlenereed@gmail.com">
  </div>

  <div class="edit-profile-input-wrapper">
    <label for="birthday" class="edit-profile-label">Date of Birth</label>
    <input class="edit-profile-input"
           id="birthday" name="date"
           type="text"
           onclick="(this.type='date')"
           onfocus="(this.type='date')"
           onblur="if(!this.value)this.type='text'"
           placeholder="25 January 1990">
        <img class="edit-profile-open-button" src="@/assets/images/arrow-down.png" alt="arrow-down">
  </div>

  <div class="edit-profile-input-wrapper">
    <label for="address-permanent" class="edit-profile-label">Permanent Address</label>
    <input class="edit-profile-input" id="address-permanent" type="text" placeholder="San Jose, California, USA">
  </div>

  <div class="edit-profile-input-wrapper">
    <label for="postal" class="edit-profile-label">Postal Code</label>
    <input class="edit-profile-input" id="postal" type="text" placeholder="45962">
  </div>

  <div class="edit-profile-input-wrapper">
    <label for="username" class="edit-profile-label">User Name</label>
    <input class="edit-profile-input" id="username" type="text" placeholder="Charlene Reed">
  </div>

  <div class="edit-profile-input-wrapper">
    <label for="password" class="edit-profile-label">Password</label>
    <input class="edit-profile-input" id="password" type="password" placeholder="**********">
  </div>

  <div class="edit-profile-input-wrapper">
    <label for="address-present" class="edit-profile-label">Present Address</label>
    <input class="edit-profile-input" id="address-present" type="text" placeholder="San Jose, California, USA">
  </div>

  <div class="edit-profile-input-wrapper">
    <label for="city" class="edit-profile-label">City</label>
    <input class="edit-profile-input" id="city" type="text" placeholder="San Jose">
  </div>

  <div class="edit-profile-input-wrapper">
    <label for="country" class="edit-profile-label">Country</label>
    <input class="edit-profile-input" id="country" type="text" placeholder="USA">
  </div>
  <BaseButton class="edit-profile-submit">
    Save
  </BaseButton>
</form>

</template>

<style scoped lang="scss">
  input::-webkit-calendar-picker-indicator {
    opacity: 0;
  }
  .edit-profile {
    &-form {
      display: grid;
      grid-template-columns: repeat(3, max(418px));

      height: 488px;
      gap: 22px;
      @media screen and (max-width: 1800px){
        grid-template-columns: repeat(2, max(418px));
      }
      @media screen and (max-width: 1330px){
        grid-template-columns: repeat(1, max(418px));
      }
    }
    &-input-wrapper {
      height: 80px;
      width: 418px;
      display: flex;
      flex-direction: column;
      gap: 11px;
    }
    &-input {
      height: 50px;
      border-radius: 15px;
      border: 1px solid #DFEAF2;
      padding: 16px 20px;

      font-family: Inter,serif;
      font-size: 19px;
      font-weight: 400;
      line-height: 18.15px;
      text-align: left;
    }
    &-label {
      font-family: Inter,serif;
      font-size: 19px;
      font-weight: 400;
      line-height: 19.36px;
      text-align: left;

    }
    &-open-button {
      width: 12px;
      height: 6px;
      border: none;
      background: #FFF;
      position: relative;
      left: 380px;
      bottom: 43px;
      pointer-events: none;
    }
    &-submit {
      width: 190px;
      height: 50px;
      position: relative;
      left: 670px;
      border-radius: 15px;
      background: #1814F3;
      border: none;
      
      font-family: Inter,serif;
      font-size: 18px;
      font-weight: 500;
      line-height: 21.78px;
      text-align: center;
      color: #FFF;
      margin-top: 30px;
      @media screen and (max-width: 1330px){
        left: 228px;
      }
    }
  }


</style>
