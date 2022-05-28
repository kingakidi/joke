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
  background-color: #e9e5e5;
  /* margin-top: 60px; */
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100%;
  box-sizing: border-box;
}

.jokes-container {
  display: flex;
  background-color: #fff;
  color: #504b4b;
  padding: 20px;
  width: 400px;
  height: 300px;
}
</style>
