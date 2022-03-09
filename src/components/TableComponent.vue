<template>
  <div>
    <h1>{{ msg }}</h1>
    <h2>{{ notebook.procesador }}</h2>
    <div class="container">
      <div class="row">
        <div class="col">
          <table class="table mt-5">
            <thead>
              <tr>
                <th scope="col">ID</th>
                <th scope="col">Name</th>
                <th scope="col">User name</th>
                <th scope="col">Email</th>
                <th scope="col">Address</th>
                <th scope="col">Phone</th>
                <th scope="col">Website</th>
                <th scope="col">Company</th>
              </tr>
            </thead>
            <tbody>
              <tr v-for="(users, i) in usersDates" :key="i">
                <td>{{ i + 1 }}</td>
                <td>{{ users.name }}</td>
                <td>{{ users.username }}</td>
                <td>{{ users.email }}</td>
                <td>{{ users.address.street + users.address.suite }}</td>
                <td>{{ users.phone }}</td>
                <td>{{ users.website }}</td>
                <td>{{ users.company.name }}</td>
              </tr>
            </tbody>
          </table>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";

export default {
  name: "TableComponente",
  data() {
    return {
      saludo: "Hola mundo(Estoy dentro de Vue)",
      gatos: 2,
      casado: false,
      notebook: {
        procesador: "AMD Ryzen 9 4900H",
      },
      nombreGatos: ["Frijol", "Nieblita"],
      usersDates: [],
    };
  },
  created() {
    // acá estoy invocando
    this.getData();
  },
  methods: {
    async getData() {
      try {
        const URL = "https://jsonplaceholder.typicode.com/users";
        const request = await axios.get(URL);
        this.usersDates = request.data;
      } catch (error) {
        console.error(error);
      }
    },
  },
  props: {
    msg: String,
  },
};
</script>

<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
