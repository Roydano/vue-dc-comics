<template>
  <div id="app">
    <Header/>

    <!-- <main>
      <Content/>
      <ShopAction/>
    </main>

    <footer>
      <FooterTop/>
      <FooterBottom/>
    </footer> -->

  </div>
</template>

<script>
import Header from './components/Header.vue'

export default {
  name: 'App',
  components: {
    Header
  }
}
</script>

<style lang="scss">
  @import 'style/commons.scss'
</style>
