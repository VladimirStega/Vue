<!-- eslint-disable linebreak-style -->
<!-- eslint-disable vue/valid-template-root -->
<template>
  <ul class="catalog__list">
    <ProductItem v-for="product in products" :key="product.id" :product="product"/>
  </ul>
</template>

<script>

import ProductItem from './ProductItem.vue';

export default {
  name: 'ProductList',
  components: { ProductItem },
  props: ['products'],
};
</script>
