<template>
    <tr>
        <td>{{user.name}}</td>
        <td>{{user.age}}</td>
    </tr>
</template>

<script>
export default {
    name: 'user',
    props: {
        user: {
            type: Array,
            default: []
        }  
    },
    data() {
        return {

        }
    }
}
</script>

<style>

</style>