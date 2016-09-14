<template>
  <div id="app">
    <scores :points="points"></scores>
    <shooting-points :points="points" :point-counter="pointCounter"></shooting-points>
  </div>
</template>

<script>
import Scores from './components/Scores'
import ShootingPoints from './components/ShootingPoints'

export default {
  data () {
    return {
      points: [{
        name: 'Home',
        score: 0
      },
      {
        name: 'Away',
        score: 0
      }]
    }
  },
  methods: {
    pointCounter (point, index) {
      this.points[index].score += point
    }
  },
  components: {
    Scores,
    ShootingPoints
  }
}
</script>

<style>
html {
  height: 100%;
}

body {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100%;
}

#app {
  color: #2c3e50;
  margin-top: -100px;
  max-width: 600px;
  font-family: Source Sans Pro, Helvetica, sans-serif;
  text-align: center;
}

#app a {
  color: #42b983;
  text-decoration: none;
}

.logo {
  width: 100px;
  height: 100px
}

#box {
  float: left;
  width: 40%;
}

</style>
