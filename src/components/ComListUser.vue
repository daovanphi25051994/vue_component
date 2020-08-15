<template>
  <table>
    <tr>
      <th>Name</th>
      <th>Age</th>
      <th>Delete</th>
    </tr>
    <com-user v-for="(user, index) in listUsers"
              v-bind:key="index"
              v-bind:user="user"
              v-bind:index="index"
              v-on:onDelete="onDeleteUserClick"/>
  </table>
</template>

<script>
import ComUser from './ComUser.vue'

export default {
  name: 'com-users',
  props: {
    listUsers: {
      type: Array,
      default: []
    }
  },
  data() {
    return {}
  },
  methods: {
    onDeleteUserClick(index) {
    this.$emit('onDeleteUser', index)
    }
  },
  components: {
    ComUser
  }
}
</script>

<style>

</style>
