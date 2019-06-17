<script>
  import { Button, Field, Input, Modal } from "svelma";
  import "bulma/css/bulma.css";
  import Person from "./components/person/person.svelte";
  import NewPerson from "./components/person/newPerson.svelte";
  import NewActivity from "./components/activity/newActivity.svelte";

  let activityList = [];
  let addUser = false;

  function addActivity() {
    activityList = [...activityList, {}];
  }

  function newPerson() {
    addUser = !addUser;
  }

  function removeActivity() {
    let count = activityList.length;
    console.log(activityList);
    activityList = activityList.slice(0, count - 1);
    console.log(activityList);
  }
</script>

<Button type="is-primary" on:click={newPerson}>Add to the team</Button>
<Modal bind:active={addUser}>
  <p>
    <NewPerson />
  </p>
</Modal>

<Button type="is-success" on:click={addActivity}>Add an activity</Button>

<button on:click={removeActivity}>Remove last activity</button>

{#each activityList as newActivitiy}
  <NewActivity a="b" />
{/each}
