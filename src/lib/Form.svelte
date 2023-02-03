<script lang="ts">
    export let addTodo;

    let newTodo = "";
    function send() {
        if (!newTodo) {
            alert(newTodo);
        } else{
            addTodo(newTodo);
        }
    }
</script>

<form on:submit={send}>
    <input placeholder="To Do..." bind:value={newTodo} />
    <button type="submit">Add</button>
</form>
