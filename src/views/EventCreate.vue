<template>
  <div>
    <h1>Create an Event, {{ local }}</h1>
    <p>This event was created by {{ user.id }}</p>
    <p>There are {{ catLength }} categories</p>
  </div>
</template>

<script>
import { mapState } from 'vuex'
export default {
  computed : {
    catLength() {
      return this.$store.getters.catLength
    },
    ...mapState (['user', 'categories'])
  }
}
</script>

<style>

</style>