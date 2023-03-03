<script ln="ts">
  import {Cloudinary} from '@cloudinary/url-gen'
  import {Resize} from '@cloudinary/url-gen/actions'
  import { crop } from '@cloudinary/url-gen/actions/resize';
  import Dropzone from 'dropzone'
  import {onMount} from 'svelte'

  import 'dropzone/dist/dropzone.css'

  const cloudinary = new Cloudinary({
    cloud: {
      cloudName: ""
    },
    url: {
      secure: true
    }
  })

  onMount(() => {
    const dropzoneElem = new Dropzone('#dropzone', {
    acceptedFiles: ".jpg,.png,.webp", 
    createImageThumbnails: true,
    maxFilesize: 2,
    maxThumbnailFilesize: 10,
    uploadMultiple: false,
    defaultTemplate: null,
  })

  dropzoneElem.on("sending", (file, xhr, formData) => {
    formData.append("upload_preset", process.env.upload_preset)
    formData.append("timestamp", Date.now() / 1000)
    formData.append("api_key", process.env.api_key)
    console.log("sending")
  })

  dropzoneElem.on("success", () => {
    console.log("Sucess!!")
  })

  dropzoneElem.on("error", () => {
    console.error("Error: ")
  })

  dropzoneElem.on("addedfile", function(file) {
    console.log("added!")
  })
  })
</script>

<div>
  <form id="dropzone" action="https://api.cloudinary.com/v1_1/${process.env.cloud_name}/image/upload">
    <button>Upload file</button>
    <strong>or <span id="drop">drop</span> here a file</strong>
  </form>
</div>

<style>
  form {
    padding: 2em;
    display: flex;
    gap: 1em;
    flex-direction: column;
    align-items: center;
  }

  form > button {
    width: 10em;
  }

  #drop {
    color: #6b3f09ec;
  }
</style>
