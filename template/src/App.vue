<template>
  <div id="app">{{#router}}
    <router-view/>
    {{else}}
    <HelloWorld/>
    {{/router}}
  </div>
</template>

<script>
{{#unless router}}
import HelloWorld from './components/HelloWorld'

{{/unless}}
export default {
  name: 'App'{{#router}}{{else}},
  components: {
    HelloWorld
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
