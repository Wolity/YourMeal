<script setup>
import burger from "../assets/menu/cheesburger.svg"
import onion from "../assets/menu/onion.svg"
let menu = [
    {
        name:"Бургеры",
        src:burger
    },
    {
        name:"Закуски",
        src:onion
    },
]

</script>

<template>
  <nav>
    <ul>
      <li v-for="(item,i) in menu" :key="i">
        <img :src="item.src"/>
        <a>{{ item.name }}</a>
      </li>
    </ul>
  </nav>
</template>

<style scoped lang="scss">
nav {
  ul {
    li {
      a {
        color: black;
      }
    }
  }
}
</style>
