<template>
  <div>
    <v-for-grid />

    data: {{dummyData}}

    <hr />
    <div v-for="data in dummyData" :key='data' class="card-container-basic">
      <Card :data=data />
    </div>
  </div>
</template>

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
    }
  },
  computed: {
    dummyData() {
      return dummyData.data;
    }
  }
}
</script>

<style>

</style>