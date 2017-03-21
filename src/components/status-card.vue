<template>
  <a class="status-card" :href="app.url" target="_blank">
    <div class="status-app">
      <h3>{{ app.name }}</h3>
    </div>
    <div class="status-image status-ok" v-if="app.status === 1">
      <img src="../assets/img/check.png">
    </div>
    <div class="status-image status-error" v-else>
      <img src="../assets/img/warn.png">
    </div>
  </a>
</template>

<script>
export default {
  name: 'status-card',
  props: ['app'],
  data () {
    return {}
  }
}
</script>

<style lang="scss">
.status-card {
  color: rgba(0, 0, 0, 0.8);
  background-color: #f7f7f7;
  border-radius: 2px;
  box-shadow: 0 1px 3px 0 rgba(0,0,0,.2), 0 1px 1px 0 rgba(0,0,0,.14), 0 2px 1px -1px rgba(0,0,0,.12);
  height: 100px;
  display: flex;
  justify-content: space-between;
  align-items: center;

  .status-app {
    padding: 0 16px;
    max-width: 150px;

    h3 {
      margin: 0;
      display: inline-block;
    }
  }

  .status-image {
    display: inline-block;
    height: 100px;
    width: 100px;
    float: right;
    border-top-right-radius: 2px;
    border-bottom-right-radius: 2px;

    img {
      padding: 10px;
      height: 80px;
    }

    &.status-ok {
      background: #388E3C;
    }

    &.status-error {
      background: #e28332;
    }
  }
}
</style>
