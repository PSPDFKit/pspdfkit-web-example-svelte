<script>
  import PSPDFKit from "pspdfkit";

  export let pdf;
  export let licenseKey;
  export let baseUrl = "";

  // variable that the parent can bind to for error messages handling
  export let errorMsg = "";

  let instance;

  function handlePDF(element, pdf) {
    load(element, pdf);
    return {
      update(pdf) {
        unload(element);
        load(element, pdf);
      },
      destroy() {
        unload(element);
      }
    };
  }

  async function load(container, pdf) {
    try {
      instance = await PSPDFKit.load({
        container,
        pdf,
        licenseKey,
        baseUrl,
        theme: PSPDFKit.Theme.DARK
      });
      errorMsg = "";
    } catch (error) {
      unload(container);
      errorMsg = error.message;
    }
  }

  function unload(container) {
    if (instance) {
      PSPDFKit.unload(instance);
      instance = null;
    } else {
      PSPDFKit.unload(container);
    }
  }
</script>

<style>
  .container {
    height: 100%;
  }
</style>

<div use:handlePDF={pdf} class="container" />
