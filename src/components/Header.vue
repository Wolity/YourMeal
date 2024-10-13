<script setup>
import logo from "../assets/logo.svg";
import burger from "../assets/burger.svg";
</script>

<template>
  <header>
    <img :src="logo" />
    <div>
      <img :src="burger" />
      <nav>
        <h1>Только самые</h1>
        <h2>сочные бургеры!</h2>
        <p>Бесплатная доставка от 599₽</p>
      </nav>
    </div>
  </header>
</template>

<style scoped lang="scss">
header {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background: #ffab08;
  img {
    margin-top: 24px;
    width: 150px;
  }
  div {
    margin-top: 40px;
    display: flex;
    margin-bottom: 72px;
    gap: 57px;

    img {
      width: 250px;
    }
    nav {
      color: white;
      margin-top: 46px;
      h2 {
        line-height: 60px;

        color: #ff5c00;
      }
      h1,
      h2 {
        font-weight: 800;
        font-size: var(--size-50-50-36-30);
      }
      p {
        margin-top: 52px;
        font-size: var(--size-16-16-12-12);
      }
    }
  }
}
@media screen and (max-width: 768px) {
  header {
    div {
      margin-bottom: 50px;

      img {
        width: 176px;
      }
      nav {
        h2 {
          line-height: 43px;
        }
        p {
          margin-top: 26px;
        }
      }
    }
  }
}
@media screen and (max-width: 480px) {
  header {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    img {
      margin-top: 24px;
      width: 150px;
    }
    div {
      gap: 37px;
      align-items: center;
      flex-direction:column-reverse ;
      margin-top: 24px;
      margin-bottom: 37px;

      img {
        width: 176px;
        margin-top: 0px;
      }
      nav {
        text-align: center;
        margin-top: 0px;
        p {
          margin-top: 16px;
        }
      }
    }
  }
}
</style>
