<template>
    <v-circle :config="configCircle"></v-circle>
</template>

<script>
    export default {
        name: "Ball",
        props: [
            'posx',
            'posy'
        ],
        data() {
            return {
                configCircle: {
                    x: this.posx,
                    y: this.posy,
                    radius: 70,
                    fill: "red",
                    stroke: "black",
                    strokeWidth: 4
                }
            }
        },
        watch: {
            posx() {
                this.configCircle.x = this.posx;
            },
            posy() {
                this.configCircle.y = this.posy;
            },
        }

    }
</script>

<style scoped>

</style>
