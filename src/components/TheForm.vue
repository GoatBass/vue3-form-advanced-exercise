<template>
  <form @submit.prevent="submitForm">
    <div>
      <rating-control
        question="What is your Vue skill level ?"
        v-model="rating"
      ></rating-control>
    </div>
    <div>
      <button type="submit">Submit Form</button>
    </div>
  </form>
</template>

<script>
import RatingControl from "./RatingControl.vue";
export default {
  components: { RatingControl },
  data() {
    return {
      rating: null,
    };
  },
  methods: {
    submitForm() {
      console.log("Rating : " + this.rating);
      this.rating = null;
    },
  },
};
</script>

<style scoped>
form {
  margin: 2rem auto;
  max-width: 40rem;
  border-radius: 12px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.26);
  padding: 2rem;
  background-color: #ffffff;
}

button {
  font: inherit;
  border: 1px solid #0076bb;
  background-color: #0076bb;
  color: white;
  cursor: pointer;
  padding: 0.75rem 2rem;
  border-radius: 30px;
}

button:hover,
button:active {
  border-color: #002350;
  background-color: #002350;
}
</style>