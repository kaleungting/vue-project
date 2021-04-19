<template>
  <header>
    <h1>{{ title }}</h1>
    <Button
      :text="taskToggle ? 'Close' : 'Add Task'"
      :color="taskToggle ? 'red' : 'green'"
      @btn-click="$emit('show-add-task')"
      :taskToggle="taskToggle"
    />
    <!-- <Button text="Update Task" color="blue" />
    <Button text="Delete Task" color="red" /> -->
  </header>
</template>

<script>
import Button from "./Button";

export default {
  name: "Header",
  props: {
    title: {
      type: String,
      default: "Blank",
    },
    taskToggle: Boolean,
  },
  components: {
    Button,
  },
};
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin: 10px;
}
</style>