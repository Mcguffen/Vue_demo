<template>
  <div id="app">
    {{count}}
    
    {{$store.getters.doubleCount}}
    <button @click="$store.commit('increment', 2)">count++</button>
    <button @click="$store.dispatch('increment', 2)">count++</button>

  </div>
</template>

<script>

export default {
  name: 'app',
  computed: {
    count(){
      return this.$store.state.count
    }
  }
}
</script>

<style>

</style>
