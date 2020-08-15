<template>
  <tr>
    <td>{{ index }}</td>
    <td>{{ user.name }}</td>
    <td>{{ user.age }}</td>
    <td><button v-on:click="onDeleteClick(index)">Delete</button></td>
  </tr>
</template>

<script>
export default {
  name: 'user',
  props: {
    user: {
      type: Object,
      default: {}
    },
    index: Number
  },
  data() {
    return {}
  },
  methods : {
    onDeleteClick(index) {
      this.$emit('onDelete', index);
    }
  }
}
</script>

<style>

</style>
