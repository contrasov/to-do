<template>
  <div id="app">
    <MenuHeader />
    <TaskInput @add-task="addTask" />
    <TaskList :tasks="tasks" @delete-task="deleteTask" />
  </div>
</template>

<script>
import MenuHeader from './components/MenuHeader.vue';
import TaskInput from './components/TaskInput.vue';
import TaskList from './components/TaskList.vue';

export default {
  name: 'App',
  data() {
    return {
      tasks: []
    };
  },
  methods: {
    addTask(taskText) {
      this.tasks.push(taskText);
    },
    deleteTask(taskToDelete) {
      const indexToDelete = this.tasks.indexOf(taskToDelete);
      if (indexToDelete !== -1) {
        this.tasks.splice(indexToDelete, 1);
      }
    }
  },
  components: {
    MenuHeader,
    TaskInput,
    TaskList
  }
};
</script>

<style>
#app {
  margin-top: 20px;
  font-family: 'Inter', sans-serif;
  text-align: center;
  display: flex;
  flex-direction: column;
  align-items: center;
}

body {
  background-color: #101010;
}
</style>
