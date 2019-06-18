<script>
    import { Field, Input } from 'svelma'
    let name = "James Swash"
    
</script>


<input type="text" bind:value={name} placeholder="Text input" />


<Field label="Textarea"> 
  <Input type="textarea" maxlength="200" />
</Field>