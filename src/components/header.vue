<script >
    export default {
        name:"Header",
        data(){
            return{
                links: [
                    {
                        text: "CHARACTERS",
                        url: "",
                        active: false,
                    },
                    {
                        text: "COMICS",
                        url: "",
                        active: false,
                    },
                    {
                        text: "MOVIES",
                        url: "",
                        active: false,
                    },
                    {
                        text: "TV",
                        url: "",
                        active: false,
                    },
                    {
                        text: "GAMES",
                        url: "",
                        active: false,
                    },
                    {
                        text: "COLLECTIBLES",
                        url: "",
                        active: false,
                    },
                    {
                        text: "VIDEOS",
                        url: "",
                        active: false,
                    },
                    {
                        text: "FANS",
                        url: "",
                        active: false,
                    },
                    {
                        text: "NEWS",
                        url: "",
                        active: false,
                    },
                    {
                        text: "SHOP",
                        url: "",
                        active: false,
                    },

                ]
            }
            
        }
    }
</script>

<template>
    <header>
        <div class="wrapper">
            <a href=""><img src="../assets/dc-logo.png" alt="DC-logo.png"></a>
            <div>
                <nav>
                    <ul>
                        <li v-for="link in links"><a href="#">{{ link.text }}</a></li>
                    </ul>
                </nav>
            </div>
        </div> 
    </header>
</template>

<style scoped lang="scss">
@use "../assets/styles/mixin.scss" as*;
@use "../assets/styles/variables.scss" as*;

    header{
        background-color: #fff;
        height: 150px;
        .wrapper{
            height: 100%;
            @include flex (row, space-between, center);
            img{
                min-width: 103px;
            }
            ul{
                @include flex(row,space-between,center);
                height: 150px;
                li{
                height: 100%;
                line-height: 150px;
                padding: 0 .5rem;
                min-width: 50px;
                text-align: center;
                    &:hover{
                        border-bottom: 5px solid $primary;
                        color: $primary;
                    }
                    
                }
            }
        }
    }
</style>
