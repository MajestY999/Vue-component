<template>
  <div id="app" style="text-align: center; padding-top: 40px; font-family: sans-serif;">
    <h1>Изучение слотов во Vue.js</h1>

    <BaseAlert>
      Это первое уведомление, здесь просто текст.
    </BaseAlert>

    <BaseAlert>
      <b>Внимание!</b> Это очень важное и  жирное сообщение.
    </BaseAlert>

    <BaseAlert>
      Тут какая-то ошибка. Подробнее можно узнать <a href="#">здесь</a>.
    </BaseAlert>
  </div>
</template>

<script setup>
import BaseAlert from './components/BaseAlert.vue'
</script>