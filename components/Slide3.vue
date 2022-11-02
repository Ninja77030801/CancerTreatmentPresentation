<script>
  import * as info from './info'
  export default {
    name: "Slide3",
    data()
    {
        return {
            heading: "",
            content: []
        }
    },
    mounted()
    {
        this.heading = info.slide3.heading
        this.content = info.slide3.content
    }
  }
</script>
<template>
    <h1>{{ heading }}</h1>
    <p v-for="para in content">{{ para }}</p>
</template>