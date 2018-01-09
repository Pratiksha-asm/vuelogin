<template>


<div class="col-md-4 loginpage">
<h1>Login</h1>
<form >
   <div class="form-group">
      <label for="email">Email:</label>
      <input type="email" class="form-control" id="email" placeholder="Enter email" name="email" v-model="newuser.email">
    </div>
    <div class="form-group">
      <label for="pwd">Password:</label>
      <input type="password" class="form-control" id="pwd" placeholder="Enter password" name="pwd" v-model="newuser.ppwrd">
    </div>
   
   <button type="button" name="login" v-on:click="sublog()" class="btn btn-success">Login</button>
   <br>
  <router-link to="/change">Change the Password</router-link>
  
  </form>
  </div>


</template>

<style scoped>
.loginpage{
  border:red;
}
h1{
  color:red;
  border:black;
}
</style>
<script>
import axios from 'axios';
export default {
  name: 'Login',
  data () {
    return {
     newuser:{email: '', password : ''},
      posts: [],
      errors: []
    }
  },
methods:{
  sublog() {
    axios.post('/api/v1/login', { data: this.newuser })
      .then(function (response) {
          console.log(response);
      })
      .catch(function (error) {
          console.log(error.message);
      });
    }
  }
}
  
</script>
