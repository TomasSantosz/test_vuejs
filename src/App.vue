

<script>
import ComentariosItem from './components/ComentariosItem.vue'

export default {
  name: 'App',
  components: {
    ComentariosItem,
  }
}
</script>

<style>
  :root{
    --grey_light: #c4c4c4;
    --white: #ffffff;
    --body_main: #ffffff;
    --grey: #5c5c5c;
    --grey_section: #dbdbdb;
  }

  *{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    outline: 0;
  }

  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
  }
  body::-webkit-scrollbar {
      display: none;
    }

  h1,h2,h3,h4,h5,h6, strong {
    font-weight: 500;
  }

  a{
    text-decoration: none;
    color: var(--grey);
  }

  a:hover{
    text-decoration: none;
    color: var(--grey_light);
  }

  button{
    cursor: pointer;
  }
</style>
<template>
  <ComentariosItem msg="Hello My friend"/>
</template>