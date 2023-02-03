<script lang="ts">
  import Form from "./lib/Form.svelte";
  import TodoList from "./lib/TodoList.svelte";

  let todos = [
    { id: 1, text: "se réveiller", isDone: true },
    { id: 2, text: "se lever", isDone: false },
    { id: 3, text: "ouvrir les yeux", isDone: false },
  ];

  class Todo {
    id: number;
    text: string;
    isDone: boolean;

    constructor(text: string) {
      this.id = 1;
      this.text = text;
      this.isDone = false;
    }
  }

  export class List {
    todos: Todo[] = [
      { id: 1, text: "se réveiller", isDone: true },
      { id: 2, text: "se lever", isDone: false },
      { id: 3, text: "ouvrir les yeux", isDone: false },
    ];

    public addTodo(todo: string) {
      const newTodo = new Todo(todo);
      this.todos.push(newTodo);
    }
  }
</script>

<main>
  <TodoList {todos} />
</main>

<style>
</style>
