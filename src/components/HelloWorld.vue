<template>
  <div>
    <table>
      <tr>
      <th>Név</th>
      <th>Ár</th>
      <th>Darab</th>
      </tr>
      <tr>
        <td>{{msg.title}}</td>
        <td>{{msg.price}}</td>
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


