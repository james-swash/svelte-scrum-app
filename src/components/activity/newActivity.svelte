<script>
  import { Field, Input } from "svelma";
  let activity = {
    id: 0,
    activity: "",
    created: "",
    user_id: ""
  };
</script>

<h1>New Activity</h1>
<Field label="Activity">
  <Input
    type="text"
    bind:value={activity.activity}
    placeholder="New activity..." />
</Field>
