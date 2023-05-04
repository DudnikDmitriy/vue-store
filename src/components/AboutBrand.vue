<template>
  <div class="about-brand">
    <h3 class="about-brand__title">What makes our brand special</h3>
    <div class="about-brand-elements">
      <div 
        class="about-brand-element"
        v-for="(element, i) in aboutBrands"
        :key="i"
      >
      <img 
        class="about-brand-element__img"
        :src="element.img" 
        alt="element.title"
      >  
        <h5 class="about-brand-element__title">{{ element.title }}</h5>
        <span class="about-brand-element__description">{{ element.description }}</span>
      </div> 
    </div>
  </div>
</template>

<script setup>
  import { ref } from 'vue'

  const aboutBrands = [
    {
      img: '/svg/about-brand-1.svg',
      title: 'Next day as standard',
      description: 'Order before 3pm and get your order the next day as standard'
    },
    {
      img: '/svg/about-brand-2.svg',
      title: 'Made by true artisans',
      description: 'Handmade crafted goods made with real passion and craftmanship'
    },
    {
      img: '/svg/about-brand-3.svg',
      title: 'Unbeatable prices',
      description: 'For our materials and quality you won’t find better prices anywhere'
    },
    {
      img: '/svg/about-brand-4.svg',
      title: 'Recycled packaging',
      description: 'We use 100% recycled to ensure our footprint is more manageable'
    }
  ]
</script>

<styles lang="scss" scoped>
  .about-brand {
    padding: 80px 80px 130px 80px;
    &__title {
      text-align: center;
      font-size: 24px;
      color: #2a254b;
      margin: 0 0 84px
    }
    &-elements {
     
      font-family: 'Clash Display', sans-serif;
      display: grid;
      grid-template-columns: repeat(4, 305px);
      justify-content: space-between;
    }
    &-element{
     background-color: #F9F9F9;
      color: #2a254b;
      margin: 10px;
      padding: 38px;
      &__img{
        display: block;
        margin-bottom: 12px;
      }
      &__title{
        margin-bottom: 12px;
        font-size: 20px;
        font-weight: normal;
        
      }
      &__description{
        font-size: 16px;
        line-height: 1.5;
        
      }
    }
  }
</styles>





 