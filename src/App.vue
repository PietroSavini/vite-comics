<script>
    import Header from "./components/header.vue";
    import AppMain from "./components/main.vue";
    import Store from "./components/store.vue";
    import Footer from "./components/footer.vue";
    import Cta from "./components/cta.vue"
    export default {
        components:{
            Header,
            AppMain,
            Store,
            Footer,
            Cta,
        }
    }
</script>

<template>
    <Header />
    <AppMain />
    <Store />
    <Footer />
    <Cta />

</template>

<style scoped>

</style>
