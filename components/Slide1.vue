<script>
  import * as info from './info'
  export default {
    name: "Slide1",
    data() {
      return {
        paragraph: "",
        list: []
      }
    },
    mounted(){
      this.paragraph = info.slide1.p1
      this.list = info.slide1.list
    }
  }
</script>
<template>
  <h1>Introduction</h1>
  <p>{{ paragraph }}</p>
  There are three types of radiation therapy. They are: <br />
  <ol>
    <li v-for="item of list">{{ item }}</li>
  </ol>
</template>
<style></style>