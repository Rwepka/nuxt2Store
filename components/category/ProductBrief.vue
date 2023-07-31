<template>
  <div class="wrapper">
    <nuxt-link :to="`/product/${product.pSlug}`">
      <p>{{ product.pName }}</p>
      <img :src="product.image" />
    </nuxt-link>
    <p>Цена {{ product.pPrice }}</p>
  </div>
</template>

<script>
export default {
  props: {
    product: {
      type: Object,
      default: () => {}
    }
  }
}
</script>

<style>
.wrapper {
  display: flex;
  flex-direction: column;
}
</style>
