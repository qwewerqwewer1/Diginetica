<template>
  <div id="app">
    <div class="container">
      <TheHeader />
      <TheMain />
    </div>
  </div>
</template>

<script>
import TheHeader from "./components/TheHeader";
import TheMain from "./components/TheMain";

export default {
  name: "App",
  components: {
    TheHeader,
    TheMain,
  },
};
</script>

<style lang="scss">
@import "../node_modules/the-new-css-reset/css/reset";
@import "./assets/scss/app";

body {
  background-color: #fff;
  min-height: 100vh;
  font-family: "PT Sans", sans-serif;
}

img {
  width: 100%;
  height: auto;
  object-fit: cover;
}

.container {
  display: flex;
  flex-direction: column;

  max-width: 1920px;
  padding: 0 100px 36px 100px;
  margin: 0 auto;

  @media (max-width: 767px) {
    padding: 0 16px 16px 16px;
  }
}

.quantity {
  font-size: 12px;
  line-height: 14px;
  color: var(--light-gray);
  transition: color 0.3s ease-in-out;
}

input[type="search"]::-webkit-search-cancel-button {
  appearance: none;
  -webkit-appearance: none;
  width: 20px;
  height: 20px;
  background-image: url("./assets/images/clear-field.svg");
  background-repeat: no-repeat;
  background-size: cover;
  cursor: pointer;
  transition: background-image 0.3s ease-in-out;
}
</style>
