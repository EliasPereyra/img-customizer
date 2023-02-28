<script>
  import ErrorIcon from '../assets/error.svg'
</script>

<div id="container">
  <img src={ErrorIcon} alt="An error icon" />
  <h1>An error here</h1>
  <p>That page does not exist</p>
</div>

<style>
  #container {
    margin-top: 1em;
    display: flex;
    flex-direction: column;
    gap: 1em;
    align-items: center;
    justify-content: center;
  }

  img {
    width: 6em;
  }

  h1 {
    color: rgb(231, 11, 11);
  }

  p {
    color: rgb(172, 7, 7);
  }
</style>
