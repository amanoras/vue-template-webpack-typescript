<template>
  <div id="app">
    <link href="https://fonts.googleapis.com/earlyaccess/notosansjapanese.css" rel="stylesheet" />
    {{#router}}
    <router-view></router-view>
    {{/router}}
  </div>
</template>

<script lang="ts">
import Vue from "vue";
{{#vueClassComponent}}import Component from "vue-class-component";{{/vueClassComponent}}

{{#vueClassComponent}}
@Component
export default class App extends Vue {
  name =  "app";
};
{{/vueClassComponent}}
{{^vueClassComponent}}
export default {
  name: "app",
} as Vue.ComponentOptions<Vue>;
{{/vueClassComponent}}
</script>

<style>
</style>

