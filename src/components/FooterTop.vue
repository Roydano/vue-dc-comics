<template>
    <section class="footground">
        <div class="container flex">
            <div class="link-list">
                <h3>dc comics</h3>
                <ul>
                    <li v-for="(list, index) in dcComics" :key="index" ><a :href="list.url">{{list.link}}</a></li>
                </ul>

                <h3>shop</h3>
                <ul>
                    <li v-for="(list, index) in shop" :key="index" ><a :href="list.url">{{list.link}}</a></li>
                </ul>
            </div>
            <div class="link-list">
                <h3>dc</h3>
                <ul>
                    <li v-for="(list, index) in dc" :key="index" ><a :href="list.url">{{list.link}}</a></li>
                </ul>
            </div>
            <div class="link-list">
                <h3>sites</h3>
                <ul>
                    <li v-for="(list, index) in sites" :key="index" ><a :href="list.url">{{list.link}}</a></li>
                </ul>
            </div>
            <div class="dc-logo flex">
                <img src="@/assets/img/dc-logo-bg.png" alt="">
            </div>
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

            shop: [
                {
                   link: 'Shop DC',
                   url: '#' 
                },
                {
                    link: 'Shop DC Collectibles',
                    url:'#'
                }
            ],

            dc: [
                {
                   link: 'Term of Use',
                   url: '#' 
                },
                {
                   link: 'Privacy policy (New)',
                   url: '#' 
                },
                {
                   link: 'Ad Choices',
                   url: '#' 
                },
                {
                   link: 'Advertising',
                   url: '#' 
                },
                {
                   link: 'Jobs',
                   url: '#' 
                },
                {
                   link: 'Subscriptions',
                   url: '#' 
                },
                {
                   link: 'Talent Workshops',
                   url: '#' 
                },
                {
                   link: 'CPSC Certificates',
                   url: '#' 
                },
                {
                   link: 'Ratings',
                   url: '#' 
                },
                {
                   link: 'Shop Help',
                   url: '#' 
                },
                {
                   link: 'Contact Us',
                   url: '#' 
                },
            ],

            sites: [
                {
                   link: 'DC',
                   url: '#' 
                },
                {
                   link: 'MAD Magazine',
                   url: '#' 
                },
                {
                   link: 'DC Kids',
                   url: '#' 
                },
                {
                   link: 'DC Universe',
                   url: '#' 
                },
                {
                   link: 'DC Power Visa',
                   url: '#' 
                },
            ] 

        }
    }
}
</script>

<style lang="scss" scoped>
    @import '../style/var.scss';

    .footground{
        background-image: url(../assets/img/footer-bg.jpg);
        height: 400px;
        overflow: hidden;

       .link-list{
           padding: 20px 0 60px;
           width: 100%;
           
            h3{
            color: white;
            text-transform: uppercase;
            margin: 15px 0;
            }

            li{
            list-style: none;

                a{
                text-decoration: none;
                color: $secondary-color;
                font-size: 14px;

                &:hover{
                    color: white;
                }
                }
            }
        }

        .dc-logo{
            display: flex;
            justify-content: flex-end;
            align-items: center;
            height: 400px;
            width: 100%;

            img{
                height: 140%;
            }
        }
    }

    .flex{
        display: flex;
    }

</style>





 