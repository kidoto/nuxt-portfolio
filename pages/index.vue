<template>
<section class="container">
  <div id="main">

    <div>
      <h1 class="title">
          {{greeting}}
      </h1>
      <h2 class="subtitle">
        {{message}}
      </h2>
    </div>
  </div>
</section>
</template>

<script>

export default {
  layout: 'default',
  asyncData() {
    return {
      greeting: "kidotoのポートフォリオサイトへようこそ",
      message: "Vue.js + Nuxt.jsで構築したポートフォリオです"
    }
  },
  transition: {
    name: 'page',
    mode: 'out-in'
  }
}
</script>

<style>

.container {
  display: flex;
  justify-content: center;
  align-items: center;
}

.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
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
