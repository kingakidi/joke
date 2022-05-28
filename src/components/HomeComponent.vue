<template>
  <div class="jokes-container">
    <h3>Welcome to Programmer Jokes</h3>
    <hr />
    <div class="show-joke">
      {{ singleJoke }}
    </div>
  </div>
</template>

<script>
import axios from "axios";
export default {
  data() {
    return {
      jokeApiUrl: "https://v2.jokeapi.dev/joke/Programming?type=single",
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
  },
  mounted() {
    this.getSingleJoke();
  },
};
</script>

<style></style>
