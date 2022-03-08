<template>
  <div>
    <h1>{{ msg }}</h1>
    <div class="container">
      <div class="row">
        <div class="col">
          <table class="table mt-5">
            <thead>
              <tr>
                <th scope="col">#</th>
                <th scope="col">Nombre</th>
                <th scope="col">Apellido</th>
                <th scope="col">RUN</th>
                <th scope="col">Nacimiento</th>
                <th scope="col">Edad</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <th scope="row">1</th>
                <td>Jose</td>
                <td>Pérez</td>
                <td>123456-2</td>
                <td>12-04-67</td>
                <td>57</td>
              </tr>
              <tr>
                <th scope="row">2</th>
                <td>María</td>
                <td>Rodríguez</td>
                <td>654321-1</td>
                <td>30-11-90</td>
                <td>30</td>
              </tr>
              <tr>
                <th scope="row">3</th>
                <td>Manuel</td>
                <td>Patiño</td>
                <td>14223456-6</td>
                <td>02-12-59</td>
                <td>62</td>
              </tr>
            </tbody>
          </table>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "TableComponente",
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
