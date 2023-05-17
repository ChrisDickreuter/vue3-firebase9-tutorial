<template>
  <div class="chris-todo">
    <div class="title has-text-centered">
      Chris Todo
    </div>

    <div class="field has-addons mb-5">
      <div class="control">
        <input class="input" type="text" placeholder="Add a Todo">
      </div>
      <div class="control">
        <a class="button is-info">
          Add
        </a>
      </div>
    </div>

    <div v-for="todo in todos" class="card mb-5">
      <div class="card-content">
        <div class="content">
          <div class="columns is-mobile is-vcentered">
            <div class="column">
              {{ todo.content}}
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

/* 
  todos
*/

const todos = ref([
  {
    id: 'id1',
    content: 'Einkaufen',
    done: false
  },
  {
    id: 'id2',
    content: 'Staubsaugen',
    done: true
  },
  {
    id: 'id3',
    content: 'Essen kochen',
    done: false
  }
])

</script>

<style>
@import 'bulma/css/bulma.min.css';

.chris-todo {
  max-width: 400px;
  padding: 20px;
  margin: 0 auto;
}
</style>
