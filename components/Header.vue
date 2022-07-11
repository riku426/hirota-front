<template>
  <div class="header">
    <el-menu :default-active="activeIndex" class="el-menu" mode="horizontal" background-color="rgb(238, 236, 236)" text-color="orange">
      <el-menu-item class="menu-item" index="1" @click="handleHome"
        >ホーム</el-menu-item
      >
      <el-menu-item class="menu-item" index="2" @click="handleAdmin"
        >管理</el-menu-item
      >
      <el-menu-item class="menu-item" index="3" @click="handleDrink"
        >おすすめ飲料</el-menu-item
      >
      <el-menu-item class="menu-item" index="4" @click="handleProfile"
        >プロフィール</el-menu-item
      >
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
      this.activeIndex = "1";
      this.$router.push("/");
    },
    handleAdmin() {
      this.activeIndex = "2";
      this.$router.push("/admin");
    },
    handleDrink() {
      this.activeIndex = "3";
      this.$router.push("/drink");
    },
    handleProfile() {
      this.activeIndex = "4";
      this.$router.push("/profile");
    },
  },
};
</script>


<style lang="scss" scoped>
.header {
  width: 100%;
  background-color: rgb(238, 236, 236);
  text-align: center;
  .menu-item {
    width: 25%;
    font-size: 12px;
  }
}
</style>
