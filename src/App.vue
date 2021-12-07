<template>
  <div id="app">
    <table>
      <thead>
        <tr>
        <th>Termék</th>
        <th>Ár</th>
        <th>Mennyiség</th>
        <th>Operations</th>
      </tr>
      </thead>
      <tbody>
        <tr v-for="row in rows"
            v-bind:key="row.title">
            <td>{{row.title}}</td>
            <td>{{row.price}}</td>
            <td>{{row.quantity}}</td>
            <td>
              <button>Törlés</button>
              <button>Módosít</button>
            </td>
        </tr>

      </tbody>
    </table>
  </div>
</template>

<script>


export default {
  name: 'App',
  components: {

  },
  data() {
    return {
      rows: [
        {
          title: 'Kerék',
          price: 100,
          quantity: 12
        },
        {
          title: 'Teleszkóp',
          price: 1000,
          quantity: 300
        },
        {
          title: 'Kormány',
          price: 230,
          quantity: 5
        },
        {
          title: 'Ajtó',  
          price: 45120,
          quantity: 321
        },
      ]
    }
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
