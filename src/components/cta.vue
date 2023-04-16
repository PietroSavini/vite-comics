<script>
    export default{
        data(){
            return{
                name : "CTA",
                ctaComponents:[
                    {
                        img:"../src/assets/footer-facebook.png"
                    },
                    {
                        img:"../src/assets/footer-periscope.png"
                    },
                    {
                        img:"../src/assets/footer-pinterest.png"
                    },
                    {
                        img:"../src/assets/footer-twitter.png"
                    },
                    {
                        img:"../src/assets/footer-youtube.png"
                    },
                ]
            }
        }
    }
</script>

<template>
    <section>
        <div class="wrapper">
            <div class="col left">
                <a href="#"><span>SING-UP NOW!</span></a>
            </div>
            <div class="col right">
                <ul>
                    <h3>FOLLOW US</h3>
                    <li v-for="item in ctaComponents">
                        <a href="#"><img :src="item.img" alt=""></a>
                    </li>
                </ul>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
    @use "../assets/styles/mixin.scss" as*;
    @use "../assets/styles/variables.scss" as*;
    
    section{
        background-color: $cta-bg;
        .wrapper{
            @include flex(row,space-between,center);
            .left{
                width: 50%;
                text-align: left;
                span{
                    display: inline-block;
                    color: #fff;
                    font-weight: 700;
                    border:1px solid $primary;
                    padding: .7rem 1rem;
                    transition: 200ms;
                    cursor: pointer;
                    &:hover{
                        transform: scale(1.1);
                        background : linear-gradient(rgb(15, 121, 191),rgba(2, 37, 144, 0.678) );
                        margin-left: 5px;
                        border-color: #fff;
                    }
                }
            }
            .right{
                width: 50%;
                text-align: right;
                color: $primary;
                ul{
                    @include flex(row, center,center);
                    gap:10px;
                    h3{
                        margin-right: 10px;
                    }
                    img{
                        transition: 200ms;
                        &:hover{
                        transform: scale(1.1);
                        }
                    }
                }
            }
        }
    }
</style>