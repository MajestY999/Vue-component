<template>
  <link
    rel="stylesheet"
    href="https://cdnjs.cloudflare.com/ajax/libs/semantic-ui/2.4.1/semantic.min.css"
  />

  <div v-if="isVisible" :class="['ui', type, 'message']">
    <i class="close icon" @click="closeNotification"></i>

    <div class="header">
      <slot name="header"></slot>
    </div>

    <p>
      <slot></slot>
    </p>
  </div>
</template>

<script setup>
import { ref } from "vue";

defineProps({
  type: {
    type: String,
    default: "info",
  },
});

const isVisible = ref(true);

const closeNotification = () => {
  isVisible.value = false;
};
</script>

<style scoped>
.ui.message .close.icon {
  cursor: pointer;
  opacity: 0.7;
  transition: opacity 0.2s;
}
.ui.message .close.icon:hover {
  opacity: 1;
}
</style>
