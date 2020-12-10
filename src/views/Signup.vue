<template>
  <div class="container">
    <span>New User Register</span>
    <input placeholder="Name" v-model="form.name" type="text">
    <span v-if="alreadyRegistered" class="alert">Error: Email Already Registered</span>
    <input placeholder="Email" v-model="form.email" type="text">
    <span id="note">Note: Dont use any real Password</span>
    <input placeholder="Enter Password" v-model="form.passwd1" id="passwd" type="text">
    <span v-if="focusCounter & form.passwd1 != '' & form.passwd1 != form.passwd2" class="alert">Error: Passwords Dont match</span>
    <input placeholder="Re-Enter Password" @blur="focusCounter = true" v-model="form.passwd2" type="text">
    <div class="auth-btn" @click="signup">SIGNUP</div>
  </div>
</template>

<script>
  export default {
    data() {
        return {
          form: {
            name: '',
            email: '',
            passwd1: '',
            passwd2: '',
          },
          focusCounter: false,
          alreadyRegistered: false,
          //button: this.form.name != '' & this.form.email != '' & this.form.passwd1 != ''
        }
    },
    methods: {
      signup: function() {
        //var uname = document.getElementById('uname').value
        //var passwd = document.getElementById('passwd').value
        const requestOptions = {
          method: "POST",
          mode: "no-cors",
          headers: { "Content-Type": "application/json"},
          body: JSON.stringify({ name: this.form.name, email: this.form.email, passwd: this.form.passwd1 })
        };
        console.log(requestOptions)
        fetch("http://localhost:3000/signup", requestOptions)
        //console.log(res)
      }
    }
  }
</script>

<style scoped>
#note {
  position: relative;
  top: 15px;
  font-size: 1rem;
  font-weight: 600;
  border: 1px solid #6E4A90;
  box-sizing: border-box;
  padding: 5px;
  background-color: #c5aadd;
}
.alert{
  color: #857842;
  position: relative;
  top: 15px;
  font-size: 1rem;
  font-weight: 600;
  border: 1px solid #90834a;
  box-sizing: border-box;
  padding: 5px;
  background-color: #ddd4aa;
}
</style>