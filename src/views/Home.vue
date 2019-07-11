<template>
  <div class="home">
    <!-- <img alt="Vue logo" src="../assets/logo.png" /> -->
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <ul>
      <li></li>
      <li></li>
      <li></li>
      <li></li>
      <li></li>
    </ul>
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'home',
  mounted() {
    const arr = document.getElementsByTagName('li');
    for(let i = 0; i<arr.length; i++) {
      arr[i].onclick = function() {
        console.log(i);
      }
    }
  }
  // components: {
  //   HelloWorld
  // }
}
</script>
<style scoped>
li {
  width: 100%;
  color: grey;
  border: 1px solid blue;
}
</style>

