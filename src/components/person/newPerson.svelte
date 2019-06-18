<script>
  import { Button, Field, Input } from "svelma";
  const URL = "http://127.0.0.1:8282/person";
  let username = '';

  export let person = {
    username: null,
    email: null
  };

  export async function AddPerson() {
    const rawResponse = await fetch(URL, {
      method: 'POST',
      headers: {
        'Content-Type': 'application/json',
        'Accept': 'application/json'
      },
      mode: 'cors',
      body: JSON.stringify(person)
    });
    const content = await rawResponse.json();

    console.log(content);
  }
</script>

<h2>Create New Person</h2>


<input type="text" bind:value={person.username} placeholder="Name..." />
<input type="email" bind:value={person.email} placeholder="Email address..." />


<Button type="is-dark" on:click={AddPerson}>Add To Team</Button>
