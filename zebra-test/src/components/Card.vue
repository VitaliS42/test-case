<script setup>
  import { ref } from "vue";
  const image = ref(true)
</script>


<template>
  <section class="card">
    <div v-show="image" class="card__img-container">
      <img src="/public/img/news-pic.jpg" alt="">
    </div>
    <div v-show="!image" style="height: 16px;"></div>
    <div class="card__container">
      <div class="card__text">
        <div class="card__date">
          <div>
            <span class="card__date-day" >28</span>
          </div>
          <div>
            <span class="card__date-rest">February</span>
            <span class="card__date-rest">2022</span>
          </div>
        </div>
        <h4>Alpha сообщает о новых высокопроизводительных оборудованиях для сельского хозяйства</h4>
        <p>Alpha объявляет о партнёрстве с Миром, ведущим мировым поставщиком экологических услуг, чтобы помочь клиентам строить светлое будущее.</p>
      </div>
      <div class="card__badge">Новости</div>
    </div>
  </section>
</template>

<style scoped>
  .card {
    position: relative;
    width: 536px;
    height: 577px;
    border: 1px solid #0F62FE;
    border-radius: 16px;
    display: flex;
    flex-direction: column;
  }
  .card__img-container {
    margin-top: -1px;
    margin-left: -1px;
    width: 536px;
    height: 250px;
    border-radius: 16px 16px 0px 0px;
  }
  .card__img-container img{
    width: 100%;
    height: auto;
  }
  .card__container {
    flex-grow: 1;
    padding: 32px;
    display: flex;
    flex-direction: column;
    align-items: baseline;
  }
  .card__text {
    flex-grow: 1;
  }
  .card__date {
    margin-bottom: 16px;
    display: flex;
    color: #A1A7B5;
  }
  .card__date-day {
    font-size: 36px;
    font-weight: 400;
    line-height: 36px;
    letter-spacing: 0em;
    text-align: left;
  }
  .card__date-rest {
    margin-left: 4px;
    display: block;
    font-size: 15px;
    font-weight: 700;
    line-height: 17px;
    letter-spacing: -0.01em;
    text-align: left;
  }
  .card h4 {
    display: inline-block;
    font-size: 22px;
    font-weight: 400;
    line-height: 26px;
    letter-spacing: 0em;
    text-align: left;
    color: #0C5BEF;
    margin-bottom: 16px;
  }

  .card h4:hover {
    cursor: pointer;
    color:#0029A9;
  }
  .card p {
    display: inline-block;
    font-size: 20px;
    font-weight: 400;
    line-height: 26px;
    letter-spacing: -0.01em;
    text-align: left;
  }
  .card__badge {
    padding: 4px 16px 4px 16px;
    border-radius: 360px;
    background-color:#F0F6FE;
  }
</style>