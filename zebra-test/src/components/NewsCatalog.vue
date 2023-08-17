<script setup>
import Card from './card.vue';
import {reactive, ref} from 'vue'

const data = ref([])
const error = ref([])

let api = 'http://flems.github.io/test/api/news/';


fetch(api)
  .then((res) => res.json())
  .then((json) => (data.value = json))
  .catch((err) => (error.value = err))
</script>

<template>
  <section class="news">
    <div class="container">
      <div class="news__flex">
        <Card v-for="newsItem in data.items" :newsItem="newsItem"/>
      </div>
      <div class="news__button-container">
        <button v-show="(data.nav.current!==data.nav.total)"  class="news__button">загрузить ещё</button>
      </div>
    </div>
  </section>
</template>

<style scoped>
  .news {padding: 64px 0 72px 0;}
  .news__flex {display: flex;flex-wrap: wrap;gap:64px 46px;margin-bottom: 72px;}
  .news__button-container {display: flex;justify-content: center;}
  .news__button {cursor: pointer;display: inline-block;font-size: 20px;font-weight: 600;line-height: 24px;letter-spacing: -0.01em;text-align: center;padding: 16px 32px;border: 1px solid #002DBF;border-radius: 8px;background-color: white;color: #002DBF;}
</style>