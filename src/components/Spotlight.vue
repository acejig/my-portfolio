<template>
    <div class="card">
        <div class="content">
            <span class="name">{{ title }}</span>
        </div>
    </div>
</template>

<script>
    import "bootstrap-icons/font/bootstrap-icons.css";
    export default {
        name: 'SpotlightBox',
        props: {
            content: String,
            title: String
        }
    }
</script>

<style scoped>
    * {
        transition:.2s;
        font-family: Avenir, Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        color: #fffcf2;
    }
    .card {
        box-sizing: border-box;
        display:flex;
        flex-direction: column;
    }
    .name {
        color: rgba(255, 255, 255, 0);
        -webkit-text-stroke-color: rgb(255, 255, 255);
    }
    @media only screen and (min-width: 1000px) {
        .subtitle {
            font-size:7.5vw;
            word-spacing: 9999999px;
            line-height:7vw;
            font-weight:bolder;
            text-transform: uppercase;
        }
        .name {
            font-size:9vw;
            font-weight: bolder;
            -webkit-text-stroke-width: 2px;
        }
    }
    @media only screen and (max-width: 999px) {
        .subtitle {
            font-size:7.5vw;
            font-weight:bolder;
            text-transform: uppercase;
        }
        .name {
            -webkit-text-stroke-width: 1px;
            font-size:20vw;
            font-weight: bolder;
        }
    }
</style>