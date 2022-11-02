<script>
  import axios from 'axios'
  export default {
    name: "Slide1",
    mounted(){
      axios({
        method: "get",
        url: "./info.json"
      }).then(result => {
        this.paragraph = result.data.slide1.p1
        this.list = result.data.slide1.list
      })
    }
    data(){
      return {
        paragraph: "",
        list: []
      }
    }
  }
</script>
<template>
  <h1>Introduction</h1>
  <p>{{ paragraph }}</p>
</template>
<style></style>