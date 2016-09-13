<template>
  <div>
    <div v-for = "point in points" id="box">
      <score :points="points" :index="$index"></score>
    </div>
  </div>
</template>

<script>
import Score from './Score'

export default {
  props: ['points'],
  data () {
    return {
    }
  },
  components: {
    Score
  }
}
</script>
