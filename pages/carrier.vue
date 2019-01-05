<template>
<section class="container">
  <div id="main">
    <div>
      <h2>経歴</h2>
    </div>
    <div>
      <!--      <carrier v-for='data in datas' v-bind:key='data.cal.name' v-bind:data='datas'></carrier>
-->
      <!--
      <carrier v-for='item in cal' v-bind:key='item.name' v-bind:item='item.name'></carrier>
              -->
      <br />
      <table class="carrier" width="90%">
        <tr>
          <th v-for='head in header' v-bind:key='head.item'>
            {{ head.item }}
          </th>
        </tr>
        <tr v-for="cal in carrier" v-bind:key='cal.key' v-bind:class='cal.index' v-on:mouseover="mouse">
          <td align='center'>{{cal.year}}</td>
          <td style="white-space: pre-wrap;">{{cal.desc}}</td>
        </tr>
      </table>
      <br />
      <div id='detail'>
        <h3>案件詳細</h3>
        {{msg}}<br />
        {{msg2}}
      </div>
      <!--
      <carrier v-for='head in header' v-bind:key='head.name' v-bind:header='head.name'></carrier>
-->
      <!--

      <table border="1">
        <tr>
          <td v-for='item in cal' v-bind:key='item.name'>
            v- for {{item.name}} -50
          </td>

        </tr>
      </table>
-->
    <!--<carrier v-for='cal in hoge' v-bind:key='cal.ele' v-bind:carrier='cal.ele'></carrier>
      -->
      <!-- {{tableData}}
-->
    </div>
  </div>
</section>
</template>

<script>
import Carrier from '~/components/Carrier.vue'
var detail = [
  'いわゆる技術派遣会社の正社員として入社しました。案件にもよりますが、孫請け、曽孫請けの規模の会社です。',
  '東京ITスクールのJavaプログラマー研修2ヶ月コースを修了しました。',
  '国内メガバンクの行員向けの信用情報管理システムのJavaプログラムの開発、jUnitによるテストを行いました。',
  '実体の開発は中国にオフショアしていたため、成果物のレビューと対顧客との要件定義の場に先輩と同行して作業しました。',
  '240万件を漏洩した委託先業者ではありません。。こちらもJavaとjUnitを担当。フロントは製造しないフェーズだったため、どんなレイアウトになったのか不明です。',
  'Cで動いている現行システムをScalaに置換しつつ、マイグレーションを行いました。',
  '稼働中の動画配信システムをメンテしつつ、機能の修正を行いました。また、エンドユーザーからの問い合わせのサマリーなどの、定常的な作業の自動化をVBAマクロで行いました。',
  'BtoB向けの製品サポートサイトの運用、機能拡張を行っています。グローバルな会社の国内ユーザー向けの機能を担当しています。'
]

var detail2 = [
  '',
  '',
  'バックエンド担当のため、Javaプログラムの開発とjUnitでのテストを行いました。',
  '画面レイアウト設計（保険の契約書類の文言等）や、事前に決められたテスト観点に基づいてテストが出来ているのかのチェックを行いました。',
  '初めてSpring Frameworkに触れました。',
  'Scalaでやることは大したことないデータの加工がメインでした。ここで初めてOracle DBと真剣に向き合い、パーティション、インデックス等に触れました。',
  'Struts2とPostgresqlに初めて触れました。また、システムがRedHat上で動作していたので、Linux上での各種コマンドもここで学びました。',
  'i18nを意識した開発作業をJava + Tomcat + Strtus2の環境で行っています。'
]

export default {
  layout: 'default',
  components: {
    Carrier
  },
  methods: {
    mouse: function(event) {
//      this.detail.item_1='detail.item_2';
      var idx = parseInt(event.target.parentNode.className, 10);
      this.msg=detail[idx];
      this.msg2=detail2[idx];
    }
  },
  data() {
    return {
      msg: '詳細を見たい経歴にマウスを乗せると詳細が表示されます。',
      msg2:'',
      detail: {
        item_1: 'アイテム1',
        item_2: 'アイテム2',

      },
      header: [{
          item: '年'
        },
        {
          item: '概要'
        }
      ],
      hoge: [
        {
          ele:{
          year: '2015',
          desc: '都内 IT技術者派遣会社入社\n従業員規模 200名'
          }
        },
        {
          ele:{
          year: '2015',
          desc: '東京ITスクール Javaプログラマー研修（2ヶ月）'
        }
        }
      ],

      carrier: [
        {
          year: '2015',
          desc: '都内 某IT技術者派遣会社入社\n従業員規模 200名',
          index: '0'
        },
        {
          year: '2015',
          desc: '東京ITスクール Javaプログラマー研修（2ヶ月）',
          index: '1'
        },
        {
          year: '2015',
          desc: '国内銀行 行員向け与信情報管理システム開発',
          index: '2'
        },
        {
          year: '2015',
          desc: '保険代理店向け 契約情報管理システム開発',
          index: '3'
        },
        {
          year: '2016',
          desc: '官公庁 マイナンバー業務 Webシステム開発',
          index: '4'
        },
        {
          year: '2016',
          desc: '通信事業者向け データウェアハウスマイグレーション開発',
          index: '5'
        },
        {
          year: '2017-2018',
          desc: '公営ギャンブル 動画配信サービス運用、保守',
          index: '6'
        },
        {
          year: '2018',
          desc: '製造業 自社商品のECサイト運用、保守',
          index: '7'
        }
      ],
      tableData: {
        columns: [
          'id',
          'name',
          'email'
        ],
        data: [{
          'id': 1,
          'name': 'sample1',
          'email': 'sample1@example.com',
          'group_name': '人事部'
        }]
      }
    }
  }



}


</script>

<style>

#detail {
  margin: 4px;
  background-color: #f5f5f5;

}

.carrier,
.carrier th,
td {
  border: solid 1px black;
  border-spacing: 0;
  border-collapse: collapse;
}



.container {
  display: flex;
  justify-content: center;
  align-items: center;
  /*  text-align: center;
*/
}

.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  /* 1 */
  display: block;
  font-weight: 300;
  font-size: 20px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 12px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
