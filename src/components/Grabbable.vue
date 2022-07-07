<template>
    <div class="card" v-on:click="drag($event)">
        {{ msg }}
    </div>
</template>

<script>
    export default {
        name: 'GrabbableCard',
        props: {
            msg: String
        },
        methods: {
            drag: function(event) {
                let self = this;
                self.style.marginTop = event.clientX + "px";
                self.style.marginLeft = event.clientY + "px";
            }
        }
    }
</script>

<style scoped>
    .card {
        cursor: grab;
        font-family: Avenir, Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        color: #2c3e50;
        display:inline-block;
        box-sizing: border-box;
        position:absolute;
        padding:3rem;
        box-shadow: rgba(0, 0, 0, 0.1) 0px 4px 12px;
    }
</style>