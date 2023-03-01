<script lang="ts">
  import SvelteIcon from '../assets/svelte.svg'
  import GithubIcon from '../assets/github.svg'
  import EmailIcon from '../assets/email.svg'
</script>

<section id="container">
  <img src={SvelteIcon} alt="Yo" />
  <h1>Elias Pereyra</h1>
  <p>I'm a web developer,</p>
  <p>You can find me here:</p>
  <div>
    <a href="https://github.com/EliasPereyra"><img id="github-icon" src={GithubIcon} alt="github icon" /></a>
    <a href="mailto:eliaspereyra_gomez@hotmail.com"><img id="email-icon" src={EmailIcon} alt="email icon" /></a>
  </div>
</section>

<style>
  #container {
    margin-top: 1em;
    padding: 2em;
    display: flex;
    flex-direction: column;
    gap: 1em;
    align-items: center;
  }

  p {
    margin: 0;
  }

  :is(#github-icon, #email-icon) {
    width: 3em;
    transition: scale .2s ease-in-out;
  }
  :is(#github-icon, #email-icon):hover {
    scale: 1.2;
  }
</style>
