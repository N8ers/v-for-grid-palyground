<template>
  <div class="card">
    Hi :)
    {{ item }}
    <!-- {{ dataObj }} -->
    <!-- <div class="title">i am Card</div>
    <div class="name">{{ dataObj.name }}</div>
    <div class="description">{{ dataObj.description }}</div> -->
  </div>
</template>

<script>
export default {
  name: 'card',
  props: {
    item: {
      type: String,
      default: 'me string'
    }
    // dataObj: {
    //   type: Object,
    //   default: () => {}
    // },
    // name: {
    //   type: String,
    //   default: ''
    // },
    // description: {
    //   type: String,
    //   default: ''
    // }
  }
}
</script>

<style>
.card {
  display: inline-block;
  width: 400px;
  height: 150px;
  text-align: left;
  border: 1px solid black;
  padding: 5px;
  margin: 5px;
}
.title {
  font-size: 24px;
}
.name {
  font-size: 18px;
}
.description {
  font-size: 16px;
}
</style>
