<template>
  <div id="app">
    <nav v-bind:class="active" v-on:click.prevent>
      <a href="#" class="home" v-on:click="makeActive('home')">Home</a>
      <a href="#" class="projects" v-on:click="makeActive('projects')">Projects</a>
      <a href="#" class="blog" v-on:click="makeActive('blog')">Blog</a>
    </nav>
    <div id="header">
      <h1>{{ intro }}</h1>
      <p>I like to build things, especially with code. To find out more, please check out some of these linked.</p>
    </div>
    <h2>Find out more about.. {{active}}</h2>
  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      intro: 'Hi, I\'m Daniel',
      active: 'home',
    }
  },
  methods: {
    makeActive: function(item) {
      this.active = item;
    },
  },
}
</script>

<style lang="scss">
body {
  margin: 0;
  background-color: #C7FF6D;
}

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#header {
  padding: 30px 30px;
  background-color: #FFBA6D;
}

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

nav {
  margin: 0 auto 0;
  background-color: #73D5FF;
  box-shadow: 0 1px 1px #ccc;
  border-radius: 2px;
}

nav a {
  display: inline-block;
  padding: 18px 30px;
  color: #fff !important;
  font-weight: bold;
  font-size: 16px;
  text-decoration: none !important;
  line-height: 1;
  text-transform: uppercase;
  background-color: transparent;
  -webkit-transition: background-color 0.25s;
  -moz-transition: background-color 0.25s;
  transition: background-color 0.25s;
}

nav.home .home,
nav.projects .projects,
nav.blog .blog {
  background-color: #FF6DB5;
}

</style>
