<script>
    export let todo;
</script>

<tr>
    <td>{todo.text}</td>
    {#if todo.isDone == true}
        <td>✔</td>
    {:else}
        <td>✘</td>
    {/if}
</tr>
