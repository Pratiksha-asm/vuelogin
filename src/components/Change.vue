

<template>
<div class="col-md-4 ">
<form >
<h3>Reset:</h3>
   <div class="form-group">
      <label for="email">Old Passord:</label>
      <input type="Password" class="form-control" id="oldprd" placeholder="Enter Old " name="oldprd" v-model="newusers.oldprd">
    </div>
    <div class="form-group">
      <label for="newprd">New Password:</label>
      <input type="password" class="form-control" id="newprd" placeholder="Enter new password" name="newprd" v-model="newusers.newprd">
    </div>
    <div class="form-group">
      <label for="conpwd">Conform Password:</label>
      <input type="password" class="form-control" id="conprd" placeholder="Enter conform password" name="conprd" v-model="newusers.conprd">
    </div>
   
   <button type="button" name="Conform" v-on:click="Changes()" class="btn btn-success">Conform</button>
   <br>
  
  </form>
  </div>

</template>


<style scoped>

</style>
<script>

    
import axios from 'axios';
export default {
  name: 'Change',
  data () {
    return {
     newusers:{old: '', new : '',conform:''},
      posts: [],
      errors: []
    }
  },
methods:{
  Changes() {
    axios.post('/api/v1/resetPwd', { data: this.newusers })
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