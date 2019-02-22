<template>
  <div id="app">
    <nav class="navbar navbar-expand-lg navbar-light bg-light">
      <a class="navbar-brand" href="#">Navbar</a>
      <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent"
        aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
    
      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav mr-auto">
          <li class="nav-item active">
            <router-link class="nav-link" :to="{name: '首頁'}" href="#">Home</router-link>
          </li>
          <li class="nav-item">
            <router-link class="nav-link" to="/page" href="#">Link</router-link>
          </li>
        </ul>
      </div>
    </nav>
    <img src="./assets/logo.png">
    
    <!-- <HelloWorld/> -->
    <router-view></router-view>

    <!-- <p>{{data.results[0].email}}</p> -->
    <!-- <div class="card" style="width: 18rem; margin: auto;">
      <img class="card-img-top" src="http://lorempixel.com/400/200/food/8" alt="Card image cap">
      <div class="card-body">
        <h5 class="card-title">Card title</h5>
        <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
        <a href="#" class="btn btn-primary">Go somewhere</a>
      </div>
    </div> -->
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'

export default {
  name: 'App',
  data(){
    return {
      data: []
    }
  },
  components: {
    HelloWorld,
  },
  created() {
    const vm = this;
    this.$http.get('https://randomuser.me/api/')
      .then((response) => {
        vm.data = response.data;
        console.log(vm.data);

      })
  }
}
</script>

<style lang="scss">
  @import "~bootstrap/scss/bootstrap";
  $color: black;
  body{
    /* background-color: $color; */
  }

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  /* margin-top: 60px; */
}
</style>
