<template>
    <div class="card">
        <div class="title">
            <i :class="icon"></i> {{ title }}
        </div>
        <div class="content">
            {{ content }}
        </div>
        <button class="button">
            View Works
        </button>
    </div>
</template>

<script>
    import "bootstrap-icons/font/bootstrap-icons.css";
    export default {
        name: 'InfoBox',
        props: {
            title: String,
            content: String,
            icon: String,
        }
    }
</script>

<style scoped>
    * {
        transition:.2s;
        font-family: Avenir, Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        color: #2b2d42;
    }
    .card {
        box-sizing: border-box;
        display:flex;
        flex-direction: column;
        padding:1rem;
        box-shadow: rgba(0, 0, 0, 0.1) 0px 4px 12px;
        border-radius: 10px;
        flex: 1 1 0;
    }
    @media only screen and (min-width: 1000px) {
        .card {
            width: 0;
        }
    }
    .title {
        font-size:30px;
        padding:2rem 1rem .5rem 1rem;
    }
    .content {
        font-size:15px;
        padding:0rem 1rem 0rem 1rem;
        text-align:justify;
        line-height:23px;
        flex-grow: 1;
    }
    .button{
        box-shadow: rgba(0, 0, 0, 0.1) 0px 4px 12px;
        font-size:15px;
        border:1px solid rgba(0,0,0,0.1);
        padding:1rem;
        background: rgb(255, 255, 255);
        border-radius: 10px;
        margin:1rem;
        color:#000;
    }
    .button:hover{
        box-shadow: rgba(0, 0, 0, 0.1) 0px 8px 24px;
        border:1px solid rgba(0,0,0,0.2);
        cursor:pointer;
    }
</style>