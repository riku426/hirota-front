<template>
  <div class="header">
    <el-menu
      :default-active="activeIndex"
      class="el-menu"
      mode="horizontal"
    >
      <el-menu-item class="menu-item" index="1" @click="handleHome">ホーム</el-menu-item>
      <el-menu-item class="menu-item" index="2" @click="handleAdmin">アルコール管理</el-menu-item>
      <el-menu-item class="menu-item" index="3" @click="handleDrink">おすすめ飲料</el-menu-item>
    </el-menu>
  </div>
</template>

<script>
export default {
  data() {
    return {
      activeIndex: "1",
      activeIndex2: "1",
    };
  },
  methods: {
    handleHome() {
      this.$router.push('/')
    },
    handleAdmin() {
      this.$router.push('/admin')
    },
    handleDrink() {
      this.$router.push('/drink')
    }
  },
};
</script>


<style lang="scss" scoped>
.header {
  width: 100%;
  .el-menu {
    width: 100%;
    .menu-item {
      width: 33%;
    }
  }
}
</style>
