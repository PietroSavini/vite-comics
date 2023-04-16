<script>
    export default{
        data(){
            name: "Store"
            return{
                buy:[
                    {
                        title: "DIGITAL COMICS",
                        img: "comics-digital-comics.png"
                    },
                    {
                        title: "DC MERCHANDISE",
                        img: "comics-merchandise.png"
                    },
                    {
                        title: "SUBSCRIPTION",
                        img: "comics-subscriptions.png"
                    },
                    {
                        title: "COMIC SHOP LOCATOR",
                        img: "comics-shop-locator.png"
                    },
                    {
                        title: "DC POWER VISA",
                        img: "dc-power-visa.svg"
                    },
                ]
            }
        }
    }
</script>

<template>
    <section>
        <div class="wrapper">
            <ul class="row">
                <a href="#" v-for="card in buy">
                    <li>
                        <img :src="`../src/assets/buy-`+ card.img" :alt="card.title">
                        <p>{{ card.title }}</p>
                    </li>
                </a>
            </ul>
        </div>
    </section>
</template>
<style scoped lang="scss">
@use "../assets/styles/mixin.scss" as*;
@use "../assets/styles/variables.scss" as*;

    section{
        background-color: $primary ;
        .row{
            @include flex(row,space-between,center);
            padding: 1rem 2rem;
            li{
                min-height: 100%;
                color: #fff;
                object-fit: cover;
                display: flex;
                align-items: center;
                min-width: 150px;
                margin-right: 10px;
                transition:200ms;
                &:hover{
                    transform: scale(1.2);
                    filter: drop-shadow(0 0 .5rem rgb(0, 0, 0));
                }
                img{
                    width: 50px;
                    height: 50px;
                    object-fit: contain;
                    margin-right: 5px ;
                }
                p{
                    font-size: .7rem;
                }
            }
        }
    }
</style>