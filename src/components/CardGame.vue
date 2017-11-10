<template>
  <div class="card-game">
    <h2>{{ title }}</h2>
    <div v-for="value in values" class="card-container">
      <div v-for="suite in suites" class="card">
        <p>{{ value }}</p>
        <p>{{ suite.icon }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'CardGame',
  data () {
    return {
      title: 'Card Game',
      suites: [
        { name: 'clubs', icon: '♣️' },
        { name: 'diamonds', icon: '♦️' },
        { name: 'hearts', icon: '♥️' },
        { name: 'spades', icon: '♠️' }
      ],
      values: [ 2, 3, 4, 5, 6, 7, 8, 9, 10, 'A', 'J', 'Q', 'K' ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
.card-container {
  display: flex;
  justify-content: center;
}
.card {
  border: 1px solid green;
  border-radius: 5px;
  display: flex;
  flex-direction: column;
  margin: 10px;
  height: 100px;
  width: 50px;
  p {

  }
}
</style>
