<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <!-- <Todo /> -->
  <Todo2 />
</template>

<script>
import Todo2 from './components/TodoV2'
// import Todo from './components/Todo.vue'

export default {
  name: 'App',
  components: {
    // Todo,
    Todo2
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
  display: flex;
  flex-direction: column;
  align-content: center;
  justify-content: center;

}
button{
  width: 300px;
  height: 150px;
  border: 0px;
  border-radius: 10px;
  background: #41B883;
  color: #000;
}
img{
  width: 200px;
  height: 200px;
  margin-bottom: 50px;
}
</style>
