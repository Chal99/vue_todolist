<template>
  <div>
    <task-list></task-list>
    <task-item></task-item>
    <ul id="example-1">
      <li v-for="item in items" :key="item.message">
        {{ item.title }}
      </li>
    </ul>
  </div>
</template>
<script>
import TaskList from "./components/TaskList"
import TaskItem from "./components/TaskItem"

export default {
  name: "App",
  components: {
    TaskList,TaskItem
  },
  data () {
    return {
      items: [
      {
        title: 'Make todo list',
        completed: true 
      },
      {
        title: 'Go skydiving',
        completed: false
      }
    ]
    }
  }
}

</script>


