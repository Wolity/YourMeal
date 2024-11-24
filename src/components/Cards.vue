<script setup>
import { defineProps } from "vue";
defineProps({
  content: Array,
});
</script>

<template>
  <section>
    <h2>Бургеры</h2>
    <div>
      <article v-for="item in content" :key="item.id">
        <img :src="item.src" />
        <h3>{{ item.price }}₽</h3>
        <p>{{ item.title }}</p>
        <span>{{ item.weight }}</span>
        <button>Добавить</button>
      </article>
    </div>
  </section>
</template>

<style scoped lang="scss">
section {
  h2 {
    font-size: var(--size-40-40-28-28);
    font-weight: 600;
    margin-top: 50px;
  }
  div {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    gap: 30px;
    margin-top: 24px;
    article {
      display: flex;
      flex-direction: column;
      border-radius: 18px;
      width: 100%;
      padding: 12px;
      background: white;
      img {
        object-fit: cover;
        aspect-ratio: 5/4;
        border-radius: 12px;
      }
      h3 {
        font-size: var(--size-24-24-16-16);
        margin-top: 16px;
      }
      p {
        font-size: var(--size-16-16-12-12);
        margin-top: 8px;
      }
      span {
        opacity: 0.6;
        font-size: var(--size-16-16-12-12);
        margin-top: 8px;
      }
      button {
        text-align: center;
        margin-top: 8px;
        padding-top: 11px;
        padding-right: 92px;
        padding-bottom: 11px;
        padding-left: 92px;
        gap: 10px;
        border: none;
        border-radius: 12px;
        transition: background 0.3s ease;
      }
      button:hover {
        background: #ffab08;
      }
    }
  }
}

@media screen and (max-width: 1024px) {
  section {
    div {
      display: grid;
      grid-template-columns: 1fr 1fr;
    }
  }
}

@media screen and (max-width: 768px) {
  section {
    h2 {
      font-size: var(--size-40-40-28-28);
      font-weight: 600;
      margin-top: 50px;
    }
    div {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 20px;
      margin-top: 24px;
      article {
        display: flex;
        flex-direction: column;
        border-radius: 18px;
        width: 100%;
        padding: 12px;
        background: white;
        img {
          object-fit: cover;
          aspect-ratio: 5/4;
          border-radius: 12px;
        }
        h3 {
          font-size: var(--size-24-24-16-16);
          margin-top: 16px;
        }
        p {
          font-size: var(--size-16-16-12-12);
          margin-top: 8px;
        }
        span {
          opacity: 0.6;
          font-size: var(--size-16-16-12-12);
          margin-top: 8px;
        }
        button {
          text-align: center;
          margin-top: 8px;
          padding-top: 11px;
          padding-right: 92px;
          padding-bottom: 11px;
          padding-left: 92px;
          gap: 10px;
          border: none;
          border-radius: 12px;
          transition: background 0.3s ease;
        }
        button:hover {
          background: #ffab08;
        }
      }
    }
  }
}

@media screen and (max-width: 640px) {
  section {
    h2 {
      font-size: var(--size-40-40-28-28);
      font-weight: 600;
      margin-top: 50px;
    }
    div {
      display: grid;
      grid-template-columns: 1fr;
    }
  }
}
</style>
