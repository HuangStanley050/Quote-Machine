<template>
  <div id="app" class="container">
    <Header :quoteCount="quotes.length" :maxQuotes="maxQuotes" />
    <NewQuote @quoteAdded="newQuote" />
    <QuoteGrid @quoteDeleted="deleteQuote" :quotes="quotes" />
    <div class="row">
      <div class="col-sm-12 text-center">
        <div class="alert alert-info">
          Click on a quote to delete it
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import QuoteGrid from "./components/QuoteGrid.vue";
import NewQuote from "./components/NewQuote.vue";
import Header from "./components/Header.vue";
export default {
  name: "app",
  methods: {
    newQuote(quote) {
      if (this.quotes.length >= this.maxQuotes) {
        return alert("Please delete quote first");
      }
      this.quotes.push(quote);
    },
    deleteQuote(index) {
      this.quotes.splice(index, 1);
    }
  },
  data: function() {
    return {
      maxQuotes: 10,
      quotes: ["default quote"]
    };
  },
  components: {
    QuoteGrid,
    NewQuote,
    Header
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
