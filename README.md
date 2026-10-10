# Acme Store Ecommerce Demo

Acme Store is the controlled demo website designed for the **Patchwork** visual website-editing platform. It includes promotional content, category navigation, a product grid, client-side add-to-cart interactions, and a mock order-confirmation page.

## Project Structure

```text
Ecommerce/
├── index.html          # Storefront with hero, categories, products, and cart
├── checkout.html       # Static order confirmation page
├── styles.css          # Site stylesheet with scoped component classes
├── app.js              # Client-side demo cart and navigation logic
├── patchwork.map.json  # Component mapping schema for Patchwork Visual Editor
└── check-map.mjs       # Validation script for IDs, selectors, and mapping
```

## Run Locally

From the repository root, navigate into `Ecommerce` and start a local HTTP server:

### Option 1: Python (Port 3000 - matches Patchwork Visual Editor)
```powershell
cd Ecommerce
python -m http.server 3000
```

> **Note:** If your editor is configured for port 4000, simply run:
> ```powershell
> python -m http.server 4000
> ```

### Option 2: Node.js
```powershell
cd Ecommerce
npx serve -l 3000 .
```

Then visit <http://localhost:3000> (or <http://localhost:4000>) in your browser or through the **Patchwork Visual Editor**.

## Validate PATCHWORK Component Mapping

To verify that all `data-patchwork-id` attributes, CSS selectors, and mappings in `patchwork.map.json` are consistent:

```powershell
cd Ecommerce
node check-map.mjs
```
