<template>
  <div id="app">
    <!-- Header Image -->
    <header class="header">
      <img src="../pic/R.jpg" alt="2025MedAI" class="header-img" />
      <div class="header-text">MedAI2025</div>
    </header>

    <!-- Navigation Bar -->
    <nav class="navbar">
      <router-link to="/" class="nav-link">Home</router-link>
      <router-link to="/committes" class="nav-link">COMMITTEES</router-link>
    </nav>

    <router-view />
  </div>
</template>

<style scoped>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin: 0;
  padding: 0;
  background-color: #f8f8f8; /* Light background for contrast */
}

.header {
  position: relative;
  width: 100%;
  height: 300px;
  /* 图片的高度，可根据需要调整 */
  overflow: hidden;
}

.header-img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  /* 确保图片按比例填充，不会变形 */
}

.header-text {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  font-size: 3rem;
  font-weight: bold;
  color: white;
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.7);
  /* 添加文字阴影 */
}

.navbar {
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: #343a40;
  /* 浅灰色背景 */
  padding: 10px 0;
  width: 100%;
}

.nav-link {
  color: white;
  text-decoration: none;
  font-weight: bold;
  margin: 0 20px;
  font-size: 1.2rem;
  padding: 5px 10px;
  transition: color 0.3s ease;
  position: relative; /* 为伪元素定位 */
}

.nav-link::after {
  content: "";
  position: absolute;
  right: -15px; /* 调整分割线位置 */
  top: 50%;
  transform: translateY(-50%);
  width: 1px; /* 分割线宽度 */
  height: 60%; /* 分割线高度 */
  background-color: white; /* 分割线颜色 */
}

.nav-link:last-child::after {
  display: none; /* 移除最后一个选项的分割线 */
}

.nav-link:hover {
  text-decoration: underline; /* 鼠标悬停时添加下划线 */
}

.nav-link.router-link-exact-active {
  color: white;
  text-decoration: none;
}
</style>
