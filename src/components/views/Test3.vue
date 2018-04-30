<template>
    <section class="content">
        this test page3
        <div>{{response}}</div>
        <br>
        <button @click="callApi">Call API</button>
    </section>
</template>
<script>
/* import axios from 'axios' */
import api from '../../api'
export default {
  name: 'Login',
  data(router) {
    return {
      response: ''
    }
  },
  methods: {
    callApi () {
      api.request('get', 'http://localhost:5000/api/random')
      .then(response => {
        console.log(response.data.randomNumber)
        this.response = response.data.randomNumber
      })
      .catch(error => {
        console.log(error)
      })
    }
  }
}
</script>

<style>
  
</style>
