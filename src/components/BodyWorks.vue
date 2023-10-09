<template>
    <div class="works-list">
      <div v-for="(card, i) in cards" :key="i" class="works-item">
        <v-card
            class="mx-auto"
            max-width="400"
        >
          <v-img
              class="align-end text-white"
              height="200"
              :src="`./images/${card.img}`"
              cover
          >
            <v-card-title>{{ card.title }}</v-card-title>
          </v-img>

          <v-card-subtitle class="pt-4">
            {{ card.date }}
          </v-card-subtitle>

          <v-card-text>
            {{ card.content }}
          </v-card-text>
        </v-card>
      </div>
      <div class="works-item">
        <v-card
            class="mx-auto"
            max-width="400"
        >
          <v-img
              class="align-end text-white"
              height="200"
              src="../../public/images/todo.png"
              cover
          >
            <v-card-title>アプリ開発</v-card-title>
          </v-img>

          <v-card-subtitle class="pt-4">
            <a href="https://todo.stg.golink.jp">https//todo.stg.golink.jp</a>
          </v-card-subtitle>

          <v-card-text>
            ソーシャルデータバンク本社の会議室管理アプリケーションを提案・開発・運用。エンジニア兼PMとして社員の方からのヒアリングから０１で開発を行い、約３ヶ月で導入することができた。社内ツールで公開はできないため、一部機能を利用してGoogleカレンダー連携ToDoアプリを開発した。
          </v-card-text>
        </v-card>
      </div>
    </div>
</template>

<script>
export default {
  data () {
    return {
      cards: [
        {
          img: 'baseball.jpg',
          title: '高校野球',
          date: '2017',
          content: '小中高大と野球に関わる。NPBよりMLBを視聴することが多い。',
        },
        {
          img: 'fpga.jpg',
          title: 'FPGA実装',
          date: '2022',
          content: '卒業研究は「差分プライバシ匿名化機能を付加したMQTTブローカのハードウェア実装」。IEEE Consumer Communications & Networking Conference（CCNC）でPosterを発表する予定。',
        },
        {
          img: 'sdb.jpg',
          title: '長期インターン',
          date: '2022',
          content: 'ソーシャルデータバンク株式会社でエンジニアとしてLaravelによるWEBアプリケーション開発を行っている。フロントエンドはVue.jsを使用し、WebSocketを利用した双方向な非同期通信機能を実装。また、Terraformを使用してLaravelアプリケーション用ECS on Fargateのテンプレートを作成した。',
        },
      ],
    }
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}

.works-list {
  display: flex;
  flex-wrap: wrap;
  margin-bottom: -40px;
}

.works-item {
  width: 31.74603%;
  margin-right: 1.58730%;
  margin-bottom: 40px;
  color: #333;
}

.works-item:hover {
  opacity: .9;
}

.works-item:nth-of-type(3n) {
  margin-right: 0;
}

.works-img img {
  border: 1px solid #e6e6e6;
}

.works-name {
  font-size: 12px;
  font-weight: bold;
  margin-top: 8px;
}

.works-info {
  font-size: 10px;
  margin-top: 5px;
}
</style>