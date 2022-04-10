<template>
  <div>
    <!-- <input type="text" v-model="task" />-->
    <!--
      Removing the v-model from the input
    -->
    <h2>Lista de Tareas</h2>
    <input type="text" :value="task" @input="task = $event.target.value" />
    <button @click="AddTask">Añadir</button>
  </div>
</template>
<script>
export default {
  name: "TaskInput",
  data() {
    return {
      task: "",
    };
  },
  methods: {
    AddTask() {
      this.$emit("add-task", this.task);
      this.task = "";
    },
  },
};
</script>

<!--<template>
  <div>
    <strong>Mi tarea es: {{ task }}</strong>
    <br />
    <input type="text" v-model="task" />
  </div>
</template>
<script>
export default {
  name: "TaskInput",
  data() {
    return {
      task: "",
    };
  },
};
</script>-->