<script setup></script>

<template>
  <section class="basket">
    <div class="basket_top">
      <h2>Корзина</h2>
      <span>4</span>
    </div>
    <article class="basket_card">
      <img
        src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRx3TOn2yLGB3Gm4d2M-mpe7zDYhAHrel716Q&s"
      />
      <div>
        <p>Супер сырный</p>
        <span>512г</span>
        <h3>550р</h3>
      </div>
      <nav>
          <button>-</button>
          <span>0</span>
          <button>+</button>
      </nav>
    </article>
    <div class="basket_price">
      <h4>Итого</h4>
      <h3>1300</h3>
    </div>
    <button class="basket_buy">Оформить заказ</button>
  </section>
</template>

<style scoped lang="scss">
.basket {
  .basket_top {
    display: flex;
    h2 {
    }
    span {
    }
  }
  .basket_card {
    align-items: center;
    display: flex;
    img{
        width:64px;
        
    }
    div{
       p{
       }
       span{
       }
       h3{

       } 
    }
    nav{
margin-left: auto;
    }
  }
  .basket_price{
    
  }
}
</style>
