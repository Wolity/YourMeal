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
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    background: #ffab08;
    img {
      margin-top: 24px;
      width: 152px;
    }
    div {
      margin-top: 40px;
      display: flex;
      margin-bottom: 50px;
      gap: 57px;

      img {
        width: 176px;
      }
      nav {
        color: white;
        margin-top: 41px;
        h2 {
          line-height: 43px;

          color: #ff5c00;
        }
        h1,
        h2 {         
          font-weight: 800;
          font-size:36px;
        }
        p {
          margin-top: 26px;
          font-size: var(--size-16-16-12-12);
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
    background: #ffab08;
    img {
      margin-top: 40px;
      width: 150px;
    }
    div {
      margin-top: 24px;
      display: flex;
      margin-bottom: 37px;

      img {
       margin-top: 222px;
       width: 176px;
      }
      nav {
        justify-content: center;
        align-items: center;
        text-align: center;
        color: white;
        margin-top: 24px;
        h2 {

          line-height: 36px;

          color: #ff5c00;
        }
        h1,
        h2 {
          font-weight: 800;
          font-size: var(--size-50-50-36-30);
        }
        p {
          margin-top: 16px;
          font-size: var(--size-16-16-12-12);
        }
      }
    }
  }
}
</style>
