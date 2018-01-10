<template>
  <div id="app">
    <NavBar></NavBar>
    <router-view/>
    <BottomContent></BottomContent>
  </div>
</template>

<script>
import NavBar from './components/NavBar'
import About from './components/About'
import Projects from './components/Projects'
import Resume from './components/Resume'
import Contact from './components/Contact'
import BottomContent from './components/BottomContent'

export default {
   /* eslint-disable */
  name: 'app',
  components: {
    NavBar,
    About,
    Projects,
    Resume,
    BottomContent,
    Contact
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}

.main {
  /*display: block;*/
  min-height: 87vh;
}
</style>
