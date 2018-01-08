



<template>
  <div class="change">
    <div class="form-group">
      <label for="pwd">Old Password:</label>
      <input type="password" class="form-control" id="pwd" placeholder="Enter password" name="pwd" v-model="newuser1.ppwrd">
    </div>
    <div class="form-group">
      <label for="pwd">New Password:</label>
      <input type="password" class="form-control" id="newppwrd" placeholder="Enter password" name="newppwrd" v-model="newuser1.newppwrd">
    </div>
      <div class="form-group">
      <label for="pwd"> Conform Password:</label>
      <input type="password" class="form-control" id="confppwrd" placeholder="Enter password" name="confppwrd" v-model="newuser1.confppwrd">
    </div>
   
  
   <br>
  </div>
</template>

<script>
export default {
  name: 'Change',
  data () {
    return {
     
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>






























