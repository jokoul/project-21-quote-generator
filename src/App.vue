<template>
  <div class="app">
    <Header title="The Anime Quoter" />
    <Quote :quote="quote" />
    <div class="button-container">
      <button @click="getQuote">Generate</button>
    </div>
    <QuoteList :quotes="quotes" />
    <Footer />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Quote from "./components/Quote.vue";
import QuoteList from "./components/QuoteList.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "App",
  components: { Header, Quote, QuoteList, Footer },
  data() {
    return {
      quote: {},
      quotes: [],
    };
  },
  methods: {
    async getQuote() {
      if (this.quote.content) {
        this.quotes = [...this.quotes, this.quote];
      }
      console.log(this.quotes);

      const data = await fetch("https://animechan.vercel.app/api/random").then(
        (res) => res.json()
      );
      console.log(data);
      this.quote = {
        content: data.quote,
        anime: data.anime,
        character: data.character,
      };
    },
  },
  created() {
    //life cycle to define when the function have to be launch
    this.getQuote();
  },
};
</script>

<style lang="scss">
:root {
  --primary: #d81e5b;
  --secondary: #8a4fff;
  --tertiary: #87e5ff;
  --dark: #131a26;
  --light: #eee;
  --grey: #848484;
  --green: #006345;
}
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Fira Sans", sans-serif;
}

.button-container {
  display: flex;
  justify-content: center;
  padding: 0 12px;
  margin: 20px auto;

  button {
    border: none;
    outline: none;
    background-color: var(--primary);
    padding: 16px 32px;
    border-radius: 99px;
    color: var(--light);
    font-size: 28px;
    font-weight: 700;
    text-transform: uppercase;
    cursor: pointer;
    transition: 0.4s;
    &:hover {
      background-color: var(--secondary);
    }
  }
}
</style>
