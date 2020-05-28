<template>
    <div id="app">
        <Header/>
        <Information/>
    </div>
</template>

<script>

    import Header from "./components/Header";
    import Information from "./components/Information";

    export default {
        name: 'App',
        components: {
            Information,
            Header
        }
    }
</script>

<style>
    #app {
        font-family: Avenir, Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: center;
        color: #2c3e50;
        margin-top: 60px;
    }
</style>
