<script>
    export default{
        data(){
            return{
                dcLogo: "../src/assets/dc-logo-bg.png",
                name: "footer",
                footerComponents:[
                    {
                     name: "DC COMICS",
                     components:[
                        "characters",
                        "comics",
                        "Movies",
                        "TV",
                        "Games",
                        "Videos",
                        "News",
                     ]
                    },
                    {
                     name: "SHOP",
                     components:[
                        "Shop DC",
                        "Shop DC Collectibles",
                     ]
                    },
                    {
                     name: "DC",
                     components:[
                        "Therms Of Use",
                        "Privacy policy (New)",
                        "Ad Choices",
                        "Advertising",
                        "Jobs",
                        "Subscriptions",
                        "Talent Workshops",
                        "CPSC Certificates",
                        "Ratings",
                        "Shp help",
                        "Contact Us",
                     ]
                    },
                    {
                    name: "Sites",
                    components:[
                        "DC",
                        "MAD Magazine",
                        "DC Kids",
                        "DC Universe",
                        "DC Powre Visa",
                     ]
                    }
                ]
            }
        }
    }
</script>

<template>
    <section>
        <div class="wrapper">
            <div class="row">
                <div class="col left">
                    <div class="footer-col">
                        <ul>
                            <h2>{{ footerComponents[0].name}}</h2>
                            <li v-for="listItem in footerComponents[0].components">
                                <a href=""><p>{{ listItem }}</p></a>
                            </li>
                        </ul>
                        <ul>
                            <h2>{{footerComponents[1].name}}</h2>
                            <li v-for="listItem in footerComponents[1].components">
                                <a href=""><p>{{ listItem }}</p></a>
                            </li>
                        </ul>
                    </div>
                    <div class="footer-col">
                        <ul>
                            <h2>{{ footerComponents[2].name }}</h2>
                            <li v-for="listItem in footerComponents[2].components">
                                <a href=""><p>{{ listItem }}</p></a>
                            </li>
                        </ul>
                    </div>
                    <div class="footer-col">
                        <ul>
                            <h2>{{ footerComponents[3].name }}</h2>
                            <li v-for="listItem in footerComponents[3].components">
                                <a href=""><p>{{ listItem }}</p></a>
                            </li>
                        </ul>
                    </div>
                </div>
                <div class="col right">
                    <img :src="dcLogo" alt="">
                </div>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
    @use "../assets/styles/mixin.scss" as*;
    @use "../assets/styles/variables.scss" as*;
    section{
        background-image: url(../assets/footer-bg.jpg);
        background-repeat: no-repeat;
        background-size: cover;
        z-index: 2;
        overflow: hidden;
        .row{
            width: 100%;
            margin: 0 auto;
            @include flex (row, space-between,center );
            .col{
                height: 100%;
            }
            .left{
                width: 50%;
                display: flex;
                .footer-col{
                    margin-right: 2rem;
                    
                    ul{
                        margin-bottom: 1.5rem;
                        &:hover h2{
                            color:$primary;
                        }
                        h2{
                            color: #fff;
                            margin-bottom: 1rem;
                        }
                        li{
                            margin-bottom: 5px;
                            p{
                                color: $footer-text;
                                &:hover{
                                    color:$primary;
                                }
                            }
                        }
                    } 
                }
            }
            .right{
               min-width: 50%;
                text-align: right;
                position: relative;
                align-self: flex-start;
                img{
                    position: absolute;
                    transform: scale(1.3);
                    min-width: 500px;
                    left: 100px;
                    top: -100px;
                    z-index: 0;
                }
            }
        }
    }
</style>