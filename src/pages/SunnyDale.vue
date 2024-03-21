<template>
  <section>
    <BreadCrumbs />
    <h2>КРОССОВКИ МУЖСКИЕ SKECHERS SUNNY DALE</h2>
    <ProductCard />
  </section>
</template>

<script setup>
import BreadCrumbs from "@/components/BreadCrumbs.vue";
import ProductCard from "@/components/ProductCard.vue";
</script>

<style lang="scss" scoped>
section {
  width: 100%;
  h2 {
    margin-top: 24px;
    font-size: 32px;
    color: #071435;
    font-family: "GothamPro-Medium", sans-serif;
    font-weight: 400;
  }
}
</style>