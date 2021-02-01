<template>
  <div v-if="slotTest"></div>
  <div v-else>
    <v-for-grid
      :data="dummyData"
      :gridProps="gridProps"
    >
      <Card :item="item" />
    </v-for-grid>

    <!-- data: {{dummyData}} -->

    <hr />
    <!-- <div v-for="data in dummyData" :key='data' class="card-container-basic">
      <Card :data=data />
    </div> -->
  </div>
</template>


// I need to give VForGrid a props object (containing)
// data


<script>
import VForGrid from '../lib/VForGrid'

import Card from './Card'
import dummyData from '../data.js'

export default {
  name: 'Home',
  components: {
    'v-for-grid': VForGrid,
    Card
  },
  data() {
    return {
      slotTest: true
    }
  },
  computed: {
    dummyData() {
      return dummyData.data;
    },
    gridProps() {
      let gridProps = { name: 'name', description: 'description' }
      return gridProps;
    }
  }
}
</script>

<style>

</style>