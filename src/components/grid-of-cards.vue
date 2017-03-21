<template>
  <div class="margin-side">
    <div class="grid-wrapper">
      <!-- FOR EACH "status" ITEM, CREATE A GRID ITEM -->
      <div class="grid-item">A</div>
      <div class="grid-item">B</div>
      <div class="grid-item">C</div>
      <!-- GRID ITEMS SHOULD CONTAIN <status-card> DIRECTIVE -->
    </div>
  </div>
</template>

<script>
// GET A BUNCH OF "status" JSON ITEMS

// PASS DATA TO CHILD COMPONENT (status-card)
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
.margin-side {
  margin: 0 auto;

  .grid-wrapper {
    display: grid;
    grid-template-columns: 200px 200px 200px;
    grid-gap: 10px;
    justify-content: center;

    .grid-item {
      background-color: #f7f7f7;
      padding: 10px;
      font-size: 150%;
    }
  }
}
</style>
