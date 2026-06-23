<template>
  <div class="alert-box">
    <span class="alert-icon">📢</span>
    <div class="alert-content">
      <slot></slot>
    </div>
  </div>
</template>

<style scoped>
.alert-box {
  display: flex;
  align-items: center;
  border: 1px solid #333;
  padding: 15px;
  margin: 10px auto;
  max-width: 400px;
  background-color: #f9f9f9;
  border-radius: 4px;
  text-align: left;
}
.alert-icon {
  font-size: 20px;
  margin-right: 15px;
}
.alert-content {
  font-size: 14px;
}
</style>
