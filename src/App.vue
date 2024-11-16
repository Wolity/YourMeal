<script setup>
import Basket from "./components/Basket.vue";
import Menu from "./components/Menu.vue";
import Header from "./components/Header.vue";
import Cards from "./components/Cards.vue";
import { onMounted, ref } from "vue";
//переменные
let products = ref([]);
let menuActive = ref("zakuski");
//функция
async function getProducts() {
  let data = await fetch("https://04467dff024a9932.mokky.dev/products");
  products.value = await data.json();
  console.log(products.value);
}
onMounted(() => {
  getProducts();
});
</script>
<template>
  <Header />
  <Menu :menuActive="menuActive" />
  <main>
    <Basket class="main_basket" />
    <Cards />
  </main>
</template>
<style lang="scss">
body {
  background: #f9f9f9;
}
main {
  padding: 50px 75px;
  display: grid;
  grid-template-columns: 300px auto;
  gap: 30px;
  .main_basket {
    margin-top: 135px;
  }
}
</style>
