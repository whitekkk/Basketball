<template>
  <div>
    <div v-for = "n in 3" id="button">
      <button @click="pointCounter($index+1,index)">+{{n+1}}</button>
    </div>
    <button :disabled="!points[index].score" @click="pointCounter(-1,index)">-1</button>
  </div>
</template>

<script>
export default {
  props: ['points', 'pointCounter', 'index']
}
</script>

<style>
#button {
  float: left;
}
</style>
