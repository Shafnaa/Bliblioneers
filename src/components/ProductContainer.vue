<script setup>
import ProductCard from "./ProductCard.vue";
</script>

<template>
  <div class="container-product">
    <ProductCard price="3550000" discount="99" imgUrl="./assets/R.webp">
      <template #title>
        NIKE AJ1 Retro High White University Blue Hazzardous Malicious
      </template>
    </ProductCard>

    <ProductCard price="3550000">
      <template #title>
        NIKE AJ1 Retro High White University Blue Hazzardous Malicious
      </template>
    </ProductCard>

    <ProductCard price="3550000" discount="99" imgUrl="./assets/R.webp">
      <template #title>
        NIKE AJ1 Retro High White University Blue Hazzardous Malicious
      </template>
    </ProductCard>

    <ProductCard price="3550000">
      <template #title>
        NIKE AJ1 Retro High White University Blue Hazzardous Malicious
      </template>
    </ProductCard>

    <ProductCard price="3550000" discount="99" imgUrl="./assets/R.webp">
      <template #title>
        NIKE AJ1 Retro High White University Blue Hazzardous Malicious
      </template>
    </ProductCard>

    <ProductCard price="3550000">
      <template #title>
        NIKE AJ1 Retro High White University Blue Hazzardous Malicious
      </template>
    </ProductCard>

    <ProductCard price="3550000" discount="99" imgUrl="./assets/R.webp">
      <template #title>
        NIKE AJ1 Retro High White University Blue Hazzardous Malicious
      </template>
    </ProductCard>

    <ProductCard price="3550000">
      <template #title>
        NIKE AJ1 Retro High White University Blue Hazzardous Malicious
      </template>
    </ProductCard>

    <ProductCard price="3550000" discount="99" imgUrl="./assets/R.webp">
      <template #title>
        NIKE AJ1 Retro High White University Blue Hazzardous Malicious
      </template>
    </ProductCard>

    <ProductCard price="3550000">
      <template #title>
        NIKE AJ1 Retro High White University Blue Hazzardous Malicious
      </template>
    </ProductCard>
  </div>
</template>

<style scoped>
.container-product::-webkit-scrollbar {
  display: none;
}
.container-product {
  width: 100%;
  display: grid;
  grid-auto-flow: column;
  gap: 1em;
  padding: 0.125em;
  overflow-x: auto;
  -ms-overflow-style: none;
  scrollbar-width: none;
}

@media (min-width: 801px) {
  .container-product {
    order: 5;
  }
}
</style>
