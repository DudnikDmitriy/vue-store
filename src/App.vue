<script setup>
   
  import Header from './components/Layout/Header.vue'
  import Hero from './components/Hero.vue'
  import AboutBrand from './components/AboutBrand.vue'
  import Products4Column from './components/Products4Column.vue'

  



</script>

<template>
  <div class="container">
    <Header/>
    <Hero/>
    <AboutBrand/>
    <Products4Column/>
  </div>
</template>

<style lang="scss">
@import url('https://fonts.cdnfonts.com/css/satoshi');
@import url('https://fonts.cdnfonts.com/css/clash-display');
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
  body{
    font-family: 'Satoshi', sans-serif;
    font-size: 16px;
    color: #22202e;
    font-weight: 400;
    // font-family: 'Clash Display', sans-serif;
  }
  .container {
    max-width: 1440px;
    margin: auto;
  }
  img {
    max-width: 100%;
  }
</style>
