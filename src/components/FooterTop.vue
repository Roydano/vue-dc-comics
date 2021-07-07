<template>
    <section class="footground">
        <div class="container">
            <div class="link-list">
                <h3>dc comics</h3>
                <ul>
                    <li v-for="(list, index) in dcComics" :key="index" ><a :href="list.url">{{list.link}}</a></li>
                </ul>
            </div>
            <div class="dc-logo"></div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'FooterTop',
    
    data(){
        return{
            dcComics: [
                {
                    link: 'Characters', 
                    url: '#'
                },
                {
                    link: 'Comics', 
                    url: '#'
                },
                {
                    link: 'Movies', 
                    url: '#'
                },
                {
                    link: 'TV', 
                    url: '#'
                },
                {
                    link: 'Games', 
                    url: '#'
                },
                {
                    link: 'Videos', 
                    url: '#'
                },
                {
                    link: 'News', 
                    url: '#'
                },
            ],
            

        }
    }
}
</script>

<style lang="scss" scoped>
    @import '../style/var.scss';

    .footground{
        background-image: url(../assets/img/footer-bg.jpg);

        h3{
            color: white;
            text-transform: uppercase;
        }

        li{
            list-style: none;

            a{
                text-decoration: none;
                color: $secondary-color;
            }
        }
    }

</style>





 