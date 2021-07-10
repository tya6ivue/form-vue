<template>
  <div class="Form">
    <h1>Validation Login page</h1>
    <p v-if="error.length">
      
      <ul> 
        <li v-for="e in error" v-bind:key="e.id">
          {{e}}
        </li>
      </ul>
    </p>
    <form @submit="Login">
      <input type="text" placeholder="enter name" v-model="name" /><br /><br />
      <input type="text" placeholder="enter password" v-model="password" /><br /><br />
      <button type="submit">Login</button>
    </form>
  </div>
</template>

<script>
export default {
  name: "Formvalidation",
  data() {
    return {
      error: [],
      name: null,
      password: null,
    };
  },
  methods: {
    Login(e) {
      this.error = [];
      if (this.name && this.password) {
        alert("Confirm ?");
      }
      if (!this.name) {
        this.error.push("User name is required");
      }
      if (!this.password) {
        this.error.push("Password is required");
      }
      console.warn("hello", this.error);
      e.preventDefault();
    },
  },
};
</script>

<style scoped>
.Form {
  color: rgb(233, 139, 23);
  background-color: blanchedalmond;
  width: 200px;
  margin-left: 600px;
}
</style>>