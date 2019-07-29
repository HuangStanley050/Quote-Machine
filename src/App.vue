<template>
  <div id="app" class="container">
    <QuoteGrid :quotes="quotes" />
    <NewQuote />
  </div>
</template>

<script>
import QuoteGrid from "./components/QuoteGrid.vue";
import NewQuote from "./components/NewQuote.vue";
export default {
  name: "app",
  data: function() {
    return {
      maxQuotes: 10,
      quotes: ["default quote"]
    };
  },
  components: {
    QuoteGrid,
    NewQuote
  }
};
</script>

<style>
/* #app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
} */
</style>
