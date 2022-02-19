<template>
  <el-container>
    <el-aside width="200px">
      <home-nav></home-nav>
    </el-aside>
    <el-container class="as-container">
      <el-header>{{$route.name}}</el-header>
      <el-main v-if="$route.name == 'Home'">
        welcome
      </el-main>
      <el-main v-else>
        <router-view></router-view>
      </el-main>
    </el-container>
  </el-container>
</template>

<script>
import homeNav from '../components/HomeNav.vue'
export default {
  name: 'Home',
  components: {
    homeNav
  },

  watch: {
    '$route'(val) {
      console.log(val)
    }
  }
}
</script>

<style lang="scss" scoped>
  .el-container {
    height: 100%;
  }

  .as-container {
    &>header {
      text-align: start;
      padding-left: 10px;
      line-height: 60px;
      font-weight: bold;
      border-bottom: 1px solid #ccc;
    }
  }
</style>
