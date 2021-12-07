<template>
  <div id="app">
    <HelloWorld
    v-on:delete-item="deleteAdat"
    />
    <table>
      <thead>
        <tr>
        <th>Termék</th>
        <th>Ár</th>
        <th>Mennyiség</th>
        <th>Operations</th>
        <th>Összérték</th>
      </tr>
      </thead>
      <tbody>
        <tr v-for="row in rows"
            v-bind:key="row.title">
            <td>{{row.title}}</td>
            <td>{{row.price}}</td>
            <td>{{row.quantity}}</td>
            <td>
              <button>Módosít</button>
              <button v-on:click="deleteItem">X</button>
            </td>
          <td>{{ row.price * row.quantity }} </td>
        </tr>
        
        <td>
              <input type="text" v-model="title" placeholder="Név">
            </td>
            <td>
              <input type="number" v-model="price" placeholder="Ár">
            </td>
            <td>
              <input type="number" v-model="quantity" placeholder="Darabszám">
            </td>
            <button v-on:click="Hozzaad">Hozzáad</button>

      </tbody>
    </table>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
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
  },
  methods: {
    deleteAdat(row) {
      this.rows = this.rows.filter(function(item){
        return row.title != item.title
      })
    }
  },
  Hozzaad(){
    this.$$emit('item-post',{
      new:{
        title:this.title,
        price:this.price,
        quantity:this.quantity
      }
    })
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
