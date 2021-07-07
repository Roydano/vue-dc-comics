<template>
  <section>
      <div class="container flex">
          <div class="action" v-for="(card, index) in cards" :key="index">
              <a :href="card.url">
                  <img :src="getCard(card.img)" :alt="card.alt">
              </a>
              <a href="#">{{card.title}}</a>
          </div>
      </div>
  </section>
</template>

<script>
export default {
    name:'ShopAction',
    data(){
        return{

            cards:[
                {
                    img: 'img/buy-comics-digital-comics.png',
                    url: '#',
                    alt: 'digital comics',
                    title: 'digital comics'
                },
                {
                    img: 'img/buy-comics-merchandise.png',
                    url: '#',
                    alt: 'dc merchandise',
                    title: 'dc merchandise'
                },
                {
                    img: 'img/buy-comics-subscriptions.png',
                    url: '#',
                    alt: 'subscription',
                    title: 'subscription'
                },
                {
                    img: 'img/buy-comics-shop-locator.png',
                    url: '#',
                    alt: 'comic shop locator',
                    title: 'comic shop locator'
                },
                {
                    img: 'img/buy-dc-power-visa.png',
                    url: '#',
                    alt: 'dc power visa',
                    title: 'dc power visa'
                }
            ]
        }
    },
    
    methods: {
        getCard(card) {
            return require('../assets/'+ card);
        }
    }
}



</script>

<style lang="scss" scoped>
    @import '../style/var.scss';

    section{
        background-color: $primary-color;
        text-align: center;
        height: 120px;
    }

    .flex{
        display: flex;
        height: 100%;
        justify-content: space-between;
    }

    .action{

        img{
            width: 15%;
            vertical-align: middle;

        }

        a{

        line-height: 120px;
        text-decoration: none;
        text-transform: uppercase;
        font-size: 12px;
        color: white;
        padding: 5px;
        }

    }

    

</style>



        
