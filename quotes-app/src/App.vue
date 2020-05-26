<template>
  <div class="container">
    <new-quote @quoteAdded="newQuote"></new-quote>
    <quote-grid :quotes="quotes" ></quote-grid>
  </div>
</template>

<script>
import NewQuote from './components/NewQuote.vue'
import QuoteGrid from './components/QuoteGrid.vue'

export default {
  components:{
    QuoteGrid,
    NewQuote
  },
  data() {
    return {
      quotes: ['Here I am '],
      maxQuotes: 10,
    };
  },
  methods: {
    newQuote(quote){
      this.quotes.push(quote)
    }
  },
};
</script>

<style></style>
