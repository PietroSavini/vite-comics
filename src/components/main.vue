<script>
export default{
    name: "AppMain",
    data(){
        return{
            thumbs:[
                {
                    thumb: 'https://www.coverbrowser.com/image/action-comics/1-1.jpg',
                    price: '$19.99',
                    series: 'Action Comics',
                    type: 'comic book',
                },
                {
                    thumb: 'https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg',
                    price: '$3.99',
                    series: 'American Vampire 1976',
                    type: 'comic book',
                },
                {
                    thumb: 'https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg',
                    price: '$16.99',
                    series: 'Aquaman',
                    type: 'graphic novel',
                },
                {
                    thumb: 'https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg',
                    price: '$2.99',
                    series: 'Batgirl',
                    type: 'comic book',
                },
                {
                    thumb: 'https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg',
                    price: '$3.99',
                    series: 'Batman',
                    type: 'comic book',
                },
                {
                    thumb: 'https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg',
                    price: '$2.99',
                    series: 'Batman Beyond',
                    type: 'comic book',
                },
                {
                    thumb: 'https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg',
                    price: '$3.99',
                    series: 'Batman/Superman',
                    type: 'comic book',
                },
                {
                    thumb: 'https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg',
                    price: '$4.99',
                    series: 'Batman/Superman Annual',
                    type: 'comic book',
                },
                {
                    thumb: 'https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg',
                    price: '$5.99',
                    series: 'Batman: The Joker War Zone',
                    type: 'comic book',
                },
                {
                    thumb: 'https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg',
                    price: '$6.99',
                    series: 'Batman: Three Jokers',
                    type: 'comic book',
                },
                {
                    thumb: 'https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg',
                    price: '$4.99',
                    series: 'Batman: White Knight Presents: Harley Quinn',
                    type: 'comic book',
                },
                {
                    thumb: 'https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg',
                    price: '$16.99',
                    series: 'Catwoman',
                    type: 'graphic novel',
                },
            ]
        }
    }
}
</script>
<template>
    <div class="jumbotron"></div>
    <section>
        <main>
            <div class="wrapper">
                <span class="current-series">CURRENT SERIES</span>
                <div class="row">
                    <div class="col" v-for="thumbnail in thumbs">
                        <div class="card">
                            <div class="card-img">
                                <img :src="thumbnail.thumb" alt="">
                            </div>
                            <div class="card-content">
                                <p>{{thumbnail.series}}</p>
                                <span>{{thumbnail.price}}</span>
                            </div>
                        </div>
                    </div>
                </div>
                <span class="btn">LOAD MORE</span>
            </div>
        </main>
    </section>
</template>
<style scoped lang="scss">
@use "../assets/styles/mixin.scss" as*;
@use "../assets/styles/variables.scss" as*;

    .jumbotron{
        width: 100%;
        background-image: url(../assets/jumbotron.jpg);
        background-repeat: no-repeat;
        background-size: cover;
        height: 400px;
        z-index: 1;
    }
    section{
        background-color: $main-bg;
        .wrapper{
            position: relative;
            padding-top: 2rem;
            z-index: 2;
            .current-series{
                z-index: 3;
                top: -60px;
                position: absolute;
                padding: .7rem 1.5rem;
                background-color: $primary;
                color: #fff;
                font-weight: 700;
                font-size: 25px;
                box-shadow: 0 0 10px black;
            }
            .btn{
                display: inline-block;
                padding: .7rem 1.5rem;
                background-color: $primary;
                color: #fff;
                font-weight: 700;
                font-size: 15px;
                box-shadow: 0 0 10px black;
                margin-left: 50%;
                //non chidedtemi perchè non funziona il margin 0 auto //////////////////////////////////////////////////////////////
                transform: translateX(-50%);
                transition: 200ms;
                cursor: pointer;
                &:hover{
                    transform: scale(1.1) translateX(-45%);
                }
            }
            .row{
                width: 100%;
                padding: 0 .5rem;
                @include flex (row, center, center );
                flex-wrap: wrap;
                margin-bottom: 1.5rem;
                .col{
                    width: calc(100% / 6);
                    min-width: 170px;
                    padding: .5rem .5rem;
                    max-height: 300px;
                    margin-bottom: 20px;
                    cursor: pointer;
                    .card{
                        color: #fff;
                        transition: 200ms;
                        @include flex(column,normal,center);
                        &:hover{
                            transform: scale(1.1);
                        }
                        .card-img{
                            height: 250px;
                            margin-bottom: 10px;
                            overflow: hidden;
                            img{
                                display: block;
                                object-fit: cover;
                                width: 100%;
                                height: 100%;
                            }
                        }
                        .card-content{
                            width: 100%;
                            max-height: 40px;
                            @include flex(row, space-between,center);
                            padding: .5rem .3rem .5rem 0;
                            gap:10px;

                            p{
                                font-size: .8rem;
                            }
                            span{
                                font-size: .9rem;
                                color: rgb(255, 234, 0);
                            }
                        }
                    }
                }
            }
        }
    }
    
</style>