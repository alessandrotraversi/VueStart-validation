<template lang="pug">
  .hello
    img(src="../assets/logo.png")/
    p.myclass aaa
    h1 {{ msg }}
    h2 Essential Links
    router-view
    ul
      li
        a(href='https://vuejs.org', target='_blank') Core Docs
      li
        a(href='https://forum.vuejs.org', target='_blank') Forum
      li
        a(href='https://gitter.im/vuejs/vue', target='_blank') Gitter Chat
      li
        a(href='https://twitter.com/vuejs', target='_blank') Twitter
      br
      li
        a(href='http://vuejs-templates.github.io/webpack/', target='_blank') Docs for This Template
    h2 Ecosystem
    ul
      li
        a(href='http://router.vuejs.org/', target='_blank') vue-router
      li
        a(href='http://vuex.vuejs.org/', target='_blank') vuex
      li
        a(href='http://vue-loader.vuejs.org/', target='_blank') vue-loader
      li
        a(href='https://github.com/vuejs/awesome-vue', target='_blank') awesome-vue
    br/
    br/

    // form validator
    
    .row
      form.col.s12
        .row
          .input-field.col.s6(:class="{ 'control': true }")
            label.label(for='email') Email
            input.validate(v-validate="'required|email'" :class="{'input': true, 'is-danger': errors.has('email') }" name="email" type="text" placeholder="Email")/
            span.help.is-danger(v-show="errors.has('email')") {{ errors.first(&apos;email&apos;) }}

</template>

<script>
$(document).ready(function(){
  $('.myclass').css('color','#f00');
});

console.log('componente home.vue caricato');

export default {
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h1, h2 {
  font-weight: normal;
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
</style>
