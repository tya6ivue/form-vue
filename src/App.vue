<template>
  <div>
    <Form />
    <formValidation />
    <!-- <Filter /> -->
  </div>
</template>

<script>
// import Filter from "./components/Filter.vue";
import Form from "./components/Form.vue";
import FormValidation from "./components/FormValidation.vue";
export default {
  name: "App",
  components: {
    Form,
    FormValidation,
    // Filter,
  },
};
</script>

<style
    FormValidation>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
