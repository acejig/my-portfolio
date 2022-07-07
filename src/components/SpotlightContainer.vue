<template>
    <div class="container spectrum-background">
            <div class="tl"></div>
            <div class="br"></div>
            <SpotlightBox title="Andrew Caroselli"/>
            <SpotlightTags tag1="developer" tag2="&amp;" tag3="designer"/>
            <ScrollDown/>
    </div>
</template>

<script>
    import SpotlightBox from './Spotlight.vue';
    import ScrollDown from './ScrollDown.vue';
    import SpotlightTags from './SpotlightTags.vue';

    export default {
        name: 'SpotlightContainer',
        components: {
            SpotlightBox,
            SpotlightTags,
            ScrollDown
        }
    }
</script>

<style scoped>
    .container {
        transition:.2s;
        display:flex;
        justify-content:center;
        align-items:center;
        gap:1rem;
        height: 100vh;
        width: 100%;
        box-sizing:border-box;
        flex-direction: column;
    }
    .tl {
        position:absolute;
        box-sizing: border-box;
        border-left:2px solid #fffcf2;
        border-top:2px solid #fffcf2;
        top:0;
        left:0;
        margin:5rem;
        animation: stretch 2s 1 normal forwards;
    }
    .br {
        position:absolute;
        box-sizing: border-box;
        border-right:2px solid #fffcf2;
        border-bottom:2px solid #fffcf2;
        right:0;
        bottom:0;
        margin:5rem;
        animation: stretch 2s 1 normal forwards;
    }
    @keyframes stretch {
        0%{
            width:0vw;
            height:0vh;
        }
        100%{
            width:50vw;
            height:75vh;
        }
    }
    .spectrum-background {
        background:
            linear-gradient(#ccc5b9, transparent),
            linear-gradient(to top left, #252422, transparent),
            linear-gradient(to top right, #403d39, transparent);
        background-blend-mode: screen;
    }
    @media only screen and (max-width: 999px) {
        .tl, .br {
            margin:1rem;
        }
    }
</style>