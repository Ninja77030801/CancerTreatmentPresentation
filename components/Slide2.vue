<script>
  import * as info from './info'
  export default {
    name: "Slide2",
    data(){
        return {
            heading: "",
            content: "",
            currentId: 1,
            steps: [
                {
                    id: 1,
                    content: "A radiation oncologist (a doctor who specializes in using radiation to treat cancer) and radiation therapist will figure out your treatment area. You may also hear the treatment area referred to as the treatment port or treatment field. These terms refer to the places in your body that will get radiation. You will be asked to lie very still while x-rays or scans are taken."
                },
                {
                    id: 2,
                    content: "The radiation therapist will tattoo or draw small dots of colored ink on your skin to mark the treatment area. These dots will be needed throughout your course of radiation therapy. The radiation therapist will use them to make sure you are in exactly the same position for every treatment. The dots are about the size of a freckle. If the dots are tattooed, they will remain on your skin for the rest of your life. Ink markings will fade over time. Be careful not to remove them and tell the radiation therapist if they fade or lose color."
                },
                {
                    id: 3,
                    content: "A body mold may be made of the part of the body that is being treated. This is a plastic or plaster form that keeps you from moving during treatment. It also helps make sure that you are in exactly the same position for each treatment"
                },
                {
                    id: 4,
                    content: "If you are getting radiation to the head and neck area you may be fitted for a mask. The mask has many air holes. It attaches to the table where you will lie for your treatments. The mask helps keep your head from moving so that you are in exactly the same position for each treatment."
                }
            ]
        }
    },
    computed: {
        CurrentItem(){
            return this.steps[this.currentId]
        }
    },
    mounted(){
        this.heading = info.slide2.heading
        this.content = info.slide2.content
    }
  }
</script>
<template>
  <h1>{{ heading }}</h1>
  <p>{{ content }}</p><br />
  <ol id="steps-list">
    <li v-for="step of steps">{{ step.content }}</li>
  </ol>
</template>
<style>
  #steps-list {
    font-size: 10pt;
  }
</style>