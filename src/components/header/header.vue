<template>
  <div>
    <div class="nav">
      <!-- 标题 -->
      <span class="title">😀🎅😔Emoji Manage</span>
      <div class="navBox">
        <ul>
          <li><a href="#">关于</a></li>
          <li><a href="#">评价</a></li>
          <li><a href="#">自定义表情栏⭐</a></li>
          <li><a href="#">支持作者</a></li>
        </ul>
      </div>
    </div>
  </div>
</template>

<style>
body {
  background-color: #f5f5f5;
  cursor: default;
}
</style>

<style scoped>
.nav {
  width: 100%;
  height: 70px;
  background-color: #fff;
  box-shadow: 1px 1px 5px 1px rgba(0, 0, 0, 0.3);
  line-height: 70px;
  position: fixed;
}

.title {
  font-size: 30px;
  margin-left: 15px;
}

ul,
li {
  display: inline-block;
}

a {
  text-decoration: none;
  color: #626262;
}

.navBox {
  display: inline-block;
}

.navBox ul {
  margin-left: 100px;
  line-height: 70px;
}

.navBox ul li {
  font-size: 20px;
  margin-right: 50px;
  height: 70px;
}

.navBox ul li a {
  transition: 0.25s;
}

.navBox ul li a:hover {
  color: #1890ff;
}
</style>
