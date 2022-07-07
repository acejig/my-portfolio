<template>
    <div class="card">
        <div class="content">
            <span class="tag tag1">{{ tag1 }}</span><span class="tag tag2">{{ tag2 }}</span><span class="tag tag3">{{ tag3 }}</span>
        </div>
    </div>
</template>

<script>
    import "bootstrap-icons/font/bootstrap-icons.css";
    export default {
        name: 'SpotlightTags',
        props: {
            tag1: String,
            tag2: String,
            tag3: String,
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
    .content {
        display:flex;
        flex-direction: row;
        gap:1vw;
    }
    .tag { 
        background:#fff;
        padding:1vw 2vw 1vw 2vw;
        font-weight:bolder;
        color:#95918c;
        font-size:3vw;
        animation: fade-up 1s 1 ease-out forwards;
        opacity:0;
        box-shadow: rgba(0, 0, 0, 0.1) 0px 4px 12px;
        margin-top: 2rem;
    }
    .tag1{ animation-delay:1s; }
    .tag2{
        animation-delay:2s;
        color: rgba(255, 255, 255, 0) !important;
        -webkit-text-stroke-width: 1px !important;
        -webkit-text-stroke-color: rgb(255, 255, 255) !important;
        background: none !important;
        box-shadow: none !important;
        text-shadow: rgba(0, 0, 0, 0.1) 0px 4px 12px;
    }
    .tag3{ animation-delay:3s; }

    @keyframes fade-up {
        0%{
            margin-top: 2rem;
            opacity: 0;
            margin-bottom: 0rem;
        }
        100%{
            margin-top: 0rem;
            opacity: 1;
            margin-bottom: 2rem;
        }
    }
    @media only screen and (min-width: 1000px) {
        .content {
            flex-direction: row;
        }
    }
    @media only screen and (max-width: 999px) {
        .content {
            flex-direction: column;
        }
        .tag {
            font-size:8vw;
        }
    }
</style>