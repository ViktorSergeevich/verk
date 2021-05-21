<template>
  <div id="app">
    <div class="wrapper">
      <div class="header">
        <Header
          @set-content="getContent"
        />
      </div>
      <div class="content">
        <Asytp v-if="showASYTP"/>
        <Po v-if="showOP"/>
        <Interface v-if="showInterface"/>
        <Dev v-if="showDev"/>
      </div>
      <div class="footer">
        <Footer/>
      </div>
    </div>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'
import Asytp from './components/Asytp.vue'
import Po from './components/PO.vue'
import Interface from './components/Interface.vue'
import Dev from './components/Dev.vue'

export default {
  name: 'App',
  components: {
    Header,
    Footer,
    Asytp,
    Po,
    Interface,
    Dev,
  },
  data() {
    return {
      showASYTP: true,
      showOP: false,
      showInterface: false,
      showDev: false,
    }
  },
  methods: {
    getContent(indexPage) {
      if (indexPage === 'ASTP') {
        this.showASYTP = true
        this.showOP = false
        this.showInterface = false
        this.showDev = false
      } else if (indexPage === 'PO') {
        this.showASYTP = false
        this.showOP = true
        this.showInterface = false
        this.showDev = false
      } else if (indexPage === 'Interface') {
        this.showASYTP = false
        this.showOP = false
        this.showInterface = true
        this.showDev = false
      } else if (indexPage === 'Dev') {
        this.showASYTP = false
        this.showOP = false
        this.showInterface = false
        this.showDev = true
      }
    }
  }
}
</script>

<style scoped>
.wrapper {
  height: 100%;
  max-height: 100vh;
}

.header {
  position: fixed;
  height: 60px;
  width: 100%;
  background-color: rgba(40, 56, 107, 1);
}

.content {
  padding: 60px 0;
}

.footer {
  position: fixed;
  height: 60px;
  width: 100%;
  bottom: 0;
  background-color: rgba(40, 56, 107, 1);
}
</style>
