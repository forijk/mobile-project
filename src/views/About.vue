<template>
  <div class="box">
    <div class="center">
      弹性盒子是 CSS3 的一种新的布局模式。 CSS3 弹性盒（ Flexible Box 或
      flexbox），是一种当页面需要适应不同的屏幕大小以及设备类型时确保元素拥有恰当的行为的布局方式。
      引入弹性盒布局模型的目的是提供一种更加有效的方式来对一个容器中的子元素进行排列、对齐和分配空白空间。
    </div>
    <div class="left">left</div>
    <div class="right">right</div>
  </div>
</template>
<style scoped>
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
