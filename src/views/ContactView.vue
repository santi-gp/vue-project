<template>
  <section>
    <h2>Contacto</h2>
    <article>
      <staff/>
    </article>
    <article>
      <TaskInput @add-task="AddNewTask" />
      <ul>
        <li v-for="(taskItem, index) in taskList" :key="`${index}`">
          {{ taskItem.task }}
        </li>
      </ul>
    </article>
  </section>
  <aside>
    <div>
      <CurrentTime />
    </div>
  </aside>
</template>
<script>
import CurrentTime from "@/components/CurrentTime.vue";
import TaskInput from "@/components/TaskInput.vue";
import Staff from '@/components/Staff.vue';

export default {
  name: "ContactView",
  components: {
    CurrentTime,
    TaskInput,
    Staff,
  },
  data() {
    return {
      taskList: [],
    };
  },
  methods: {
    AddNewTask(task) {
      /*console.log(task);*/
      this.taskList.push({ task });
    },
  },
};
</script>
