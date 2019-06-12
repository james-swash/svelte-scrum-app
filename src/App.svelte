<script>
  import { Button } from 'svelma'
  import Person from './components/person/person.svelte'
</script>

<style>
p {
	background-color: #00d1b2;
    border-color: transparent;
    color: #fff;
}
</style>
<Button type="is-primary" inverted>I am a Button</Button>
<Person/>