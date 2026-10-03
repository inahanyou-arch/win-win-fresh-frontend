# WIN & WIN FRESH BV — Frontend Only

This repository contains only the complete responsive frontend:

- HTML, CSS and JavaScript
- Dutch, Turkish and English languages
- Product catalogue, filters and premium product images
- Responsive mobile/desktop layout
- Enquiry cart and required customer fields
- Payment method selection UI
- Company information and contact sections

It contains no database, server, admin panel or payment processing code.

## Open locally

For a quick look, open `index.html` in a browser. For full browser compatibility, serve the folder with any static server, for example:

```bash
npx serve .
```

## Upload to GitHub

Upload everything inside this folder to the root of your repository. It works with GitHub Pages because all assets use relative paths.

## Connect your backend later

Edit `config.js` and add your order API endpoint:

```js
window.WINWIN_CONFIG={
  orderEndpoint:'https://your-api.example.com/orders'
};
```

The frontend sends JSON containing:

- locale
- customer name, company, email, telephone and address
- selected payment method
- order notes
- products, quantity, price and requested weight where applicable

Your backend must allow requests from your frontend domain (CORS) and return a successful JSON response.

## Important

The payment options are interface selections only. Credit/debit card, PayPal and iDEAL require separate secure provider integrations on your backend. Never place payment secret keys in `config.js` or any frontend file.
