<template>
  <el-container>
    <el-aside width="200px">
      <home-nav></home-nav>
    </el-aside>
    <el-container>
      <el-header>Header</el-header>
      <el-main>Main</el-main>
    </el-container>
  </el-container>
</template>

<script>
import homeNav from '../components/HomeNav.vue'
export default {
  name: 'Home',
  components: {
    homeNav
  }
}
</script>

<style lang="scss" scoped>
  .el-container {
    height: 100%;
  }
</style>
