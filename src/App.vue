<template>
  <div id="app">
    <Header/>

    <main>
      <Content/>
      <!-- <ShopAction/> -->
    </main>

    <!-- <footer>
      <FooterTop/>
      <FooterBottom/>
    </footer> -->

  </div>
</template>

<script>
import Header from './components/Header.vue';
import Content from './components/Content.vue'


export default {
  name: 'App',
  components: {
    Header,
    Content
  }
}
</script>

<style lang="scss">
  @import 'style/commons.scss';
</style>
