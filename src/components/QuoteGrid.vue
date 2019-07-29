<template>
  <div class="row" style="margin-bottom:15px">
    <Quote
      @click.native="deleteQuote(index)"
      v-for="(quote, index) in quotes"
      >{{ quote }}</Quote
    >
  </div>
</template>
<script>
import Quote from "./Quote.vue";
export default {
  name: "QuoteGrid",
  methods: {
    deleteQuote(index) {
      this.$emit("quoteDeleted", index);
    }
  },
  props: ["quotes"],
  components: {
    Quote
  }
};
</script>
<style></style>
