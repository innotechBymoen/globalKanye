<template>
  <div>
      <h3>{{ kanyeQuote }}</h3>
  </div>
</template>

<script>
export default {
  data() {
    return {
      kanyeQuote: "Click the button above to get a new quote!"
    };
  },
  mounted: function(){
      this.$root.$on('newKanyeQuote', this.fetchNewQuote)
  },
  methods: {
    fetchNewQuote: function() {
      let appComponent = this;
      let ajax = new XMLHttpRequest();
      ajax.onreadystatechange = function() {
        if (this.status == 200 && this.readyState == 4) {
          let myQuote = JSON.parse(this.responseText);
          appComponent.kanyeQuote = myQuote.quote;
        }
      };
      ajax.open("GET", "https://api.kanye.rest/", true);
      ajax.send();
    }
  }
};
</script>

<style scoped>
</style>