<template>
  <section>
      <div class="jumbotron"></div>

      <div class="btn-series">
           <button>current series</button>
      </div>

      <div class="container flex">  
          <div v-for="(card, index) in cards" :key="index" class="card-container">
              <DcCard  :link="card"/>
          </div>
      </div>

      
      <div class="btn">
          <button>load more</button>
      </div>

  </section>
</template>

<script>
import DcCard from '@/components/DcCard.vue';
import CardSeries from '@/data/CardSeries.js';

export default {
    name: 'Content',
    components: {
        DcCard
    },

    data(){
        return{
            cards: CardSeries,
        }
    }
}
</script>

<style lang="scss" scoped>
    @import '../style/var.scss';
    @import '../style/mixin.scss';

    section{
        background-color: $black-ground;

        .jumbotron{
            width: 100%;
            height: 400px;
            background-image: url(../assets/img/jumbotron.jpg);
            background-size: cover;
        }

        .btn-series{
            position: relative;
            button{
                padding: 10px 20px;
                position: absolute;
                top: -20px;
                left: 220px;
                @include button($primary-color, 16px)

            }

        }

        .flex{
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
        }

        .card-container{
            padding: 20px;
            width: calc((100% / 6) * 1);

            img{
                width: 100%;
            }

        }

        .btn{
            display: flex;
            justify-content: center;
            padding: 15px;
            button{
                padding: 10px 35px;
                @include button($primary-color, 10px)
                
            }
        }
    }

</style>