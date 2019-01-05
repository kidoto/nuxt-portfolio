<template>
<section class="container">
  <div id="main">
    <div>
      <h2>連絡先</h2>
      <div id='box'>
        <div class="links">
          TwitterのDMからご自由にどうぞ。<br />
          <a href="https://twitter.com/jaVVVVVVVA" target="_blank" class="button--green">Twitter</a>
        </div>
      </div>
    </div>
  </div>
</section>
</template>

<script>
export default {
  layout: 'default',
  data() {
    return {
    }
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
