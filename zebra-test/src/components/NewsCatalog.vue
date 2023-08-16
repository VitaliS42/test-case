<script setup>
import Card from './card.vue';
</script>

<template>
  <section class="news">
    <div class="container">
      <div class="news__flex">
        <Card/>
        <Card/>
        <Card/>
        <Card/>
        <Card/>
      </div>
      <div class="news__button-container">
        <button class="news__button">загрузить ещё</button>
      </div>
    </div>
  </section>
</template>

<style scoped>
  .news {
    padding: 64px 0 72px 0;
  }
  .news__flex {
    /* display: grid;
    grid-template-columns: 536px 536px 536px; */
    display: flex;
    flex-wrap: wrap;
    gap:64px 46px;
    margin-bottom: 72px;
  }
  .news__button-container {
    display: flex;
    justify-content: center;
  }
  .news__button {
    cursor: pointer;
    display: inline-block;
    font-size: 20px;
    font-weight: 600;
    line-height: 24px;
    letter-spacing: -0.01em;
    text-align: center;
    padding: 16px 32px;
    border: 1px solid #002DBF;
    border-radius: 8px;
    background-color: white;
    color: #002DBF;
  }
</style>