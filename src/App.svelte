<script lang="ts">
  import { Router, Link, Route } from "svelte-routing";
  import Home from "./routes/Home.svelte";
  import Styles from "./routes/Css.svelte";
  import Mixin from "./routes/Mixin.svelte";
  import Data from "./routes/Data.svelte";
  import Htmls from "./routes/Htmls.svelte";
  import Props from "./routes/Props.svelte";

  export let url: string = "";

  const handleMessage = (e) => {
    const message = e.detail
    console.log(e, message)
    if(message) alert(message)
  }
</script>

<Router url="{url}">
  <nav>
    <Link to="/">回到首页</Link>
  </nav>
  <div>
    <Route path="/"><Home /></Route>
    <Route path="/styles"><Styles /></Route>
    <Route path="/data"><Data /></Route>
    <Route path="/mixin"><Mixin /></Route>
    <Route path="/htmls"><Htmls /></Route>
    <Route path="/props"><Props name="yyds!" on:message={handleMessage} /></Route>
  </div>
</Router>