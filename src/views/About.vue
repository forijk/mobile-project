<template>
  <div class="box">
    <div class="center">
      弹性盒子是 CSS3 的一种新的布局模式。 CSS3 弹性盒（ Flexible Box 或
      flexbox），是一种当页面需要适应不同的屏幕大小以及设备类型时确保元素拥有恰当的行为的布局方式。
      引入弹性盒布局模型的目的是提供一种更加有效的方式来对一个容器中的子元素进行排列、对齐和分配空白空间。
    </div>
    <div class="left">left</div>
    <div class="right">right</div>
    <div class="button orange">123</div>
  </div>
</template>
<script>


export default {
  mounted() {
    var btn = document.querySelector(".button");
    var h = 25;
    setInterval(function(){
      h ++;
      h = h % 360;
      btn.style.borderColor=`hsl(${h}, 95%, 45%)`
      btn.style.background=`linear-gradient(to bottom,  hsl(${h},95%,54.1%),  hsl(${h},95%,84.1%))`
    },100);
  }
}
</script>
<style scoped>
.button {
  display: inline-block;
  outline: none;
  cursor: pointer;
  text-align: center;
  text-decoration: none;
  font: 14px/100% Arial, Helvetica, sans-serif;
  padding: 0.5em 2em 0.55em;
  text-shadow: 0 1px 1px rgba(0, 0, 0, 0.3);
  border-radius: 0.5em;
  box-shadow: 0 1px 2px rgba(0, 0, 0, 0.2);
  color: white;
  border: solid 1px;
}

.box {
  display: flex;
  flex-wrap: wrap;
  text-align: center;
}
.center {
  background-color: rgb(218, 183, 183);
  flex: 100% 1;
}
.left,
.right {
  flex: 100% 1;
}
.left {
  background-color: rgb(176, 238, 176);
}
.right {
  background-color: rgb(95, 95, 129);
}
@media all and (min-width: 400px) {
  .left,
  .right {
    flex: 50% 1;
  }
}
@media all and (min-width: 800px) {
  .box {
    flex-wrap: nowrap;
  }
  .center {
    order: 2;
    flex: 1;
  }
  .left,
  .right {
    flex: 0 0 300px;
  }
  .left {
    order: 1;
  }
  .right {
    order: 3;
  }
}
</style>
