<script lang="ts">
  import Footer from '../components/footer.svelte'
  import UploadImage from '../components/UploadImage.svelte';
  import CloudinaryLogo from '../components/CloudinaryLogo.svelte';
</script>


  <div class="credits">
    <small>Thanks to </small>
    <a href="https://cloudinary.com" target="_blank" rel="noreferrer"><CloudinaryLogo /></a>
  </div>
  <h1>Customize your image!</h1>
  <UploadImage />
  <Footer />

  <style>
    small {
      font-style: bold;
    }
  
    .credits {
      margin-top: 2em;
  
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
    }
  </style>
