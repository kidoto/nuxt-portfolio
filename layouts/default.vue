<template>
<div>
  <div class="global-header">
    <ul>
      <li>
        <router-link to="/">Home</router-link>
      </li>
      <li>
        <router-link to="/whois">Who is this</router-link>
      </li>
      <li>
        <router-link to="/carrier">Carrier</router-link>
      </li>
      <li>
        <router-link to="/contact">Contact</router-link>
      </li>
    </ul>

  </div>  <br /><br />

  <nuxt/>

</div>
</template>
<script>

export default {
  transition: {
    name: 'page',
    mode: 'out-in'
  }}
</script>
<style>
html {
  font-family: "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}

.button--green {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #3b8070;
  color: #3b8070;
  text-decoration: none;
  padding: 10px 30px;
}

.button--green:hover {
  color: #fff;
  background-color: #3b8070;
}

.button--grey {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #35495e;
  color: #35495e;
  text-decoration: none;
  padding: 10px 30px;
  margin-left: 15px;
}

.button--grey:hover {
  color: #fff;
  background-color: #35495e;
}

.global-header {
  background-color: #333333;
  position: fixed;
  top: 0px;
  width: 100%;
  color: #FFFFFF;
  text-align: center;
  justify-content: center;
  padding:5px;
}

.global-header a {
  color: #FFFFFF;
  text-decoration: none;
}
.global-header ul {
  list-style: none;
  display: flex;
  justify-content: space-between;
  padding: 0;
  margin: 0;
}
.global-header ul li{
  flex-grow: 1;
}
#main {
  width: 100%;
  padding: 4px;
}

</style>
