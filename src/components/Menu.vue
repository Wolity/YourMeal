<script setup>
import burger from "../assets/menu/cheesburger.svg";
import onion from "../assets/menu/onion.svg";
import hotdog from "../assets/menu/hotdog.svg";
import combo from "../assets/menu/combo.svg";
import shaurma from "../assets/menu/shaurma.svg";
import pizza from "../assets/menu/pizza.svg";
import wok from "../assets/menu/wok.svg";
import dessert from "../assets/menu/dessert.svg";
import sauce from "../assets/menu/sauce.svg";
import { defineProps } from "vue";

defineProps({
  menuActive:String
})

let menu = [
  {
    name: "burgers",
    src: burger,
  },
  {
    name: "zakuski",
    src: onion,
  },
  {
    name: "hot-Dogs",
    src: hotdog,
  },
  {
    name: "combo",
    src: combo,
  },
  {
    name: "shaurma",
    src: shaurma,
  },
  {
    name: "pizza",
    src: pizza,
  },
  {
    name: "wok",
    src: wok,
  },
  {
    name: "desserts",
    src: dessert,
  },
  {
    name: "sauces",
    src: sauce,
  },
];
</script>

<template>
  <nav>
    <ul>
      <li v-for="(item, i) in menu" :key="i" :class="{ active: item.name == menuActive }">
        <img :src="item.src" />
        <a>{{ item.name }}</a>
      </li>
    </ul>
  </nav>
</template>

<style scoped lang="scss">
nav {
  display: flex;
  overflow-x: scroll;
  margin-top: 40px;
  &::-webkit-scrollbar{display: none;}
  ul {
    padding: 2px 75px;
    display: flex;
    gap: 24px;
    li {
      display: flex;
      align-items: center;
      gap: 8px;
      background: white;
      padding: 8px 14px;
      border-radius: 50px;
      outline: 1px solid#ffffff;
      transition: all 1s;
      &:hover {
        outline: 1px solid#FFAB08;
      }
      img {
        width: 24px;
      }
      a {
        font-size: var(--size-16-16-12-12);
        white-space: nowrap;
      }
    }
    .active {
      background: #ffab08;
    }
  }
}
@media screen and (max-width: 1024px){
  nav{
    ul{
      padding: 2px 32px;
    }
  }
}
@media screen and (max-width: 768px){
  nav{
    ul{
      padding: 2px 64px;
      gap: 12px;
      li{
        padding: 3px 8px;
      }
    }
  }
}
@media screen and (max-width: 480px){
  nav{
    margin-top: 30px;
    ul{
      padding: 2px 10px;
      gap: 8px;
    }
  }
}
</style>
