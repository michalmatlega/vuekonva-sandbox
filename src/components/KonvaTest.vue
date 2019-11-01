<template>
    <div>
        <Test :test-text="testText"></Test>
        <div>{{ posx }}</div>
        <div>{{ posy }}</div>
        <button type="button" @click="run">Run</button>
        <button type="button" @click="stop">Stop</button>
        <label>
            <input type="number" min="1" max="10" v-bind:value="speed" name="speed"/>
        </label>
        <v-stage :config="configKonva">
            <v-layer>
                <Ball :posx="posx" :posy="posy"></Ball>
            </v-layer>
        </v-stage>

    </div>
</template>

<script>
    import Ball from "./Ball";
    import Test from "./Test";

    export default {
        components: {
            Ball, Test
        },
        data() {
            return {
                running: false,
                interval: undefined,
                configKonva: {
                    width: 2000,
                    height: 2000
                },
                posx: 400,
                posy: 400,
                testText: 'notchanged',
                speed: 1,
            };
        },
        methods: {
            run() {
                if (!this.interval) {
                    this.testText = 'changed';
                    this.interval = setInterval(() => {
                        this.posx += 1;
                    }, 100);
                }

            },
            stop() {
                clearInterval(this.interval);
                this.interval = undefined;
            }
        }
    };

</script>

<style scoped>

</style>
