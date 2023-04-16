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
            <div class="logo">
                <a href=""><img src="../assets/dc-logo.png" alt="DC-logo.png"></a>
            </div>
            <div>
                <ul>
                    <li v-for="link in links"><a href="">{{ link.text }}</a></li>
                </ul>
            </div>
        </div> 
    </header>
</template>

<style scoped>
    
</style>
