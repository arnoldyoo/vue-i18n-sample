<template>
  <div id="app">
    <p>{{ $t("message.hello") }}</p>
    <img src="./assets/logo.png">
    <button v-on:click="changeLo('en')" >English</button>
    <button v-on:click="changeLo('ja')" >Japanish</button>
    <button v-on:click="changeLo('ko')" >Korean</button>
    <router-view/>
  </div>
</template>

<script>

export default {
  name: 'App',
  methods: {
    changeLo: function (lang) {
      // 메소드 안에서 사용하는 `this` 는 Vue 인스턴스를 가리킵니다
      this.$i18n.locale = lang
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
