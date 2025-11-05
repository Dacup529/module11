<template>
  <div id="quotes">
        <h1>Random Quote Generator</h1>

    <p v-if="loading">Loading...</p>
    <div v-else>
      <p>{{ quote }}</p>
      <p class="author" v-if="author">— {{ author }}</p>
    </div>

    <button @click="getQuote">Get New Quote</button>
    <GoBack/>
  </div>
</template>

<script>
import axios from "axios";
import GoBack from "@/components/GoBack.vue";

export default {
  name: "RandomQuotesView",
  components: {
    GoBack,
  },
  data() {
    return {
      quote: "",
      author: "",
      loading: false,
    };
  },
  methods: {
    async getQuote() {
      this.loading = true;
      try {
        const response = await axios.get(
          "https://quotes15.p.rapidapi.com/quotes/random/?language_code=en",
          {
            headers: {
              "x-rapidapi-host": "quotes15.p.rapidapi.com",
              "x-rapidapi-key": "177010af54msh28148243bf42bc2p1d9591jsnd40c2381b548",
            },
          }
        );
        this.quote = response.data.content;
        this.author = response.data.originator.name;
      } catch (error) {
        console.error("Error fetching quote:", error);
        this.quote = "Oops! Something went wrong.";
        this.author = "";
      } finally {
        this.loading = false;
      }
    },
  },
  mounted() {
    this.getQuote();
  },
};
</script>

<style>
#quotes {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.container {
  text-align: center;
  font-family: Arial, sans-serif;
  margin-top: 50px;
}
button {
  margin-top: 20px;
  padding: 10px 20px;
  font-size: 16px;
}
.author {
  font-style: italic;
  color: #555;
  margin-top: 5px;
}
</style>
