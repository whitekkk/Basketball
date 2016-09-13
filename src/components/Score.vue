<template>
  <div>
    {{points[index].name}}<br>
    {{points[index].score}}
  </div>
</template>

<script>
export default {
  props: ['points', 'index']
}
</script>
