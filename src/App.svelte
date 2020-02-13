<script>
  import PSPDFKit from "./PSPDFKit.svelte";

  const LICENSE_KEY = process.env.PSPDFKIT_LICENSE_KEY;
  let pdf = "example.pdf";
  let errorMsg = "";

  function openPDF(e) {
    pdf = window.URL.createObjectURL(e.target.files[0]);
  }
</script>

<style>
  :global(body) {
    height: 100vh;
    margin: 0;
  }
</style>

<form>
  <input type="file" on:change={openPDF} accept="application/pdf" />
</form>
<span class="error">{errorMsg}</span>
<PSPDFKit {pdf} licenseKey={LICENSE_KEY} bind:errorMsg />
