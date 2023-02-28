<script lang="ts">
  import {Link} from "svelte-routing"
</script>

<nav>
  <img src="" alt="logo" />

  <ul>
    <Link to="/"><li>Home</li></Link>
    <Link to="contact"><li>Contact</li></Link>
  </ul>
</nav>

<style>
  nav {
    padding: .2em 3em;
    background-color: #ab7941;
    display: flex;
    justify-content: space-between;
  }

  ul {
    display: flex;
    gap: .8em;
  }
</style>
