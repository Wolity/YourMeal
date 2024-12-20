<script setup>
import Basket from "./components/Basket.vue";
import Menu from "./components/Menu.vue";
import Header from "./components/Header.vue";
import Cards from "./components/Cards.vue";
import Footer from "./components/Footer.vue";
import { onMounted, ref } from "vue";
//переменные
let products = ref([]);
let menuActive = ref("burgers");
//функция
async function getProducts() {
  let data = await fetch("https://04467dff024a9932.mokky.dev/products");
  products.value = await data.json();
  console.log(products.value);
}
onMounted(async () => {
  await getProducts();
});
let basket = ref([]);
function addItemBasket(item) {
  for (const i of basket.value) {
    if (i.id == item.id) {
      i.count += 1;
      return;
    }
  }
  item.count = 1;
  basket.value.push(item);
  console.log(basket.value);
}
function cMenu(item) {
  menuActive.value = item
}
</script>
<template>
  <Header />
  <Menu :menuActive="menuActive" @changeMenu="cMenu" />
  <main>
    <Basket class="main_basket" />
    <Cards
      v-if="products.length > 0"
      :content="products[0][menuActive]"
      @addBasket="(item) => addItemBasket(item)"
    />
  </main>
  <Footer />
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
@media screen and (max-width: 1080px) {
  main {
    grid-template-columns: 1fr;
  }
}
</style>
