<template>
  <Blind
  v-bind="contacts"/>
</template>

<script>
import Blind from './components/Blind.vue'

export default {
  name: 'App',
  components: {
    Blind
  },
  
}
</script>

<style>
  #app{
    min-height: 100vh;
  }
</style>
