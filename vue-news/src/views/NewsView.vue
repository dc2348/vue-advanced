<template>
  <div>
      <div v-for="user in users" v-bind:key="user.title">{{ user.title }}</div>
  </div>
</template>

<script>
import { fetchNewList } from '../api/index.js';

export default {
  data() {
    return{
      users: []
    }
  },
  created() {
    var vm = this;
    // axios는 Promise 기반임
    // new Promese
    fetchNewList()
    .then(function(response){
      console.log(response);
      vm.users = response.data;
    })
    .catch(function(error) {
      console.log(error);
    })
  }
}
</script>

<style>

</style>