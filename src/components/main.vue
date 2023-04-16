<script>
export default{
    name: "AppMain",
    data(){
        return{

        }
    }
}
</script>
<template>
    <section>
        <main>
            <div class="wrapper">
                <span>content goes here</span>
            </div>
        </main>
    </section>
</template>
<style scoped lang="scss">
@use "../assets/styles/mixin.scss" as*;
@use "../assets/styles/variables.scss" as*;

    section{
        background-color: $main-bg;
        main{
        font-size: 20px;
        color: #fff;
        }
    }
    
</style>