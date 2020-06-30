<script>
  import PSPDFKit from "pspdfkit";

  export let doc;
  export let licenseKey;
  export let baseUrl = "";

  // variable that the parent can bind to for error messages handling
  export let errorMsg = "";

  let instance;

  function handlePDF(element, doc) {
    load(element, doc);
    return {
      update(doc) {
        unload(element);
        load(element, doc);
      },
      destroy() {
        unload(element);
      }
    };
  }

  async function load(container, doc) {
    try {
      instance = await PSPDFKit.load({
        container,
        document: doc,
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

<div use:handlePDF={doc} class="container" />
