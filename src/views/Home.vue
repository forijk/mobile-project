<template>
  <div class="home">
    <!-- <img alt="Vue logo" src="../assets/logo.png" /> -->
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <div class="parent">
      <div class="child" style="height:300px;"></div>
      <div class="child"></div>
    </div>
    <br />
    <div class="parent">
      <div class="child"></div>
      <div class="child" style="height:300px;"></div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'home',
  mounted() {
  }
  // components: {
  //   HelloWorld
  // }
}
</script>
<style scoped>
.parent {
  display: flex;
  width: 300px;
  justify-content: center;
  align-content: center;
  align-items: stretch;
}
.child {
  width: 100px;
  outline: solid 1px;
}
</style>

