<template>
  <div id="app">
    <div id="lightDiv">
      <div class="lightOn"></div>
      <img src="../assets/vue.svg" />
    </div>
    <button v-on:click="lightOn = !lightOn">Switch light</button>
  </div>
</template>

<script>
const app = {
  data() {
    return {
      lightOn: false,
    };
  },
};
</script>
<style></style>
