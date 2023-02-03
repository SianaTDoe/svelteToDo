<script lang="ts">
    import TodoElement from "./TodoElement.svelte";
    export let todos;
</script>

<table>
    <thead>
        <tr>
            <th>Description</th>
            <th>Terminée</th>
        </tr>
    </thead>
    <tbody>
        {#each todos as todo}
            <TodoElement {todo} />
        {/each}
    </tbody>
</table>

<style>
    table {
        border-collapse: collapse;
        text-align: center;
    }
</style>
