<template>
<div id="app">
    <Navbar />
    <Header />
</div>
</template>

<script>
import Header from './components/Header.vue'
import Navbar from './components/Navbar.vue'

export default {
    name: 'App',
    components: {
        Header,
        Navbar
    }
}
</script>

<style lang="scss">
#app {
    font-family: Open Sans;
    margin: -9px;
    min-width: 1280px;

    //   -webkit-font-smoothing: antialiased;
    //   -moz-osx-font-smoothing: grayscale;
    //   text-align: center;
    //   color: #2c3e50;
    //   margin-top: 60px;
}
</style>
