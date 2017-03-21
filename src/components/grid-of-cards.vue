<template>
  <div class="margin-side">
    <div class="grid-wrapper">
      <status-card v-for="app in apps" :app="app" :key="app.name"></status-card>
    </div>
  </div>
</template>

<script>
// Import Vue to allow use of vue-resource for http.get
// and import status-card for passing data to child compnent
import Vue from 'vue'
import StatusCard from './status-card.vue'

// PASS DATA TO CHILD COMPONENT (status-card)
export default {
  components: { StatusCard },
  name: 'grid-of-cards',
  data () {
    return {
      apps: []
    }
  },
  created: function() {
    // var vm = this;
    // Get app statuses on load
    this.getStatuses();
  },
  methods: {
    // Gets app statuses from /status endpoints
    //   TODO: Should move to status-card and call once for each card, based on a
    //   JSON file of apps and their /status urls
    getStatuses: function() {
      // var vm = this;
      this.$http.get('http://localhost:8080/demo-statuses.json').then(response => {
        // Set app
        this.apps = response.body.apps;
      }, response => {
        // Error
        console.error('Something went wrong');
      })
    }
  }
}
</script>

<style lang="scss">
.margin-side {
  margin: 0 auto;

  .grid-wrapper {
    display: grid;
    grid-template-columns: 100%;
    grid-template-rows: auto;
    grid-gap: 15px;
    justify-content: center;

    @media (min-width: 615px) {
      grid-template-columns: 300px 300px;
    }

    @media (min-width: 938px) {
      grid-template-columns: 300px 300px 300px;
    }
  }
}
</style>
