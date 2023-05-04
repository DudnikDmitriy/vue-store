<template>
  <div class="hero">
    <div class="hero-info">
      <div class="hero-info-text">
        <h2 class="hero-info-text__title">
          Luxury homeware for people who 
          love <br/> tinless design quality
        </h2>
        <span class="hero-info-text__description">
          Shop the new Spring 2022 collection today
        </span>
      </div>
      <a href="#" class="hero-info-link">View collection</a>
    </div>
  </div>
</template>

<style lang="scss">
  .hero {
    background: url(.././assets/img/hero.jpg);
    height: 704px;
    background-size: cover;
    display: flex;
    align-items: center;
    justify-content: flex-end;
    padding-right: 80px;
   &-info {
    background: #fff;
    max-width: 630px;
    padding: 50px 55px;
    height: 444px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    &-text {
      &__title{
        font-family: 'Clash Display', sans-serif;
        font-weight: 400;
        line-height: 1.5;
      }
      &__description{
        color: #585676;
        font-size: 18px;
        margin-top: 30px;
      }
       
    }
   
   
    &-link {
      color: #2a254b;
      text-decoration: none;
      &:hover{
        text-decoration: underline;
      }
    }
   }
  }

</style>