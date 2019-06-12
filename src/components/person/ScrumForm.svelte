<script>
    import { Field, Input } from 'svelma'
    let name = "James Swash"
    
</script>


<Field label="Name">
  <Input type="text" bind:value={name} placeholder="Text input" />
</Field>

<Field label="Textarea"> 
  <Input type="textarea" maxlength="200" />
</Field>