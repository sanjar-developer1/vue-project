<template>
  <h1>App component bunda option api da yozilgan</h1>
  <ChildComponent />
</template>

<script>
import ChildComponent from './components/ChildComponent.vue';

export default {
  name: "App",
  components: { ChildComponent },
  provide() {
    return {
      username: "Sanjar",
      age: 14
    }
  }
}
</script>


<style></style>
