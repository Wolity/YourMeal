<script setup>
import Basket from "./components/Basket.vue"
import Menu from "./components/Menu.vue";
import Header from "./components/Header.vue";
import Cards from "./components/Cards.vue";
</script>
<template>
  <Header />
  <Menu />
  <main>
    <Basket class="main_basket"/>
    <Cards/>
  </main>
</template>
<style lang="scss">
body{
 background: #F9F9F9;
}
main{
  padding: 50px 75px;
  display: grid;
  grid-template-columns: 300px auto;
  gap: 30px;
  .main_basket{
    margin-top: 135px;
  }
}
</style>
