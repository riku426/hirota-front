<template>
  <div class="container">
    <div class="header">
      <Header />
    </div>
    <div class="content">
      <p>名前</p>
      <el-input placeholder="名前" v-model="name" class="input"></el-input>
      <p>身長</p>
      <el-input placeholder="身長" v-model="height" class="input"></el-input>
      <p>体重</p>
      <el-input placeholder="体重" v-model="weight" class="input"></el-input>
      <p>拡張期血糖値</p>
      <el-input
        placeholder="拡張期血糖値"
        v-model="blood"
        class="input"
      ></el-input>
      <p>空腹時血糖値</p>
      <el-input
        placeholder="空腹時血糖値"
        v-model="suger"
        class="input"
      ></el-input>
    </div>
    <div class="reserve-button">
      <el-button type="primary" class="reserve-btn" @click="handleReserve"
        >保存</el-button
      >
    </div>
  </div>
</template>

<script>
export default {
  name: "IndexPage",
  data() {
    return {
      name: "",
      height: "",
      weight: "",
      blood: "",
      suger: "",
      alertFlag: false,
    };
  },
  methods: {
    handleReserve() {
      window.alert('プロフィールを保存しました')
    },
  },
};
</script>


<style lang="scss">
.container {
  height: 750px;
  background: -webkit-linear-gradient(left, #f89174, #ffc778);
  .reserve-button {
    margin-top: 20px;
    text-align: right;
  }
}

.input {
  width: 70%;
  margin: 10px;
}
.money {
  width: 40%;
  margin: 10px;
}
.reserve-btn {
  margin: 15px;
}
</style>