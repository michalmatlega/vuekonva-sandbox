<template>
    <div>{{ textowo }}</div>
</template>

<script>
    export default {
        props: [
            'testText'
        ],
        name: "Test",
        data() {
            return {
                textowo: this.testText
            }
        }
    }
</script>

<style scoped>

</style>
