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

    <div
      v-for="i in 3" 
      class="card mb-5"
    >
      <div class="card-content">
        <div class="content">
          <div class="columns is-mobile is-vcentered">
            <div class="column">
              Einkaufen
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

//Todo: Watch and code -> 5:28 Elements & Styles - Todo List

<style>
@import 'bulma/css/bulma.min.css';

.chris-todo {
  max-width: 400px;
  padding: 20px;
  margin: 0 auto;
}
</style>
