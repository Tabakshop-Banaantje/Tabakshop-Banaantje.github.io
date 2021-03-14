<template>
    <div id="gegevens">
        <div id="titel">Gegevens</div>
        <div v-for="gegeven in gegevens" v-bind:key="gegeven.titel">
            <div class="gegeven">{{gegeven.titel}}:</div>
            <div v-for="waarde in gegeven.waardes" v-bind:key="waarde">
                {{waarde}}
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "Gegevens",
        data() {
            return {
                gegevens: [
                    {
                        titel: "Adres",
                        waardes: ["Polderlaan 9B",
                            "3074 MA Rotterdam"]
                    }
                ]
            }
        }
    }
</script>

<style scoped>
    #titel{
    }
    #gegevens>div:not(:last-child){
        margin-bottom: 10px;
    }
    #gegevens{
      flex-grow: 1;
      display: flex;
      flex-direction: column;
      border: 1px solid black;
      border-radius: 10px;
      background: #000000c2;
      color: white;
      padding: 15px;
      margin: 0;
    }
    .gegeven {
        font-weight: bold;
    }
</style>
