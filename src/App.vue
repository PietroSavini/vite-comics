<script>
    import Header from "./components/header.vue";
    import AppMain from "./components/main.vue";
    import Store from "./components/store.vue";
    import Footer from "./components/footer.vue";
    export default {
        components:{
            Header,
            AppMain,
            Store,
            Footer,
        }
    }
</script>

<template>
    <Header />
    <AppMain />
    <Store />
    <Footer />
</template>

<style scoped>

</style>
