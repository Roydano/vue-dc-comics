<template>
  <div class="foot-bottom">
      <div class="container flex">
          <div class="signup">
              <button>sign-up now!</button>
          </div>
          <div class="social">
              <h3>follow Us</h3>
              <div v-for="(item, index) in social" :key="index" class="social-network">
                  <img :src="getItem(item.img)" :alt="item.alt">
              </div>

          </div>
      </div>
  </div>
</template>

<script>
export default {
    name: 'FooterBottom',

    data(){
        return{
            social: [
                {
                    img:'img/footer-facebook.png',
                    url:'#',
                    title: 'facebook',
                    alt: 'facebook-icon'
                },
                {
                    img:'img/footer-twitter.png',
                    url:'#',
                    title: 'twitter',
                    alt: 'twitter-icon'
                },
                {
                    img:'img/footer-youtube.png',
                    url:'#',
                    title: 'youtube',
                    alt: 'youtube-icon'
                },
                {
                    img:'img/footer-pinterest.png',
                    url:'#',
                    title: 'pinterest',
                    alt: 'pinterest-icon'
                },
                {
                    img:'img/footer-periscope.png',
                    url:'#',
                    title: 'periscope',
                    alt: 'periscope-icon'
                },
            ]
        }
    },

    methods: {
        getItem(item) {
            return require('../assets/'+ item);
        }
    }

}
</script>

<style lang="scss" scoped>
    @import '../style/var.scss';

    .foot-bottom{
        background-color: $footer-bg;

        button{
            text-transform: uppercase;
            padding: 10px 15px;
            color: white;
            background-color: $footer-bg;
            border-color: $primary-color;
            cursor: pointer;
        }

        .flex{
        display: flex;
        justify-content: space-between;
        align-items: center;
        height: 100px;

        }

        .social{
            display: flex;
            align-items: center;

            h3{
                color: $primary-color;
                text-transform: uppercase;
                padding: 0 15px;
            }

            img{
                padding: 0 10px;
                cursor: pointer;
            }
        }
    }

</style>