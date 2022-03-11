<template>
  <div>
    <h1 class="mb-5">{{ msg }}</h1>
    <table class="table">
      <thead>
        <tr>
          <th scope="col">#</th>
          <th scope="col">Nombre</th>
          <th scope="col">Edad</th>
          <th scope="col">Rut</th>
          <th scope="col">Diagnóstico</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(paciente, i) in pacientes" :key="i">
          <th>{{ i + 1 }}</th>
          <td>{{ paciente.nombre }}</td>
          <td>{{ paciente.edad }}</td>
          <td>{{ paciente.rut }}</td>
          <td>{{ paciente.diagnostico }}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  name: "TablePacientes",
  data() {
    return {
      pacientes: [
        {
          nombre: "Jess González",
          edad: 32,
          rut: "18.522.901-7",
          diagnostico: "Problemas para decidir qué ponerse para salir",
        },
        {
          nombre: "Islebi Pinto",
          edad: 31,
          rut: "17.737.695-7",
          diagnostico: "Cansancio terminal",
        },
        {
          nombre: "Marco Felina",
          edad: 14,
          rut: "22.737.901-7",
          diagnostico: "Embarazo adolescente",
        },
        {
          nombre: "Molotov Gatuso",
          edad: 1,
          rut: "22.522.695-9",
          diagnostico: "Hiperactividad",
        },
      ],
    };
  },
  props: {
    msg: String,
  },
};
</script>

<style></style>
