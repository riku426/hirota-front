<template>
  <div class="container">
    <div class="header-comp">
      <Header />
    </div>
    <div class="content">
      <div class="top">
        <h1 class="title">酒量管理アプリ</h1>
        <p>にようこそ</p>
        <p>
          このアプリではお酒の飲み過ぎで健康を損なわないようにするためのツールです
        </p>
        <img src="@/img/beer.jpeg" class="beer-img" />
        <p class="point-title">あなたのビールポイントは...</p>
        <div class="point-box">
          <h3 class="test">333<span>pt</span></h3>
        </div>
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
  height: 750px;
  width: 100%;
  background: -webkit-linear-gradient(left, #f89174, #ffc778);
  .header-comp {
    background-color: gray;
  }
  .top {
    text-align: center;
    padding: 5px;
    .title {
      color: rgb(3, 3, 80);
    }
    .beer-img {
      padding: 0 5px;
      width: 95%;
      height: auto;
      border-radius: 30px;
    }
  }
  .point-box {
    padding: 10px;
    width: 60%;
    margin: auto;
    background-color: white;
    border-radius: 20px;
  }
}
</style>