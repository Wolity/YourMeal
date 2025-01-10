<script setup></script>

<template>
  <footer class="footer">
    <article class="main">
      <img src="../assets/Footer.svg" alt="" class="main_picture" />
      <section class="connect">
        <h1>Номер для заказа</h1>
        <div class="connect_block">
          <img src="../assets/Call.svg" />
          <p>+7(930)833-38-11</p>
        </div>
      </section>
      <section class="social">
        <h2>Мы в соцсетях</h2>
        <img src="../assets/Telegram.svg" class="social_tg" />
        <img src="../assets/Vk.svg" class="social_vk" />
      </section>
    </article>
  </footer>
</template>
<style lang="scss">
footer {
}
.main {
  display: flex;
  .main_picture {
    padding-left: 75px;
  }
}
.connect {
  padding-left: 355px;
  h1 {
    font-size: var(--size-24-24-16-16);
    padding-bottom: 24px;
  }
  .connect_block {
    display: flex;
    img {
      padding-right: 2px;
    }
    p {
      font-size: var(--size-16-16-12-12);
    }
  }
}
.social {
  h2 {
    padding-bottom: 22px;
    padding-left: 125px;
    font-size: var(--size-24-24-16-16);
  }
  .social_tg {
    padding-left: 125px;
  }
  .social_vk {
    padding-left: 15px;
  }
}
</style>
