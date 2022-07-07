<template>
    <h1>Todos</h1>
    <ul>
      <li v-for="s of stocks.data" :key="s.result">
        {{ s.result }}
      </li>
    </ul>
</template>

<script>
    import axios from "axios";

    export default {
        name: "TodoList",
        data() {
            return {
                stocks: []
            };
        },
        async created() {
            try {
                const res = await axios.get(`https://finnhub.io/api/v1/search?q=AMD&token=sandbox_capk6fiad3i1rqbdai5g`);

                this.stocks = res.data;
                console.log(res);
            } catch (e) {
                console.error(e);
            }
        }
    };
</script>

<style scoped>
    h1 { text-decoration: underline; }
    li { color: white; }
</style>