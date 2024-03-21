<template>
  <div class="app">
    <MainHeader />
    <main class="main">
      <slot/>
    </main>
    <MainFooter class="footer"/>
  </div>
</template>

<script setup>
import MainFooter from './MainFooter.vue';
import MainHeader from './MainHeader.vue';

</script>

<style lang="scss" scoped>
.app {
  width: 100vw;
  height: 100vh;
  .main {
    max-width: 1600px;
    min-height: 600px;
    margin: 0 auto;
    padding: 24px;
  }
}

</style>