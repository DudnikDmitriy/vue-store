<template>
  <div class="product">
    <a href="#">
      <img class="product-image" :src="img" :alt="title">
    </a>
    <a class="product-name" href="#">{{ title }}</a>
    <span class="product-price">£{{ price }}</span>
  </div>
</template>

<script setup>
  const props = defineProps({
    img: {
      type: String,
      required: true
    },
    title: {
      type: String,
      required: true
    },
    price: {
      type: Number,
      required: true
    }
  });
</script>

<style lang="scss" scoped>
  .product {
    &-image{
      display: block;
      margin-bottom: 24px;
    }
    &-name{
      display: block;
      color: #2a254b;
      font-size: 20px;
      line-height: 28px;
      font-family: 'Clash Display', sans-serif;
      margin-bottom: 18px;
      text-decoration: none;
      &:hover{
        text-decoration: underline;
      }
    }
    &-price{
      display: block;
      font-size: 18px;
      color: #2a254b;
    }
  }
</style>