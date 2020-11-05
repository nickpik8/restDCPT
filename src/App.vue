<template>
  <div id="app">
    <Navigation v-bind:nav="nav"/>
    <router-view />
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
          {id: 1, title: 'Главная', href: '/'},
          {id: 2, title: 'Меню', href: '/menu'},
          {id: 3, title: 'Забронировать', href: '/reservation'},
          {id: 4, title: 'Контакты', href: '/'}
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
  margin: 0px auto;
  max-width: 90%;
}
a{
  text-decoration: none;
}
.m-1{
  margin: 1rem;
}
.m-2{
  margin: 2rem;
}
</style>
