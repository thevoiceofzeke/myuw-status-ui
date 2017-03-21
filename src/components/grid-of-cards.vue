<template>
  <div>
    <p>{{ msg }}</p>
  </div>
</template>

<script>
export default {
  name: 'grid-of-cards',
  data () {
    return {
      msg: 'WHAT WHAT'
    }
  }
}
</script>

<style lang="scss">
p {
  color: red;
}
</style>
