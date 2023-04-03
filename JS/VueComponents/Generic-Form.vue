<!-- 
Generic Vue Form - Global Save
This template defines a form with input fields for the user's name, email, and age. 
Each input field is bound to a data property using v-model. When the user submits the form, the submitForm method is called. 
This method sets each input value as a global variable using window and resets the form fields to their initial values.
 -->

<template>
  <form @submit.prevent="submitForm">
    <label for="name">Name:</label>
    <input type="text" id="name" v-model="name">
    <label for="email">Email:</label>
    <input type="email" id="email" v-model="email">
    <label for="age">Age:</label>
    <input type="number" id="age" v-model.number="age">
    <button type="submit">Submit</button>
  </form>
</template>

<script>
export default {
  data() {
    return {
      name: '',
      email: '',
      age: null
    }
  },
  methods: {
    submitForm() {
      // Set each value as a global variable
      window.name = this.name;
      window.email = this.email;
      window.age = this.age;

      // Reset form fields
      this.name = '';
      this.email = '';
      this.age = null;
    }
  }
}
</script>



