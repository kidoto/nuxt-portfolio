<template>
<section class="container">
  <div id="main">
    <div>
      <h2>これを書いた人</h2>
      <div id='box'>
        名前：{{name}}<br />
        年齢：{{age}}歳
      </div>
    </div>
  </div>
</section>
</template>

<script>
const now = new Date();
const mybirth = {
  year: 1988,
  month: 6,
  date: 6
};

// Dateインスタンスに変換
const birthDate = new Date(mybirth.year, mybirth.month - 1, mybirth.date);
console.log(birthDate);
// 文字列に分解
const y2 = birthDate.getFullYear().toString().padStart(4, '0');
const m2 = (birthDate.getMonth() + 1).toString().padStart(2, '0');
const d2 = birthDate.getDate().toString().padStart(2, '0');

// 今日の日付
const today = new Date();
const y1 = today.getFullYear().toString().padStart(4, '0');
const m1 = (today.getMonth() + 1).toString().padStart(2, '0');
const d1 = today.getDate().toString().padStart(2, '0');

// 引き算
const age = Math.floor((Number(y1 + m1 + d1) - Number(y2 + m2 + d2)) / 10000);

export default {
  layout: 'default',
  data() {
    return {
      name: 'jaVVVVVVVA',
      age: age
    }
  }
}
</script>

<style>
#main {
  width: 100%;
  padding: 4px;
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
