<template>
  <div>
    <h2>Список категорий</h2>
    <div class="wrapper">
      <div
        v-for="category in categories"
        :key="category.cSlug"
        class="block"
      >
        <nuxt-link :to="`/category/${category.cSlug}`">
          <p>{{ category.cName }}</p>
          <img :src="category.cImage" />
        </nuxt-link>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    categories: {
      type: Array,
      default: () => []
    }
  }
}
</script>
<!-- <style lang="scss">
//   В этом месте поломался sass-loader, дальше без него

  ////////////////////////////////////////////////////////////////////////////////////////////////
  //   in ./components/common/CategoriesList.vue?vue&type=style&index=0&id=0ef42073&lang=scss&  //
  // Module build failed (from ./node_modules/sass-loader/dist/cjs.js):                         //
  // TypeError: this.getOptions is not a function                                               //
  //     at Object.loader (/home/rwepka/nuxt2Store/node_modules/sass-loader/dist/index.js:19:24)//
  ////////////////////////////////////////////////////////////////////////////////////////////////

.wrapper {
display: flex;
}
.block {
display: flex;
flex-direction: column;
}
</style> -->
<style>
.wrapper {
display: flex;
}
.block {
display: flex;
flex-direction: column;
}
</style>