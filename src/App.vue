<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <HelloWorld msg="Hello Vue 3.0 + Vite" />
  <Calculator />
  <Tutorial />
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Tutorial from './components/Tutorial.vue'
import Calculator from './components/Calculator.vue'
import SearchResults from './components/SearchResults.vue'

export default {
  name: 'App',
  components: {
    Calculator,
    HelloWorld,
    Tutorial,
    SearchResults,
  }
}
</script>