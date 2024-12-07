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
      <h3>1300₽</h3>
    </div>
    <button class="basket_buy">Оформить заказ</button>
  </section>
</template>

<style scoped lang="scss">
.basket {
  .basket_top {
    display: flex;
    align-items: center;
    justify-content: space-between;
    h2 {
      font-size: var(--size-24-24-16-16);
    }
    span {
      font-size: var(--size-12-12-12-12);
    }
  }
  .basket_card {
    margin-top: 12px;
    align-items: center;
    display: flex;
    img {
      margin-right: 6px;
      width: 64px;
      height: 52px;
      border-radius: 8px;
    }
    div {
      p {
      }
      span {
        font-size: var(--size--12-12-12-12);
        margin-top: 1px;
        opacity: 0.6;
      }
      h3 {
        font-size: var(--size--12-12-12-12);
        margin-top: 6px;
      }
    }
    nav {
      font-size: var(--size--12-12-12-12);
      margin-left: auto;
      button {
        font-size: var(--size-16-16-12-12);
        border: none;
      }
      span {
        margin-left: 18px;
        margin-right: 15px;
        font-size: var(--size-16-16-12-12);
      }
    }
  }
  .basket_price {
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-top: 16px;
    
    h4 {
    }

    h3 {
    }
  }
  .basket_buy{
      text-align: center;
        margin-top: 24px;
        padding-top: 11px;
        padding-right: 92px;
        padding-bottom: 11px;
        padding-left: 92px;
        gap: 10px;
        border: none;
        border-radius: 12px;
        color: white;
        background: #FF7020;
    }
}
</style>
