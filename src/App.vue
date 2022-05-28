<template>
  <HomeComponent />
</template>

<script>
import HomeComponent from "./components/HomeComponent.vue";

export default {
  name: "App",
  components: {
    HomeComponent,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  /* background-color: #e9e5e5; */
  /* margin-top: 60px; */
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100%;
  box-sizing: border-box;
}

.jokes-container {
  display: flex;
  flex-direction: column;
  background-color: transparent;
  color: #504b4b;
  padding: 20px;
  /* width: 400px; */
  max-width: 500px;
  box-shadow: 0px 10px 15px rgba(0, 0, 0, 0.39);
}
.show-joke {
  line-height: 2;
  margin: 5px 20px;
}

.joke-title {
  margin-bottom: 10px;
}

button {
  background: rgb(9, 238, 226);
  border: solid rgba(0, 0, 0, 0.39) 1px;
  padding: 10px;
}
body:before {
  content: "Developer Progress";
  position: fixed;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  z-index: -1;

  color: #0d745e;
  font-size: 25px;
  font-weight: 500px;
  display: grid;
  justify-content: center;
  align-content: center;
  opacity: 0.2;
  transform: rotate(-45deg);
}
</style>
