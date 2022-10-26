<!-- eslint-disable vuejs-accessibility/label-has-for -->
<!-- eslint-disable max-len -->
<template>

  <li class="catalog__item">
    <a class="catalog__pic" href="#">
      <img :src="product.image" srcset="img/radio@2x.jpg 2x" :alt="product.title">
    </a>

    <h3 class="catalog__title">
      <a href="#">
        {{ product.title }}
      </a>
    </h3>

    <span class="catalog__price">
      {{ product.price }} ₽
    </span>

    <ul class="colors colors--black">
      <li class="colors__item" v-for="(item, index) in product.colorCode" :key="index">
        <label class="colors__label" >
          <input class="colors__radio sr-only" type="radio" value="#73B6EA">
          <span class="colors__value" :style="`background-color: ${item};`"></span>
        </label>
      </li>
    </ul>
  </li>

</template>

<script>
export default {
  data() {
    return {
      color: '73B6EA',
    };
  },
  name: 'ProductItem',
  props: ['product'],
};
</script>
