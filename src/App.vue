<template>
  <div>
    <input type="text" v-model.number="myVal">
    <com-a :my-value="myVal" @my-event="getMyEvent">
       <!-- <p>123</p>
      <span>fish</span> -->
      <p slot="header">xxxx header</p>
      <p slot="footer">yyy footer</p>
    </com-a>
  </div>
</template>

<script>
// import Vue from 'vue'
import ComA from './components/A'
export default {
  components: {
    ComA
  },
  data () {
    return {
      myVal: ''
    }
  },
  methods: {
    getMyEvent (hello) {
      console.log('i got my event' + hello)
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
