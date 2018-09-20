<template>
  <div id="app">{{#router}}
    <router-view/>
    {{else}}
    <Hello/>
    {{/router}}
  </div>
</template>

<script>
{{#unless router}}
import Hello from './components/Hello'

{{/unless}}
export default {
  name: 'App'{{#router}}{{else}},
  components: {
    Hello
  }{{/router}},
  props: [],
  // created(){},
  // mounted(){},
  // updated(){},
  // activated(){}
  computed: {},
  watch: {},
  methods: {},
  data () {
    return {

    }
  }
}
</script>

<style>
@import './assets/css/reset.css';
@import './assets/css/functional.css';

#app {
  /* -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale; */
  font-family: Montserrat;
}
</style>
