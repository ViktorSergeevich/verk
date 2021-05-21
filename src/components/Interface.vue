<template>
  <article class="page">
    <div class="page__image">
      <img src="../assets/images/YkilSzVH2qk.jpeg" alt="">
    </div>
    <div class="page__container container">
      <h1 class="page__header">Программный интерфейс</h1>
      <div class="page__content">
        <p>В интерфейсе пользователя есть возможности ввода входных данных, запуск процесса ректификации, а также возможность отслеживания текущих параметров и построения графиков изменения параметров с момента запуска установки.
        </p>
      <img src="../assets/images/interface.jpeg" alt="">
      </div>
    </div>
  </article>
</template>

<script>
export default {
  name: 'Interface'
}
</script>

<style scoped>
.page__header {
  text-align: center;
  margin-bottom: 20px;
}

.page__content {
  display: flex;
  flex-direction: column;
}

.page__content img {
  align-self: center;
  width: 80%;
  object-fit: cover;
}
</style>