<script>
  import { Button, Field, Input } from "svelma";

  let person = {
    username: "",
    email: ""
  };

  function AddPerson() {}
</script>

<h2>Create New Person</h2>

<Field label="Name">
  <Input type="text" bind:value={person.username} placeholder="Name..." />
</Field>

<Field label="Email">
  <Input type="text" bind:value={person.email} placeholder="Email address..." />
</Field>

<Button type="is-dark" on:click={AddPerson}>Add To Team</Button>
