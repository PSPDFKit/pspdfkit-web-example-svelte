<script>
  import PSPDFKit from "./PSPDFKit.svelte";

  let doc = "example.pdf";
  let errorMsg = "";

  function openDocument(e) {
    doc = window.URL.createObjectURL(e.target.files[0]);
  }
</script>

<style>
  :global(body) {
    height: 100vh;
    margin: 0;
  }
</style>

<form>
  <input type="file" on:change={openDocument} accept="application/pdf" />
</form>
<span class="error">{errorMsg}</span>
<PSPDFKit {doc} bind:errorMsg />
