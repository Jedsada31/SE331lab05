<template>
  <p>Registration form here</p>
  <button @click="register">Register Me</button>
</template>

<script>
export default {
  props: ['id', 'event'],
  methods: {
    register() {
      //Assuming sucessful API call to register them

      //Set a flash message to appear on the next page loaded which says
      // 'You are successfully registered for ' + this.event.title

      this.$router.push({
        name: 'EventDetails',
        params: { id: this.event.id }
      })
    }
  }
}
</script>
