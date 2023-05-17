<template>
  <div class="chris-todo">
    <div class="title has-text-centered">
      Chris Todo
    </div>

    <form @submit.prevent="addTodo">
      <div class="field has-addons mb-5">
        <div class="control">
          <input
            v-model="newTodoContent"
            class="input"
            type="text"
            placeholder="Add a Todo">
        </div>
        <div class="control">
          <button
            :disabled="!newTodoContent"
            class="button is-info">
            Add
          </button>
        </div>
      </div>
    </form>

    <div
      v-for="todo in todos"
      class="card mb-5">
      <div class="card-content">
        <div class="content">
          <div class="columns is-mobile is-vcentered">
            <div class="column">
              {{ todo.content }}
            </div>
            <div class="column is-5 has-text-right">
              <button class="button is-light">
                &check;
              </button>
              <button class="button is-danger ml-2">
                &cross;
              </button>
            </div>
          </div>
        </div>
      </div>
    </div>

  </div>
</template>
//Todo: Watch and code -> 
<script setup>
/* 
  imports
*/
import { ref } from "vue";
import { v4 as uuidv4 } from "uuid";

/* 
  todos
*/
const todos = ref([
  // {
  //   id: 'id1',
  //   content: 'Einkaufen',
  //   done: false
  // },
  // {
  //   id: 'id2',
  //   content: 'Staubsaugen',
  //   done: true
  // },
  // {
  //   id: 'id3',
  //   content: 'Essen kochen',
  //   done: false
  // }
])

/* 
  add todo
*/
const newTodoContent = ref('')

const addTodo = () => {
  const newTodo = {
    id: uuidv4(),
    content: newTodoContent.value,
    done: false
  }

  todos.value.unshift(newTodo)
  newTodoContent.value = ''
}

</script>

<style>
@import 'bulma/css/bulma.min.css';

.chris-todo {
  max-width: 400px;
  padding: 20px;
  margin: 0 auto;
}
</style>
