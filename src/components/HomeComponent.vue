<template>
  <div class="jokes-container">
    <h3 class="joke-title">Welcome to Jokes</h3>
    <hr />
    <div class="show-joke">
      {{ singleJoke }}
    </div>
    <button @click="getAnotherJoke">Get Another Joke</button>
  </div>
</template>

<script>
import axios from "axios";
export default {
  data() {
    return {
      jokeApiUrl: "https://v2.jokeapi.dev/joke/Any?type=single",
      singleJoke: "",
      jokeStatus: false,
    };
  },
  methods: {
    async getSingleJoke() {
      await axios.get(this.jokeApiUrl).then((res) => {
        this.singleJoke = res.data.joke;
        if (res.data.joke) {
          this.jokeStatus = true;
        } else {
          this.jokeStatus = true;
          console.log("No joke");
          axios.get(this.jokeApiUrl).then((res) => {
            this.singleJoke = res.data.joke;
          });
        }
      });
    },
    getAnotherJoke() {
      this.getSingleJoke();
    },
  },
  mounted() {
    this.getSingleJoke();
  },
};
</script>

<style></style>
