<script lang="ts">
  import {Router, Route, Link} from "svelte-routing"
  import Footer from "./components/footer.svelte";
  
  import Header from './components/header.svelte'
  import Contact from "./pages/contact.svelte";
  import Home from "./pages/home.svelte";
  import NotFound from "./pages/NotFound.svelte";

</script>

<main>
  <Router>
    <Header />
    <Route path="/" component={Home} />
    <Route path="contact" component="{Contact}" />
    <Route component={NotFound} />
    <Footer />
  </Router>
</main>


