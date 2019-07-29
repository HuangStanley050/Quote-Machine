<template>
  <div class="row">
    <form>
      <div
        class="form-group col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3"
      >
        <lable>
          Quote
        </lable>
        <textarea v-model="quote" rows="3" class="form-control"></textarea>
      </div>
      <div
        class="form-group col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3"
      >
        <button @click.prevent="createNew" class="btn btn-primary">
          Add Quote
        </button>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  methods: {
    createNew() {
      this.$emit("quoteAdded", this.quote);
      this.quote = "";
    }
  },
  data: function() {
    return {
      quote: ""
    };
  }
};
</script>
<style></style>
