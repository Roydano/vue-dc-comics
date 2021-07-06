<template>
  <header>
      <div class="container flex">
          
          <a href="#">
              <img src="../assets/img/dc-logo.png" alt="logo dc-comics">
          </a>

          <ul>
              <li v-for="(link, index) in linkMenu" :key="index"><a href="link.url" :class="{active: link.current}">{{link.text}}</a></li>
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
    @import '../style/var.scss';

    header{
        height: 80px;
    }

    .flex{
        display: flex;
        justify-content: space-between;
        align-items: center;
        text-align: center;
    }

    img{
        padding: 10px;
        width: 60%;
    }

    li{
        list-style: none;
        display: inline-block;
        padding: 10px;

        a{
        padding-bottom: 27px;
        text-decoration: none;
        text-transform: uppercase;
        font-size: 12px;
        font-weight: bold;
        color: $terziary-color;

            &:hover{
                color: $primary-color;
            }

            &.active{
                color: $primary-color;
                border-bottom: 5px solid $primary-color;
            }
        }

    }
    

    




</style>