<template>
 <div class="header">
      <div class="header-left">
          <router-link to="/"><h4>Vue Mini Project</h4></router-link>
      </div>

      <div class="header-right">
          <router-link to="/product"><p>Product management</p></router-link>
          <router-link to="/user"><p>User management</p></router-link>
          <p class="admin"><strong>Administrator</strong></p>
      </div>
  </div>
  <router-view/>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
.header {
  display: flex;
  justify-content: space-between;
  width: 100vw;
  height: 62px;
  border: 1px solid #ccc;
  align-items: center;
}

.header-left h4 {
  margin-left: 20px;
}

.header-right {
  display: flex;
  justify-content: space-between;
  margin-right: 20px;
}

.header-right p {
    align-items: center;
    line-height: 62px;
    padding: 0 20px;
    cursor: pointer;
}

.header-right .admin {
  color: red;
  border: 1px solid #ccc;
  border-radius: 20px;
}
</style>
