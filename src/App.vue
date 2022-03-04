<template>
  <div id="app">
    <img src="./assets/logo.png">
    <comp-header
      v-bind:titleHeader="titleHeader"
      v-on:changeTitleEven="handlerChangeTitle"></comp-header>
    <div class="container">
      <list-user v-bind:listUser="listUser"></list-user>
    </div>
    <comp-footer v-bind:titleFooter="titleFooter"></comp-footer>
  </div>
</template>

<script>
import CompHeader from "./components/CompHeader";
import CompFooter from "./components/CompFooter";
import ListUser from "./components/ListUser";

export default {
  name: 'app',
  data() {
    return {
      titleHeader: 'Hello World - Header',
      titleFooter: 'Hello World - Footer',
      listUser: [
        {id: 1, email: 'duc.nd1@gmail.com', active: false},
        {id: 2, email: 'duc.nd2@gmail.com', active: false},
        {id: 3, email: 'duc.nd3@gmail.com', active: true},
        {id: 4, email: 'duc.nd4@gmail.com', active: false},
        {id: 5, email: 'duc.nd5@gmail.com', active: false},
        {id: 6, email: 'duc.nd6@gmail.com', active: false}
      ]
    }
  },
  components: {
    CompHeader,
    CompFooter,
    ListUser
  },
  methods: {
    handlerChangeTitle(data) {
      this.titleHeader = data.title;
      this.titleFooter = data.title;
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
  color: #f80303;
  margin-top: 60px;
}

.container {
  max-width: 1170px;
  margin: 0 auto;
  padding: 0 15px;
  min-height: 100px;
}

</style>
