<template>
  <div id='app'>
    <h1> {{msg}}</h1>
    <hr>
      <tinder-item avatar="https://github.com/sergicontre/interop-series-vue-polymer/blob/master/src/assets/vue.png?raw=true" :name="name" :description="description" v-on:like="likeHandler" v-on:nope="nopeHandler"></tinder-item>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      name: 'Vue',
      description: 'Web Component interop with Vue'
    }
  },
  methods: {
    likeHandler: function (event) {
      console.log('Like event...');
    },
    nopeHandler: function (event) {
      console.log('Nope event...');
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
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
