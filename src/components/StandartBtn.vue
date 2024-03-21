<template>
  <button
    :style="`color: ${color}; background: ${background}; width: ${width}; height: ${height}`"
  >
    <img :src="icon" />
    <span>{{ text }}</span>
  </button>
</template>

<script setup>
defineProps({
  icon: String,
  text: String,
  color: String,
  background: String,
  width: String,
  height: String,
});
</script>

<style lang="scss" scoped>
button {
  height: 48px;
  padding: 12px 24px 12px 24px;
  border-radius: 8px;
  display: flex;
  align-items: center;
  justify-content: space-between;

  span {
    font-family: "GothamPro-Medium", sans-serif;
    font-size: 14px;
    font-weight: 400;
    white-space: nowrap;
  }
}
</style>