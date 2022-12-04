<template>
  <header>
    <h1>{{ title }}</h1>
    <ButtonApp
      @btn-click="$emit('toggle-add-task')"
      :text="showAddTask ? 'Close' : 'Add Task'"
      :color="showAddTask ? 'red' : 'green'"
    />
  </header>
</template>
<script>
import ButtonApp from "./ButtonApp.vue";
export default {
  components: {
    ButtonApp,
  },
  name: "HeaderApp",
  props: {
    title: String,
    showAddTask: Boolean,
  },
};
</script>
<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}
</style>
