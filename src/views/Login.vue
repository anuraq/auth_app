<template>
  <div class="container">
    <span>Already a User</span>
    <input placeholder="Username / Email" type="text">
    <input placeholder="Password" type="text">
    <div class="auth-btn" v-on:click="testLogin">LOGIN</div>
  </div>
</template>

<script>

export default {
  name: 'Login',
  methods: {
    testLogin: function() {
      alert("LOGIN");
    }
  },
}
</script>

<style>
.container {
  position: relative;
  top: -10%;
  display: flex;
  flex-direction: column;
  font-size: 2rem;
}
input {
  margin-top: 30px;
  height: 3rem;
  border-radius: 40px;
  max-width: 400px;
  box-sizing: border-box;
  text-align: center;
  font-size: 1.7rem;
}
input:focus {
  outline: none;
}
.auth-btn {
  margin-top: 30px;
  width: fit-content;
  box-sizing: border-box;
  padding: 10px;
  background-color: #6E4A90;
  color: beige;
  align-self: center;
  transition: background-color 0.2s ease-in, color 0.2s ease-in ;
}
.auth-btn:hover {
  background-color: rgb(231, 231, 231);
  color: black;
  box-shadow: 5px 10px #888888;
  cursor: pointer;
}
span {
  font-size: 2.5rem;
}
</style>