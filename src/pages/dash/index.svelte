<script>
  import { slide, fade } from 'svelte/transition'
  import { setContext, getContext, onMount } from 'svelte'
  import Box from '../../comp/ui/box.svelte';
  import Tab from '../../comp/ui/tab.svelte';
  import { afterPageLoad } from "@sveltech/routify";
  import { metatags } from '@sveltech/routify';
  metatags.title = "dashboard home";

  let userData;
  let loggedIn;
$afterPageLoad(page => {
  userData = getContext("userData");
  loggedIn = getContext("loggedIn");
})

  console.log(userData);
  console.log(loggedIn);
</script>

<style>
</style>
<div class="dbindex" in:fade={{duration:100}}>
    <h1>dashboard</h1>
</div>
