# Acme Store Ecommerce Demo

Acme Store is a static ecommerce storefront demo with a pet-retailer-inspired
layout. It includes promotional content, category navigation, a product grid,
client-side add-to-cart interactions, and a mock order-confirmation page. The
sample products are general merchandise rather than pet supplies.

## Pages and features

- `index.html` is the storefront with a promotional hero, category navigation,
  and sample products.
- Add-to-cart buttons update the cart display and order summary in the browser.
- `checkout.html` is a static order-confirmation page linked from the storefront.
- `styles.css` contains the site styles, and `app.js` handles the demo cart and
  checkout navigation.

This project is a front-end demo only. It has no product database, account
system, working search, payment processing, or order submission. The cart is
held in browser memory and is not saved between pages or visits.

## Run locally

From the repository root, open a terminal and run:

```powershell
cd Ecommerce
py -m http.server 4000
```

Then visit <http://localhost:4000> in your browser. Keep the server running
while browsing; press `Ctrl+C` in the terminal to stop it.

Alternatively, if Node.js is installed, run `npx serve .` from this folder.

## PATCHWORK component mapping

Editable components use a unique `data-patchwork-id`, a corresponding CSS
selector, and an entry in `patchwork.map.json`. When adding or changing an
editable component:

1. Add its ID to the appropriate page (`index.html` or `checkout.html`).
2. Add its styles to `styles.css`.
3. Add its mapping to `patchwork.map.json`.
4. From this folder, run `node check-map.mjs` to validate the IDs and selectors.

The `checkout-button` mapping starts with a blue background (`#2563eb`), white
text, an 8px border radius, `12px 20px` padding, and a font weight of 600.
