<script>
    //import { TasksMethods } from '../api/tasksMethods';
    export let user = null;
    let newTask = '';

    const handleSubmit = async () => {
      if (!newTask) return;

      await Meteor.callAsync('tasks.insert', newTask);

      // Clear form
      newTask = '';
    }
</script>

<form class="task-form" on:submit|preventDefault={handleSubmit}>
    <input
            type="text"
            name="text"
            placeholder="Type to add new tasks"
            bind:value={newTask}
    />
    <button type="submit">Add Task</button>
</form>
