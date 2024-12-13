# PSPDFKit for Web Example - Svelte

This example shows how to integrate [PSPDFKit for Web](https://pspdfkit.com/web/) into a [Svelte](https://svelte.dev) app.

## Prerequisites

- [Node.js](http://nodejs.org/)

## Support, Issues and License Questions

PSPDFKit offers support for customers with an active SDK license via https://pspdfkit.com/support/request/

Are you [evaluating our SDK](https://pspdfkit.com/try/)? That's great, we're happy to help out! To make sure this is fast, please use a work email and have someone from your company fill out our sales form: https://pspdfkit.com/sales/

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

In order to make the PSPDFKit for Web's library available for building, we have to copy the `pspdfkit-lib/` directory from `node_modules/pspdfkit/dist/` into the `public/` directory. This is done in the `package.json` script `verify-installation` which is executed by `dev` script.

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
[you have signed our CLA](https://pspdfkit.com/guides/web/current/miscellaneous/contributing/) so that we can
accept your contributions.
