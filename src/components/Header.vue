<template>
  <div class="header">
    <div class="header__container">
      <nav class="header__menu menu">
        <ul class="menu__list">
          <li @click="setContent" class="menu__item"><a href="#" data-link="ASTP" class="menu__link">Описание АСУТП</a></li>
          <li @click="setContent" class="menu__item"><a href="#" data-link="PO" class="menu__link">Описание ПО</a></li>
          <li @click="setContent" class="menu__item"><a href="#" data-link="Interface" class="menu__link">Программный интерфейс</a></li>
          <li @click="setContent" class="menu__item"><a href="#" data-link="Dev" class="menu__link">Средства разработки ПО</a></li>
        </ul>
        <div class="burder" @click="opnMenu">
          <img src="../assets/images/burger.png" alt="">
        </div>
      </nav>
    </div>
  </div>
</template>

<script>
export default {
  name: "Header",
  methods: {
    setContent(event) {
      const { link } = event.target.dataset
      this.$emit('set-content', link)
    },
    opnMenu() {
      document.querySelector('.menu__list').classList.toggle('open')
    },
  },
}
</script>

<style scoped>
.header {
  width: 100%;
  position: fixed;
  overflow: hidden;
}

.header__container {
  max-width: 80%;
  margin: 10px auto;
}

.menu__list {
  display: flex;
  justify-content: space-between;
  list-style: none;
}

.menu__item {
  cursor: pointer;
  padding: 10px;
}

.menu__item:hover {
  background-color: rgb(133, 150, 180);
}

.menu__link {
  text-decoration: none;
  color: #fff;
}

@media (max-width: 875px) {
  .menu__list {
    display: none;
  }
  .burder {
    display: block;
  }

  .menu__list.open {
    position: fixed;
    display: flex;
    flex-direction: column;
    background-color: rgba(40, 56, 107, 1);
  }
}
</style>