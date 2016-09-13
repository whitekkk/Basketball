<template>
  <div>
    <div v-for = "point in points" id="box">
      <shooting-point :points="points" :point-counter="pointCounter" :index="$index"></shooting-point>
    </div>
  </div>
</template>

<script>
import ShootingPoint from './ShootingPoint'

export default {
  props: ['points', 'pointCounter'],
  data () {
    return {
    }
  },
  components: {
    ShootingPoint
  }
}
</script>
