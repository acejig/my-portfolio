<template>
    <div class="container">
        <InfoBox title="HTML" content="The raspberry is the edible fruit of a multitude of plant species in the genus Rubus of the rose family, most of which are in the subgenus Idaeobatus. The name also applies to these plants themselves. Raspberries are perennial with woody stems." />
        <InfoBox title="CSS" content="Watermelon is a flowering plant species of the Cucurbitaceae family and the name of its edible fruit. A scrambling and trailing vine-like plant, it is a highly cultivated fruit worldwide, with more than 1,000 varieties." />
        <InfoBox title="Javascript" content="A banana is an elongated, edible fruit – botanically a berry – produced by several kinds of large herbaceous flowering plants in the genus Musa. In some countries, bananas used for cooking may be called 'plantains', distinguishing them from dessert bananas." />
        <InfoBox title="Vue.js" content="The garden strawberry is a widely grown hybrid species of the genus Fragaria, collectively known as the strawberries, which are cultivated worldwide for their fruit. The fruit is widely appreciated for its characteristic aroma, bright red color, juicy texture, and sweetness." />
    </div>
</template>

<script>
    import InfoBox from './InfoBox.vue';

    export default {
        name: 'InfoBoxContainer',
        components: {
            InfoBox
        }
    }
</script>

<style scoped>
    .container {
        transition:.2s;
        display:flex;
        justify-content:center;
        align-items:stretch;
        gap:2rem;
        background:#fff;
    }
    @media only screen and (min-width: 1501px) {
        .container {
            flex-direction: row;
            padding:1rem 10rem 1rem 10rem;
        }
    }
    @media only screen and (max-width: 1500px) {
        @media only screen and (min-width: 1000px) {
            .container {
                flex-direction: row;
                padding:1rem;
            }
        }
    }
    @media only screen and (max-width: 999px) {
        .container {
            flex-direction: column;
            padding:1rem;
        }
    }
</style>