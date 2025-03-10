> ⚠️ **Repository Moved**  
> This repository has been moved to https://github.com/PSPDFKit/nutrient-web-examples/tree/main/examples/svelte.  
> Please update your bookmarks and issues accordingly.
>
> This repo is now archived and will no longer receive updates.

# Nutrient Web SDK Example - Svelte

This example shows how to integrate [Nutrient Web SDK](https://www.nutrient.io/sdk/web/) into a [Svelte](https://svelte.dev) app.

## Prerequisites

- [Node.js](http://nodejs.org/)

## Support, Issues and License Questions

PSPDFKit offers support for customers with an active SDK license via https://www.nutrient.io/support/request/

Are you [evaluating our SDK](https://www.nutrient.io/try/)? That's great, we're happy to help out! To make sure this is fast, please use a work email and have someone from your company fill out our sales form: https://www.nutrient.io/sales/

## Getting Started

Clone the repo:

```bash
git clone https://github.com/PSPDFKit/pspdfkit-web-example-svelte.git
cd pspdfkit-web-example-svelte
```

Install the project dependencies with `npm`:

```bash
npm install
```

In order to make the Nutrient Web SDK's library available for building, we have to copy the `nutrient-viewer-lib/` directory from `node_modules/nutrient/dist/` into the `public/` directory. This is done in the `package.json` script `verify-installation` which is executed by `dev` script.

## Running the Example

We are ready to launch the app! 🎉

```bash
npm run dev
```

You can now open http://localhost:8080/ in your browser and enjoy!

## License

This software is licensed under a [modified BSD license](LICENSE).

## Contributing

Please ensure
[you have signed our CLA](https://www.nutrient.io/guides/web/current/miscellaneous/contributing/) so that we can
accept your contributions.
