<template>
  <article class="page">
    <div class="page__image">
      <img src="../assets/images/YkilSzVH2qk.jpeg" alt="">
    </div>
    <div class="page__container container">
      <h1 class="page__header">Средства разработки программного обеспечения</h1>
      <div class="page__content">
        <p>Для разработки данного программного комплекса были выбраны следующие инструменты разработки:</p>
        <ul>
          <li>база данных – Cloud Firestore. Она отвечает всем требованиям, предъявляемым к программному комплексу: гибкость; слабосвязность; масштабируемость; безопасность; возможность работы в офлайн режиме.</li>
          <li>среда разработки – Android Studio. Поддерживает работу с базой данных Cloud Firestore.</li>
          <li>Язык программирования – Kotlin.</li>
        </ul>
        <img src="../assets/images/dev.jpeg" alt="">
      </div>
    </div>
  </article>
</template>

<script>
export default {
  name: 'Dev'
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