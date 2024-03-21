<template>
  <label class="checkbox-ios">
    <input type="checkbox" checked />
    <span class="checkbox-ios-switch"></span>
  </label>
</template>

<script setup>
</script>

<style lang="scss" scoped>
.checkbox-ios {
  display: inline-block;
  height: 24px;
  line-height: 24px;
  margin-right: 10px;
  position: relative;
  vertical-align: middle;
  font-size: 14px;
  user-select: none;
  cursor: pointer;
  .checkbox-ios-switch {
    position: relative;
    display: inline-block;
    box-sizing: border-box;
    width: 40px;
    height: 24px;
    border: 1px solid rgba(0, 0, 0, 0.1);
    border-radius: 25%/50%;
    vertical-align: top;
    background: #828ead;
    transition: 0.2s;
  }
  .checkbox-ios-switch:before {
    content: "";
    position: absolute;
    top: 1px;
    left: 1px;
    display: inline-block;
    width: 20px;
    height: 20px;
    border-radius: 50%;
    background: white;
    box-shadow: 0 3px 5px rgba(0, 0, 0, 0.3);
    transition: 0.15s;
  }
  input[type="checkbox"] {
    display: block;
    width: 0;
    height: 0;
    position: absolute;
    z-index: -1;
    opacity: 0;
  }
  input[type="checkbox"]:not(:disabled):active + .checkbox-ios-switch:before {
    box-shadow: inset 0 0 2px rgba(0, 0, 0, 0.3);
  }
  input[type="checkbox"]:checked + .checkbox-ios-switch {
    background: #1551e5;
  }
  input[type="checkbox"]:checked + .checkbox-ios-switch:before {
    transform: translateX(15px);
  }
}
</style>