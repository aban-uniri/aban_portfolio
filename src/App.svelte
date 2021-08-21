<!-- App.svelte -->
<script>
  import { Router, Route } from "svelte-routing";
  import Profile from "./views/Profile.svelte";
  export let url = "";
</script>

<Router {url}>
  <Route path="/" component={Profile} />
</Router>
