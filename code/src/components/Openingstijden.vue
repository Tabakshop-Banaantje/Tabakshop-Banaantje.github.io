<template>
    <div id="openingstijden">
        <div id="title">Openingstijden</div>
        <div class="table">
            <div class="row" v-for="tijd in tijden" v-bind:key="tijd.dag">
                <div class="dag cell">{{tijd.dag}}</div>
                <div class="open cell">{{tijd.open}}</div>
                <div class="divider cell"> -</div>
                <div class="sluit cell">{{tijd.sluit}}</div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "Openingstijden",
        data() {
            return {
                tijden: [
                    {dag: "Maandag", open: "11:00", sluit: "21:00"},
                    {dag: "Dinsdag", open: "11:00", sluit: "21:00"},
                    {dag: "Woensdag", open: "11:00", sluit: "21:00"},
                    {dag: "Donderdag", open: "11:00", sluit: "21:00"},
                    {dag: "Vrijdag", open: "11:00", sluit: "21:00"},
                    {dag: "Zaterdag", open: "11:00", sluit: "21:00"},
                    {dag: "Zondag", open: "11:00", sluit: "21:00"}]
            }
        }
    }
</script>

<style scoped>
    #openingstijden {
        flex-grow: 1;
        display: flex;
        flex-direction: column;

        border: 1px solid black;
        text-align: start;
        padding: 15px;
        margin: 0;
    }

    .table{
        display: table;
        padding: 0;
        margin: 0;
    }
    .row {
        display: table-row;
    }

    .cell:not(:first-child) {
        display: table-cell;
        padding-left: 15px;
    }


    .divider {

    }

    .dag {
        font-weight: bold;
    }
</style>