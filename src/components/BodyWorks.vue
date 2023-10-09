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
            ソーシャルデータバンク本社の会議室管理アプリケーションを学生チームで約３ヶ月かけて提案・開発・運用した。エンジニア兼PMとして社員の方とのヒアリングから始まり、出社勤務の不便を取り除くという目標をかかげて０１開発を行った。社内ツールであるため公開できないが、一部機能を利用してGoogleカレンダー連携ToDoアプリを個人開発して公開している。
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
          content: '小学生はリトルリーグ、中学生では軟式野球部を経て、慶應義塾志木高校の野球部に所属した。大学では軟式野球サークルに所属しながら、慶應志木野球部の学生コーチとして活動していた。',
        },
        {
          img: 'fpga.jpg',
          title: 'FPGA実装',
          date: '2022',
          content: '私の卒業研究の内容は「差分プライバシ匿名化機能を付加したMQTTブローカのハードウェア実装」である。2024年１月にラスベガスで開催されるIEEE Consumer Communications & Networking Conference（CCNC）でPosterを発表する。',
        },
        {
          img: 'sdb.jpg',
          title: '長期インターン',
          date: '2022',
          content: 'ソーシャルデータバンク株式会社でエンジニアとしてWEBアプリケーション開発を行っている。フロントエンドはVue.js、バックエンドはLaravelを使用し、WebSocketを利用した双方向な非同期通信機能を実装。また、Terraformを使用してLaravelアプリケーション用ECS on Fargateのテンプレートの作成に貢献した。',
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