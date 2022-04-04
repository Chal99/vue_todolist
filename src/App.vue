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
<style scoped>

body {
  background-color: #abc;
}
*, h1, button {
  font-family: 'Nunito', sans-serif;
}
.fade-enter-active, .fade-leave-active {
  transition: opacity .5s;
}
.fade-enter, .fade-leave-active {
  opacity: 0;
}
.tasks {
  width: 100%;
  max-width: 45rem;
  padding: 1em;
  margin: 1em auto;
  overflow: auto;
  background-color: white;
  box-shadow: 0px .25rem 1rem rgba(black, .25);
}
.tasks__list {
  clear: both;
}
.tasks__item {
  margin-bottom: .5em;
  position: relative;
}
.tasks__item__toggle {
  cursor: pointer;
  width: 100%;
  text-align: left;
  padding: .85em 2.25em .85em 1em;
  background-color: rgba(black, .05);
  border: 1px solid rgba(black, .1);
}
.tasks__item__toggle:hover {
  background-color: rgba(black, .1);
  border-color: rgba(black, .15);
}
.tasks__item__toggle--completed {
  text-decoration: line-through;
  background-color: rgba(green, .15);
  border-color: rgba(green, .2);
}
.tasks__item__toggle--completed:hover {
  background-color: rgba(green, .25);
  border-color: rgba(green, .3);
}
.tasks__item__remove {
  position: absolute;
  height: 100%;
  top: 50%;
  right: 0;
  transform: translateY(-50%);
}
.tasks__item__remove i {
  vertical-align: middle;
}

</style>

