<template>
  <header class="header">
    <div class="header-top">
      <div class="header-top-search">
        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-search" viewBox="0 0 16 16">
           <path d="M11.742 10.344a6.5 6.5 0 1 0-1.397 1.398h-.001c.03.04.062.078.098.115l3.85 3.85a1 1 0 0 0 1.415-1.414l-3.85-3.85a1.007 1.007 0 0 0-.115-.1zM12 6.5a5.5 5.5 0 1 1-11 0 5.5 5.5 0 0 1 11 0z"/>
        </svg>
      </div>
     <a href="#" class="header-logo">Impulse</a>
     <div class="header-top-right">
      <div class="header-top-right__user">
        <a href="#">
          <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-person-circle" viewBox="0 0 16 16">
            <path d="M11 6a3 3 0 1 1-6 0 3 3 0 0 1 6 0z"/>
            <path fill-rule="evenodd" d="M0 8a8 8 0 1 1 16 0A8 8 0 0 1 0 8zm8-7a7 7 0 0 0-5.468 11.37C3.242 11.226 4.805 10 8 10s4.757 1.225 5.468 2.37A7 7 0 0 0 8 1z"/>
          </svg>
        </a>
      </div>
      <div class="header-top-right__cart">
        <a href="#">
          <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-cart" viewBox="0 0 16 16">
            <path d="M0 1.5A.5.5 0 0 1 .5 1H2a.5.5 0 0 1 .485.379L2.89 3H14.5a.5.5 0 0 1 .491.592l-1.5 8A.5.5 0 0 1 13 12H4a.5.5 0 0 1-.491-.408L2.01 3.607 1.61 2H.5a.5.5 0 0 1-.5-.5zM3.102 4l1.313 7h8.17l1.313-7H3.102zM5 12a2 2 0 1 0 0 4 2 2 0 0 0 0-4zm7 0a2 2 0 1 0 0 4 2 2 0 0 0 0-4zm-7 1a1 1 0 1 1 0 2 1 1 0 0 1 0-2zm7 0a1 1 0 1 1 0 2 1 1 0 0 1 0-2z"/>
          </svg>
        </a>
      </div>
      
     </div>
    </div>
    <div class="header-menu">
      <a 
        class="header-menu__link" 
        :href="element.path" 
        v-for="(element, i) of menu"
        :key="i">{{ element.name }}</a>
    </div>
  </header>
</template>

<script setup>
  import { ref } from 'vue';

  const menu = [
    {
      name: 'Plant pots',
      path: '/plant'
    },
    {
      name: 'Ceramics',
      path: '/ceramics'
    },
    {
      name: 'Tables',
      path: '/ceramics'
    },
  ]
</script>
<style lang="scss" scoped>
  .header{
    height: 132px;
    background-color: #fff;
      &-top{
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        height: 70px;
        align-items: center;
        border-bottom: 1px solid rgba(0, 0, 0, 0.1);
        margin: 0 28px;
        &-right{
          display: flex;
          align-items: center;
          justify-content: flex-end;
          &__user {
            margin-right: 16px;
          }
        }
      }
      &-logo{
        color: #22202E;
        font-size: 24px;
        text-decoration: none;
        font-family: 'Clash Display', sans-serif;
        text-align: center;
        &:hover{
          text-decoration: underline;
        }
      }
      &-menu{
        height: 62px;  
        display: flex;
        justify-content: center;
        align-items: center;
        &__link{
          margin: 0 22px;
          color: #726E8D;
          text-decoration: none;
          &:hover{
            text-decoration: underline; 
          }
        } 
      }  
    }
</style>