<template>
  <div class="container-drink">
    <div class="header">
      <Header />
    </div>
    <div v-if="!this.visibleFlag" class="content">
      <div class="not-profile">
        <p class="suggest">
          プロフィール欄からフォーム入力して、あなたにオススメのビールを見てみましょう！
        </p>
      </div>
    </div>
    <div v-if="this.visibleFlag" class="content">
      <div class="message">
        <p>あなたにおすすめのビールは、、、</p>
        <h3>{{ recomendation.name }}</h3>
      </div>
      <div class="beer-img">
        <img :src="recomendation.path" alt="" class="beer-img" />
      </div>
      <div class="balloon1-top">
        <p>
          {{ recomendation.explanation }}
        </p>
      </div>
      <div class="rader">
        <canvas id="myRadarChart"></canvas>
      </div>
    </div>
    <div class="buy">
      <a href="">購入はこちらをクリック！</a>
    </div>
  </div>
</template>

<script>
export default {
  name: "IndexPage",
  data() {
    return {
      visibleFlag: true,
      beer: "",
      recomendation: "",
      beer_1: {
        name: "ええやんモルト",
        explanation:
          "麦芽感を全面に出したビール。ほのかに感じるフルーティーさで深いコクを演出。",
        path: require("@/img/molt.jpeg"),
        data: {
          //データの各項目のラベル(上から時計回り)
          labels: ["コク", "キレ", "フルーティ", "麦芽感", "苦味"],
          //データ設定
          datasets: [
            {
              //グラフのデータ(上から時計回り)
              data: [5, 1, 3, 5, 1],
              //グラフ全体のラベル
              label: "評価値",
              //背景色
              backgroundColor: "rgba(255,0,0,0.5)",
              //線の終端を四角にするか丸めるかの設定。デフォルトは四角(butt)。
              borderCapStyle: "butt",
              //線の色
              borderColor: "rgba(255,255,0,1)",
              //線を破線にする
              borderDash: [],
              //破線のオフセット(基準点からの距離)
              borderDashOffset: 0.0,
              //線と線が交わる箇所のスタイル。初期値は'miter'
              borderJoinStyle: "miter",
              //線の幅。ピクセル単位で指定。初期値は3。
              borderWidth: 3,
              //グラフを塗りつぶすかどうか。初期値はtrue。falseにすると枠線だけのグラフになります。
              fill: true,
              //複数のグラフを重ねて描画する際の重なりを設定する。z-indexみたいなもの。初期値は0。
              order: 0,
              //0より大きい値にすると「ベジェ曲線」という数式で曲線のグラフになります。初期値は0。
              lineTension: 0,
            },
          ],
        },
      },
      beer_2: {
        name: "ええやんブラック",
        explanation:
          "上品な苦味とほのかなフルーツ感で飲み口がすっきりとしたキレのあるビール。",
        path: require("@/img/black.jpeg"),
        data: {
          //データの各項目のラベル(上から時計回り)
          labels: ["コク", "キレ", "フルーティ", "麦芽感", "苦味"],
          //データ設定
          datasets: [
            {
              //グラフのデータ(上から時計回り)
              data: [2, 4, 3, 1, 5],
              //グラフ全体のラベル
              label: "評価値",
              //背景色
              backgroundColor: "rgba(255,0,0,0.5)",
              //線の終端を四角にするか丸めるかの設定。デフォルトは四角(butt)。
              borderCapStyle: "butt",
              //線の色
              borderColor: "rgba(255,255,0,1)",
              //線を破線にする
              borderDash: [],
              //破線のオフセット(基準点からの距離)
              borderDashOffset: 0.0,
              //線と線が交わる箇所のスタイル。初期値は'miter'
              borderJoinStyle: "miter",
              //線の幅。ピクセル単位で指定。初期値は3。
              borderWidth: 3,
              //グラフを塗りつぶすかどうか。初期値はtrue。falseにすると枠線だけのグラフになります。
              fill: true,
              //複数のグラフを重ねて描画する際の重なりを設定する。z-indexみたいなもの。初期値は0。
              order: 0,
              //0より大きい値にすると「ベジェ曲線」という数式で曲線のグラフになります。初期値は0。
              lineTension: 0,
            },
          ],
        },
      },
      beer_3: {
        name: "ええやんスライダー",
        explanation:
          "フルーティー感を全面に出したビール。キレがあり、甘ったるさを感じさせない。",
        path: require("@/img/slider.jpeg"),
        data: {
          //データの各項目のラベル(上から時計回り)
          labels: ["コク", "キレ", "フルーティ", "麦芽感", "苦味"],
          //データ設定
          datasets: [
            {
              //グラフのデータ(上から時計回り)
              data: [2, 5, 5, 1, 1],
              //グラフ全体のラベル
              label: "評価値",
              //背景色
              backgroundColor: "rgba(255,0,0,0.5)",
              //線の終端を四角にするか丸めるかの設定。デフォルトは四角(butt)。
              borderCapStyle: "butt",
              //線の色
              borderColor: "rgba(255,255,0,1)",
              //線を破線にする
              borderDash: [],
              //破線のオフセット(基準点からの距離)
              borderDashOffset: 0.0,
              //線と線が交わる箇所のスタイル。初期値は'miter'
              borderJoinStyle: "miter",
              //線の幅。ピクセル単位で指定。初期値は3。
              borderWidth: 3,
              //グラフを塗りつぶすかどうか。初期値はtrue。falseにすると枠線だけのグラフになります。
              fill: true,
              //複数のグラフを重ねて描画する際の重なりを設定する。z-indexみたいなもの。初期値は0。
              order: 0,
              //0より大きい値にすると「ベジェ曲線」という数式で曲線のグラフになります。初期値は0。
              lineTension: 0,
            },
          ],
        },
      },
      beer_4: {
        name: "ええやんトロピカル",
        explanation:
          "フルーティー感を全面に出したビール。深いコクを演出し、ビール感を感じさせない。",
        path: require("@/img/tropical.jpeg"),
        data: {
          //データの各項目のラベル(上から時計回り)
          labels: ["コク", "キレ", "フルーティ", "麦芽感", "苦味"],
          //データ設定
          datasets: [
            {
              //グラフのデータ(上から時計回り)
              data: [4, 1, 5, 1, 1],
              //グラフ全体のラベル
              label: "評価値",
              //背景色
              backgroundColor: "rgba(255,0,0,0.5)",
              //線の終端を四角にするか丸めるかの設定。デフォルトは四角(butt)。
              borderCapStyle: "butt",
              //線の色
              borderColor: "rgba(255,255,0,1)",
              //線を破線にする
              borderDash: [],
              //破線のオフセット(基準点からの距離)
              borderDashOffset: 0.0,
              //線と線が交わる箇所のスタイル。初期値は'miter'
              borderJoinStyle: "miter",
              //線の幅。ピクセル単位で指定。初期値は3。
              borderWidth: 3,
              //グラフを塗りつぶすかどうか。初期値はtrue。falseにすると枠線だけのグラフになります。
              fill: true,
              //複数のグラフを重ねて描画する際の重なりを設定する。z-indexみたいなもの。初期値は0。
              order: 0,
              //0より大きい値にすると「ベジェ曲線」という数式で曲線のグラフになります。初期値は0。
              lineTension: 0,
            },
          ],
        },
      },
      options: {
        scales: {
          r: {
            //グラフの最小値・最大値
            min: 0,
            max: 100,
            //背景色
            backgroundColor: "snow",
            //グリッドライン
            grid: {
              color: "pink",
            },
            //アングルライン
            angleLines: {
              color: "green",
            },
            //各項目のラベル
            pointLabels: {
              color: "blue",
            },
          },
        },
      },
    };
  },
  methods: {
    handleRader() {
      var ctx = document.getElementById("myRadarChart");
      var myChart = new Chart(ctx, {
        type: "radar",
        data: this.recomendation.data,
        options: this.options,
      });
    },
  },
  mounted() {
    this.beer = this.$route.query.option;
    if (this.beer == "麦芽感が強い") {
      this.recomendation = this.beer_1;
    } else if (this.beer === "苦味がある") {
      this.recomendation = this.beer_2;
    } else if (this.beer === "キレがある") {
      this.recomendation = this.beer_3;
    } else if (this.beer === "フルーティ") {
      this.recomendation = this.beer_4;
    } else if (this.beer === "コクがある") {
      this.recomendation = this.beer_1;
    } else {
      this.visibleFlag = false;
    }
    this.handleRader();
  },
};
</script>

<style lang="scss">
.container-drink {
  height: 1000px;
  background: -webkit-linear-gradient(left, #f89174, #ffc778);
  .content {
    .not-profile {
      margin: 30px 15px 15px 15px;
      background-color: white;
      border-radius: 30px;
      .suggest {
        padding: 10px;
      }
    }
    .message {
      text-align: center;
    }
    .beer-img {
      width: 95%;
      height: auto;
      margin: 10px;
      border-radius: 50px;
    }
  }
}
.balloon1-top {
  position: relative;
  display: inline-block;
  margin: 1.5em 20px;
  padding: 7px 10px;
  min-width: 120px;
  max-width: 100%;
  color: #555;
  font-size: 16px;
  background: white;
  border-radius: 5px;
}

.balloon1-top:before {
  content: "";
  position: absolute;
  top: -30px;
  left: 50%;
  margin-left: -15px;
  border: 15px solid transparent;
  border-bottom: 15px solid white;
}

.balloon1-top p {
  margin: 0;
  padding: 0;
}
.rader {
  background-color: white;
  margin: 20px;
  border-radius: 50px;
  #myRadarChart {
    padding-bottom: 20px;
  }
}
.buy {
  padding-top: 20px;
  text-align: center;
}
</style>