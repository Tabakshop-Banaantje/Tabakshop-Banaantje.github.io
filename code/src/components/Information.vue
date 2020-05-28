<template>
    <div id="information">
        <Gegevens/>
        <div class="seperator"></div>
        <Openingstijden/>

    </div>
</template>

<script>
    import Openingstijden from "./Openingstijden";
    import Gegevens from "./Gegevens";

    export default {
        name: "Footer",
        components: {Gegevens, Openingstijden}
    }
</script>

<style scoped>
    #information {
        display: flex;
        flex-direction: column;
        width: 500px;
        margin: 0 auto;
    }
    .seperator{
        width: 20px;
        height: 20px;
    }
</style>