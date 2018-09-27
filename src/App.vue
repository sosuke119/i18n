<template>
  <div id="app">
     <div class="locale">
      <select v-model="locale" @change="$i18n.locale = locale">
        <option value="en">english</option>
        <option value="ja">日本語</option>
      </select>
    </div>
    <p>{{ $t("message.hello") }}</p>
    <router-view/>
  </div>
</template>
<script>
export default {
  name: 'app',
  data () {
    return {
      locale: 'ja'
    }
  }
}
</script>
<style lang="stylus">
#app
  font-family 'Avenir', Helvetica, Arial, sans-serif
  -webkit-font-smoothing antialiased
  -moz-osx-font-smoothing grayscale
  text-align center
  color #2c3e50

#nav
  padding 30px
  a
    font-weight bold
    color #2c3e50
    &.router-link-exact-active
      color #42b983
</style>
