<template>
  <form @submit.prevent="submitForm">
      <rating-control v-model="rating" question="What is your Vue skill level?"></rating-control>
        <div>
            <button type="submit">Submit</button>
        </div>  
  </form>
</template>

<script>
import RatingControl from './RatingControl.vue'

export default {
    components: {
        RatingControl
    },
    data(){
        return {
            rating: null,
        }
    },
    methods: {
        submitForm(){
            console.log('Raiting is: ' + this.rating)
            this.rating = null
        }
    }
}
</script>

<style>

</style>