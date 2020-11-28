<template>
  <div class="container">
    <input placeholder="Username / Email" type="text">
    <input placeholder="Password" type="text">
    <div class="auth-btn">LOGIN</div>
  </div>
</template>

<script>

export default {
  name: 'Login',
  components: {
  }
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
  width: 400px;
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
</style>