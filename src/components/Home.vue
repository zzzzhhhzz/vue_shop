<template>
  <el-container>
    <el-header>
        <div>
            <img src="../assets/heima.png" alt="">
            <span>电商后台管理系统</span>
        </div>
       <el-button type="info" @click="logout">退出</el-button>
    </el-header>
    <el-container>
      <el-aside width="200px">Aside</el-aside>
      <el-main>Main</el-main>
    </el-container>
  </el-container>
</template>
    
<script>
export default {
  name: "home",
  methods: {
    logout() {
      window.sessionStorage.clear();
      this.$router.push("/login");
    },
  },
};
</script>

<style lang='less' scoped>

.el-header {
    background-color: rgb(65, 62, 62);
    display: flex;
    justify-content: space-between;
    color: rgb(230, 230, 230);
    padding-left: 0;
    align-items: center;
    font-size: 20px;
    > div {
        display: flex;
        align-items: center;
        span {
            padding-left: 15px;
        }
    }
    
}
.el-aside {
    background-color: rgb(80, 77, 77);
}
.el-container {
    height: 100%;
}
</style>
