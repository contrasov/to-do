<template>
    <div id="inputContainer">
        <input type="text" id="taskInput" placeholder="Add New Task..." v-model="taskText" @input="checkCharacterLimit" maxlength="30"/>
        <button class="addTask" @click="addTask">Add</button>
    </div>
</template>

<script>
export default {
  data() {
    return {
      taskText: ""
    };
  },
  methods: {
    addTask() {
      this.$emit("add-task", this.taskText);
      this.taskText = ""; // Limpa o input após adicionar a tarefa
    }
  }
};
</script>

<style>
#inputContainer {
    display: flex;
    margin-top: 30px;
    gap: 16px;
}

#inputContainer input {
    background-color: #101010;
    border: 3px solid #1C1C1C;
    padding: 9px 24px;
    border-radius: 15px;
    width: 353px;
    color: #C9C9C9;
    font-weight: 600;
    font-size: 15px;
}

#inputContainer input::placeholder {
    color: #2B2B2B;
    font-size: 13px;
    font-weight: 700;
}

#inputContainer input:focus {
    outline: 2px solid #2B2B2B;
}


.addTask{
    cursor: pointer;
    padding: 8px 24px;
    border-radius: 15px;
    background: #292929;
    border: transparent;
    color: #7A7A7A;
    font-weight: 600;
    font-size: 18px;
}

.addTask:hover {
    background: #E63E21;
    color: #F7E3D9;
}

</style>