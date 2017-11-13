<template>
  <div class="card-game">
    <h2>{{ title }}</h2>
    <card />
  </div>
</template>

<script>
import Card from './Card.vue'
export default {
  name: 'CardGame',
  components: {
    'card': Card
  },
  data () {
    return {
      title: 'Card Game'
    }
  }
}
</script>

<style>

</style>
