<template>
  <div id="openingstijden">
    <div id="title">Openingstijden</div>
    <div class="table">
      <div class="row" v-for="tijd in tijden" v-bind:key="tijd.dag">
        <div class="dag cell">{{ tijd.dag }}</div>
        <div class="open cell">{{ tijd.open }}</div>
        <div class="divider cell"> -</div>
        <div class="sluit cell">{{ tijd.sluit }}</div>
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
        { dag: "Maandag", open: "10:00", sluit: "20:00" },
        { dag: "Dinsdag", open: "10:00", sluit: "20:00" },
        { dag: "Woensdag", open: "10:00", sluit: "20:00" },
        { dag: "Donderdag", open: "10:00", sluit: "20:00" },
        { dag: "Vrijdag", open: "10:00", sluit: "20:00" },
        { dag: "Zaterdag", open: "10:00", sluit: "20:00" },
        { dag: "Zondag", open: "12:00", sluit: "20:00" }]
    }
  }
}
</script>

<style scoped>
#openingstijden {
  text-align: start;


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

.table {
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