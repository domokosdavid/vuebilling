<template>
  <div class="hello">
    <table>
      <tr>
        <th>{{msg.title}}</th>
      </tr>
      <tr>
        <td>{{msg.price}}</td>
      </tr>
      <tr>
        <td>{{msg.quantity}}</td>
      </tr>
    </table>
    
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
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
