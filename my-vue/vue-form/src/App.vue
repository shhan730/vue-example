<template>
  <form v-on:submit.prevent="submitForm">
    <div>
      <label for="username">id: </label>
      <input type="text" name="username" id="username" v-model="username">
    </div>
    <div>
      <label for="password">pw: </label>
      <input type="password" name="password" id="password" v-model="password">
    </div>
    <button type="submit">login</button>
  </form>
</template>

<script>
import axios from 'axios';

export default {
  data: function(){
    return {
      username: "",
      password: "",
    }
  },
  methods: {
    submitForm: function(event){
      // event.preventDefault();
      console.log(this.username, this.password);
      var url = 'https://jsonplaceholder.typicode.com/users'
      var data = {
        username: username,
        password: password
      }
      axios.post(url,data)
        .then({
          
        })
        .catch()
      
    }
  }
}
</script>

<style>

</style>