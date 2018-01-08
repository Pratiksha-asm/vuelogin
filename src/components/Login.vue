<template>


<div class="col-md-4 loginpage">
<h1>Login</h1>
<form v-on:submit="adduser">
   <div class="form-group">
      <label for="email">Email:</label>
      <input type="email" class="form-control" id="email" placeholder="Enter email" name="email" v-model="newuser.email">
    </div>
    <div class="form-group">
      <label for="pwd">Password:</label>
      <input type="password" class="form-control" id="pwd" placeholder="Enter password" name="pwd" v-model="newuser.ppwrd">
    </div>
   
   <button type="submit" name="login" v-on:click="sublog()">Login</button>
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
export default {
  name: 'Login',
  data () {
  
    return {
    newuser:{},
    user:[
    {
    email:"pratiksha@gmail.com",
      password:"pratiksha"
      },{
      email:"pratiksha1@gmail.com",
      password:"pratiksha1"
      },{
      email:"pratiksha2@gmail.com",
      password:"pratiksha2"
      },{
      email:"pratiksha3@gmail.com",
      password:"pratiksha3"
      },{
      email:"pratiksha4@gmail.com",
      password:"pratiksha4"
      },{
      email:"pratiksha5@gmail.com",
      password:"pratiksha5"
      },{
      email:"pratiksha6@gmail.com",
      password:"pratiksha6"
      }]
      
    }
  },
  methods:{
  sublog:function(event){
  alert('successfully logined...!!!!')
  },
  change(){
  this.$router.push('/change');
  },
  adduser:function(e){
  this.user.push({
  email:this.newuser.email,
  password:this.newuser.ppwrd
  });

 
  console.log('add');
  e.preventDefault();

  },
  ppwrd:{},
  email:{}
  }

}
</script>