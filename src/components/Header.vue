<template>
  <header>
      <div class="container">
          
          <a href="#">
              <img src="../assets/img/dc-logo.png" alt="logo dc-comics">
          </a>

          <ul>
              <li v-for="(link, index) in linkMenu" :key="index"><a href="link.url">{{link.text}}</a></li>
          </ul>

      </div>
  </header>
</template>

<script>
export default {
    name: 'Header',
    data(){
        return{
            linkMenu:[
                {
                    text: 'characters',
                    url: '#',
                    current: false
                },
                {
                    text: 'comics',
                    url: '#',
                    current: true
                },
                {
                    text: 'movies',
                    url: '#',
                    current: false
                },
                {
                    text: 'tv',
                    url: '#',
                    current: false
                },
                {
                    text: 'games',
                    url: '#',
                    current: false
                },
                {
                    text: 'collectibles',
                    url: '#',
                    current: false
                },
                {
                    text: 'videos',
                    url: '#',
                    current: false
                },
                {
                    text: 'fans',
                    url: '#',
                    current: false
                },
                {
                    text: 'news',
                    url: '#',
                    current: false
                },
                {
                    text: 'shop',
                    url: '#',
                    current: false
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>

</style>