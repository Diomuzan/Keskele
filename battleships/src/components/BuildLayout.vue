<template>
  <h1>hello</h1>

  <div id="container">
    <div class="grid-item">Test</div>
  </div>
</template>

<script>

export default {
  name: "BuildLayout",
  data(){
    return{
      test:0,
    }
  },
  methods:{
    LayoutJs(){
      const container = document.getElementById("container");

      function makeRows() {
        for ( let c = 0; c < (7 * 7); c++) {
          let cell = document.createElement("div");
          cell.innerText = (c + 1);
          container.appendChild(cell).className = "grid-item";
        }
      }
      makeRows();
    }
  }
}
</script>

<style scoped>
:root {
  --grid-cols: 7;
  --grid-rows: 7;
}

#container {
  display: grid;
  grid-gap: 1em;
  grid-template-rows: repeat(var(--grid-rows), 1fr);
  grid-template-columns: repeat(var(--grid-cols), 1fr);
}

.grid-item {
  padding: 1em;
  border: 1px solid #ddd;
  text-align: center;
}
</style>