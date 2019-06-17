<script>
  import { Button, Field, Input } from "svelma";
  const URL = "http://127.0.0.1:8282/person";
  let username = '';

  export let person = {
    username: null,
    email: null
  };

  export function AddPerson() {
    console.log(username)
    person.username = username;
    let json = JSON.stringify(person);
    let requestObject = {
      headers:{
        'content-type':'application/jso'
        },
      body: json,
      method: "POST",
      mode: "no-cors"
    }
    console.log(person);
    fetch(URL, requestObject)
    .then(data=>{data.json})
    .then(res=>{console.log(res)})
    .catch(err=>{console.log(err)})
  }
</script>

<h2>Create New Person</h2>

<Field label="Name">
  <Input type="text" bind:value={username} placeholder="Name..." />
</Field>

<Field label="Email">
  <Input type="email" bind:value={person.email} placeholder="Email address..." />
</Field>

<p>
HI there {username}
</p>

<Button type="is-dark" on:click={AddPerson}>Add To Team</Button>
