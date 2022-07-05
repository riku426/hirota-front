<template>
  <div class="container">
    <div class="header">
      <Header />
    </div>
    <div class="content">
      <div class="top">
        <h1 class="title">酒量管理アプリ</h1>
        <p>にようこそ</p>
        <p>
          このアプリではお酒の飲み過ぎで健康を損なわないようにするためのツールです
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "IndexPage",
};
</script>


<style lang="scss">
.container {
  height: 700px;
  background-color: rgb(241, 237, 237);
  .top {
    text-align: center;
    padding: 5px;
    .title {
      color: orange;
    }
  }
}
</style>