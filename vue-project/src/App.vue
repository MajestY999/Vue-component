<template>
  <div
    id="app"
    class="ui container"
    style="padding-top: 40px; font-family: sans-serif"
  >
    <h1>Notification Center</h1>

    <NotificationMessage type="info">
      <template #header>Вы имеете право на вознаграждение</template>
      Перейдите на страницу <b>специальных предложений</b>, чтобы увидеть его
      прямо сейчас.
    </NotificationMessage>

    <NotificationMessage type="success">
      <template #header>Аккаунт успешно создан!</template>
      Добро пожаловать на платформу. Проверьте вашу почту для подтверждения.
    </NotificationMessage>

    <NotificationMessage type="error">
      <template #header>Произошла ошибка</template>
      Не удалось отправить форму. Попробуйте перезагрузить страницу.
    </NotificationMessage>
  </div>
</template>

<script setup>
import NotificationMessage from "./components/NotificationMessage.vue";
</script>
