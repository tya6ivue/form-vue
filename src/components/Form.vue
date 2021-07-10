<template>
  <div class="login">
    <h1>Simple Login page</h1>
    <input
      type="text"
      placeholder="Enter your name"
      id=""
      v-model="signup.username"
    />
    <br /><br />
    <input
      type="password"
      placeholder="Enter your password"
      id=""
      key=""
      v-model="signup.password"
    />
    <p>Choose Hobby</p>
    <input
      type="checkbox"
      id="cricket"
      value="cricket"
      v-model="signup.hobbbies"
    />
    <label for="cricket">Cricket</label>
    <input
      type="checkbox"
      id="football"
      value="football"
      v-model="signup.hobbies"
    />
    <label for="football">Football</label><br />
    <p>Select Gender</p>
    <input type="radio" id="male" value="male" v-model="signup.gender" />
    <label for="male">Male</label>
    <input type="radio" id="female" value="female" v-model="signup.gender" />
    <label for="female">Female</label>
    <br /><br />
    <button v-on:click="submit">Submit</button>
  </div>
</template>

<script>
export default {
  name: "Form",
  data() {
    return {
      signup: {
        username: null,
        password: null,
        hobbies: null,
        hobbbies: null,
        gender: null,
      },
    };
  },
  methods: {
    submit() {
      console.warn(this.signup);
    },
  },
};
</script>

<style scoped>
.login {
  color: rgb(236, 142, 18);
  background-color: bisque;
  width: 200px;
  margin-left: 45%;
}
</style>