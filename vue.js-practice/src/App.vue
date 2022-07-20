<!--HTML-->
<template>
<div>
  <Header/>
  <TaskTable/>
</div> 
</template>

<!--JavaScript-->
<script>
import Header from './components/Header.vue'
import TaskTable from './components/TaskTable.vue'

export default {
  name: 'App',
  components: {
    Header,
    TaskTable
}
}
</script>

<!--CSS stuff-->
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
