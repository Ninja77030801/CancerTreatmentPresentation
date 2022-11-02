<script>
  import * as info from '../info';
  export default {
    name: "Slide1",
    mounted(){
      this.paragraph = info.slide1.p1
      this.list = info.slide1.list
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