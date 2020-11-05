<template>
  <div id="app">
    <Navigation v-bind:nav="nav"/>
  </div>
</template>

<script>
import Navigation from '@/components/Navigation'

export default {
  name: 'App',
  data(){
    return {
      nav: {
        listItem : [
          {id: 1, title: 'Главная'},
          {id: 2, title: 'Меню'},
          {id: 3, title: 'Забронировать'},
          {id: 4, title: 'Контакты'}
        ]
      }
    }
  },
  components: {
    Navigation
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
