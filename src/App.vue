<template>
  <div id="app">
    <div class="container">
      <div class="row">
        <div class="col-12">
          <TablePacientes msg="Tabla de pacientes" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import TablePacientes from "./components/TablePacientes.vue";

export default {
  name: "App",
  components: {
    TablePacientes,
  },
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 40px;
}
</style>
