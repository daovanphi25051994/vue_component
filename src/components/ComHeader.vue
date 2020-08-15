<template>
    <header>
        <h1>{{ titleHeader }}</h1>
        <button type="button" v-on:click="changetitle">Change Title</button>
    </header>
    
</template>

<script>
export default {
    name: 'com-header',
    props: {
        titleHeader: String
    },
    data() {
        return {
           
        }
    },
    methods: {
        changetitle() {
            let title = 'header hehe title';
            this.$emit('AppChangeTitle', title);
        }
    }
}
</script>

<style>

</style>