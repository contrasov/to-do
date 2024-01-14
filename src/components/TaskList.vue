<template>
  <div id="listTask">
    <TaskItem v-for="(task, index) in reversedTasks" :key="index" :text="task" @delete-task="deleteTask" />
  </div>
</template>

<script>
import TaskItem from "./TaskItem.vue";

export default {
  props: {
    tasks: Array
  },
  components: {
    TaskItem
  },
  computed: {
    reversedTasks() {
      return [...this.tasks].reverse(); // Crie uma cópia local da propriedade tasks
    }
  },
  methods: {
    deleteTask(taskToDelete) {
      const indexToDelete = this.tasks.indexOf(taskToDelete);
      if (indexToDelete !== -1) {
        // Emita um evento para notificar o componente pai sobre a exclusão
        this.$emit('delete-task', taskToDelete);
      }
    }
  }
};
</script>

<style>
#listTask {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-top: 20px;
  width: 500px;
  gap: 16px;
}
</style>
