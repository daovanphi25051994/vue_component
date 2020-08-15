<template>
    <header>
        <h1>{{ titleHeader }}</h1>
        <button type="button" v-on:click="changeTitle">Change Title</button>
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
      changeTitle() {
            let title = 'header  title';
            this.$emit('AppChangeTitle', title);
        }
    }
}
</script>

<style>

</style>
