<template>
    <div class="arrow">
    </div>
</template>

<script>
    export default {
        name: 'ScrollDown',
    }
</script>

<style scoped>
.arrow{
    position: absolute;
    bottom:10rem;
    font-size:10vw;
    color: #fffcf2;
    border-left:2px solid #fff;
    border-bottom:2px solid #fff;
    animation: animate 2s infinite, arrow-grow 2s normal forwards;
}
@media only screen and (max-width: 999px) {
    .arrow {
        bottom:5rem;
    }
}
@keyframes animate {
    0%{
        transform: translate(0,-15px) rotate(-45deg);
    }
    50%{
        transform: translate(0,15px) rotate(-45deg);
    }
    100%{
        transform: translate(0,-15px) rotate(-45deg);
    }
}
@keyframes arrow-grow {
    0%{
        width:0rem;
        height:0rem;
    }
    100%{
        width:3rem;
        height:3rem;
    }
}
</style>