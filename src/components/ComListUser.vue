<template>
    <table>
        <tr>
            <th>Name</th>
            <th>Age</th>
        </tr>
             <com-user v-for="(user, index) in listUsers" v-bind:key="index" v-bind:user="user"/>
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
       return{
 
       }
    },
    components: {
        ComUser
    }    
}
</script>

<style>

</style>