<template>
  <div class="content">
    <section class="about section" id="about">
      <div class="container">
        <h2 class="title">ABOUT</h2>
          <v-timeline align="start">
            <v-timeline-item
                v-for="(year, i) in years"
                :key="i"
                :dot-color="year.color"
                size="small"
            >
              <template v-slot:opposite>
                <div
                    :class="`pt-1 headline font-weight-bold text-${year.color}`"
                    v-text="year.year"
                ></div>
              </template>
              <div>
                <h2 :class="`mt-n1 headline font-weight-light mb-4 text-${year.color}`">
                  {{ year.title }}
                </h2>
                <div>
                  {{ year.content}}
                </div>
              </div>
            </v-timeline-item>
          </v-timeline>
        </div>
    </section>

    <section class="works section" id="works">
      <div class="container">
        <h2 class="title">WORKS</h2>
        <BodyWorks />
      </div>
    </section>

    <section class="skill section" id="skill">
      <div class="container">
        <h2 class="title">SKILLS</h2>
        <BodySkills />
      </div>
    </section>

    <section class="contact section" id="contact">
      <div class="container">
        <h2 class="title">CONTACT</h2>
        <p class="lead">
        </p>
        <div class="contact-list">
          <span class="contact-item">kmorise0616@gmail.com</span>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import BodyWorks from "@/components/BodyWorks";
import BodySkills from "@/components/BodySkills";

export default {
  components: {
    BodyWorks,
    BodySkills
  },
  data: () => ({
    years: [
      {
        color: 'cyan',
        year: '2016',
        title: '高校生',
        content: '慶應義塾志木高校に入学。硬式野球部に入部し、高校３年では副主将として日々練習に明け暮れた。また、12月に普通自動車第一種免許を取得し、２月にオーストラリアはケアンズで３週間語学留学を経験した。',
      },
      {
        color: 'green',
        year: '2019',
        title: '大学生',
        content: '慶應義塾大学理工学部に入学。アルバイトは地元埼玉で焼肉屋のホールとして４年間働き、大学では軟式野球サークルに所属していた。また、休日は慶應義塾志木野球部の学生コーチとして４年間選手たちと一緒に活動し、多くの貴重な経験をすることができた。',
      },
      {
        color: 'pink',
        year: '2022',
        title: '研究室配属',
        content: '大学３年までは建築について学んでいたが、コロナ禍でプログラミングに興味を持ち、大学４年の研究室配属のタイミングで情報分野を学び始めた。春には基本情報技術者試験、秋には応用情報技術者試験を所得し、夏からは長期インターンに参加し、WEBアプリケーションの開発を行っている。',
      },
      {
        color: 'amber',
        year: '2023',
        title: '大学院生',
        content: '私が所属している西研究室は地域・住民向けネットワークサービスによるスマートコミュニティの実現をテーマにしている。私の専門はネットワークに含まれる個人情報を保護するため、エッジコンピューティングを用いた匿名化について研究を行っている。特に、自動運転など低遅延性が求められるサービスに着目し、FPGAを用いた専用の回路を実装して低遅延・高スループットな匿名化アプリケーションの実装を目指している。',
      },
    ],
  }),
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
body {
  font-family: "Montserrat","Helvetica Neue",Arial,"Hiragino Kaku Gothic ProN","Hiragino Sans",Meiryo,sans-serif;
  font-size: 15px;
  letter-spacing: .05em;
  color: #333;
}

a {
  transition: opacity .3s;
  text-decoration: none;
  color: #1ca9e3;
}

img {
  max-width: 100%;
  height: auto;
  vertical-align: bottom;
  border-style: none;
}

.wrapper {
  padding-top: 73px;
}

.section {
  padding: 90px 0;
}

.section:nth-of-type(odd) {
  background-color: #f7f7f7;
}

.container {
  max-width: 1340px;
  margin: 0 auto;
  padding: 0 40px;
}

.title {
  font-size: 34px;
  font-weight: bold;
  line-height: 1;
  margin-bottom: 40px;
  text-align: center;
  letter-spacing: .05em;
  color: #333;
}

.lead {
  font-size: 16px;
  line-height: 1.8;
  margin-bottom: 30px;
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

/*--------------------------------
 Skill
---------------------------------*/
.skill-list {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  margin-bottom: -50px;
}

.skill-item {
  display: flex;
  align-items: flex-start;
  justify-content: space-between;
  width: 48%;
  margin-bottom: 50px;
}

.skill-img {
  width: 60px;
  height: auto;
  margin-right: 20px;
}

.skill-body {
  flex: 1;
}

.skill-name {
  margin-bottom: 10px;
}

.skill-text {
  font-size: 14px;
  line-height: 1.8;
}

/*--------------------------------
 About
---------------------------------*/
.profile {
  display: flex;
  flex-wrap: wrap;
  max-width: 800px;
  margin: 0 auto;
}
.profile-img {
  width: 20%;
  margin-right: 30px;
  border-radius: 50%;
}
.profile-img img {
  border-radius: 50%;
}
.profile-body {
  flex: 1;
}

.profile-body p {
  font-size: 15px;
  line-height: 1.8;
}

.profile-body p:not(:last-child) {
  margin-bottom: 30px;
}

/*--------------------------------
 Contact
---------------------------------*/
.contact {
  text-align: center;
}

.contact-item:not(:last-child) {
  margin-right: 10px;
}

.contact-text {
  margin-top: 10px;
}
/*--------------------------------
 ページトップ
---------------------------------*/
.page-top {
  font-weight: bold;
  padding: 10px;
  cursor: pointer;
  text-align: center;
  background-color: #4c4c4c;
}

.page-top .material-icons-outlined {
  vertical-align: bottom;
  color: #fff;
}

/*--------------------------------
 フッター
---------------------------------*/
.footer {
  padding: 30px;
  background-color: #333;
}

.copyright {
  font-size: 10px;
  text-align: center;
  color: #797979;
}

/*--------------------------------
 下層：Worksページ
---------------------------------*/
.article {
  padding: 80px 0;
}

.article-container {
  max-width: 1040px;
  margin: 0 auto;
  padding: 0 20px;
}

.article-title {
  margin-bottom: 30px;
  text-align: center;
}

.article-body {
  max-width: 720px;
  margin: 0 auto;
  margin-bottom: 80px;
}

.article-body h3 {
  position: relative;
  font-size: 18px;
  margin-bottom: 5px;
  padding-left: 1em;
}

.article-body h3:not(:first-child) {
  margin-top: 50px;
}

.article-body h3::before {
  position: absolute;
  top: 0;
  left: 0;
  width: 4px;
  height: 100%;
  content: "";
  border-radius: 3px;
  background-color: #333;
}

.article-body p {
  font-size: 15px;
  line-height: 1.8;
  margin-bottom: 30px;
}

.home-link {
  text-align: center;
}
</style>