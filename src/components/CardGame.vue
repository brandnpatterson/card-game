<template>
  <div class="card-game">
    <h2>{{ title }}</h2>
    <div v-for="value in values" class="card-container">
      <div v-for="suite in suites" class="card">
        <div class="top">
          <p>{{ value }}</p>
          <p>{{ suite.icon }}</p>
        </div>
        <div class="bottom">
          <p>{{ suite.icon }}</p>
          <p>{{ value }}</p>
        </div>
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
<style scoped>
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
}
.card .top p {
  margin: 0 0 0 7px;
  line-height: 15px;
  text-align: left;
}
.card .top p:first-child {
  margin-top: 7px;
}
.card .bottom p {
  margin: 0px 5px 0 0;
  text-align: left;
  transform: rotate(180deg);
}
.card .bottom p:nth-child(1) {
  margin-top: 15px;
}
</style>
