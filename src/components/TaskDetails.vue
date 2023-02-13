<template>
    <v-card class="task ">
        <div class="d-flex justify-space-between align-center">
            <h3 class="pa-4">{{ task.title }}</h3>
        <div class="icons pa-4">
      <i class="material-icons" @click="taskStore.deleteTask(task.id)"
        >delete</i
      >
      <i
        class="material-icons"
        :class="{ active: task.isFav }"
        @click="taskStore.toggleFav(task.id)"
        >favorite</i
      >
    </div>
        </div>
    </v-card>
  <!-- <div class="task">
    <h3>{{ task.title }}</h3>
    <div class="icons">
      <i class="material-icons" @click="taskStore.deleteTask(task.id)"
        >delete</i
      >
      <i
        class="material-icons"
        :class="{ active: task.isFav }"
        @click="taskStore.toggleFav(task.id)"
        >favorite</i
      >
    </div>
  </div> -->
</template>

<script setup>
import { useTaskStore } from "../stores/TaskStore";

const props = defineProps({
  task: {},
});

const taskStore = useTaskStore();
</script>
