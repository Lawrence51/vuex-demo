<template>
  <div id="app">
    <img src="./assets/logo.png">
    <input type="button" value="增加" @click="increment">
    <input type="button" value="减少" @click="decrement">
    <input type="button" value="偶数才点击" @click="clickOdd">
    <input type="button" value="点击异步" @click="clickAsync">
    <div>
      展示现在数字：{{ count }},他现在是{{ getOdd }}
    </div>
  </div>
</template>

<script>
import {mapActions, mapGetters} from 'vuex'
export default {
  computed:mapGetters([
    'count',
    'getOdd'
  ]),
  methods:mapActions([
    'increment',
    'decrement',
    'clickOdd',
    'clickAsync'
  ])
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
