<template>
  <div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  methods: {
    deleteItem(){
      this.$emit('delete-item', this.msg)
    }
  }
}
</script>


