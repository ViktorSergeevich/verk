<template>
  <footer class="footer">
    <div class="footer__container">
      <div class="footer__title">Следите за новостями</div>
      <div class="footer__links">
        <div class="footer__link">VK</div>
        <div class="footer__link">Insta</div>
        <div class="footer__link">Telega</div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'Footer',
}
</script>

<style scoped>
.footer {
  position: fixed;
  bottom: 0;
  width: 100%;
  overflow: hidden;
}

.footer__container {
  display: flex;
  align-items: center;
  height: 100%;
  max-width: 80%;
  margin: 0 auto;
}

.footer__title {
  color: #fff;
}

.footer__links {
  display: flex;
  align-items: center;
  margin-left: 25px;
  color: #fff;
}

.footer__link {
  margin-left: 15px;
}
</style>