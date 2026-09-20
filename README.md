# VYNK Premium Store

## Run locally
Open `index.html` directly for the simplest option. If your browser blocks local navigation/query behavior, run a local server:
- Python: `python -m http.server 8000`
- Then visit `http://localhost:8000`

No backend is required for the included storefront. Cart data uses localStorage. WhatsApp ordering opens the supplied WhatsApp number with a prefilled message.

## Edit products
Open `assets/app.js` and edit the `PRODUCTS` array. Each product has:
- id
- category
- name
- price
- image
- description
- features
- customization

Add another product object using the same structure. The category pages and product pages are generated automatically.

## Add categories
Edit the `CATEGORIES` object in `assets/app.js`. Add a slug, title, description, and banner image. Then add products whose `category` matches that slug.

## Replace images
Change each product `image` URL. The starter uses remote Unsplash images so the package stays small. For production, download optimized WebP/JPG files into an `assets/images/` folder and update the paths.

## Works immediately
- Responsive multi-page storefront
- Homepage, category pages, product pages, cart and contact page
- Search
- Cart persistence with localStorage
- Quantity changes/removal/subtotal
- Product customization selectors
- WhatsApp order links with product, quantity and customization
- Breadcrumbs and functional navigation
- Mobile navigation
- Contact form validation (static form; see backend note)

## Backend / production notes
No backend is needed for browsing, cart and WhatsApp ordering. The contact form is front-end only and does not send email. To receive form submissions, connect it to a service such as Formspree, Netlify Forms, a custom API, or a server-side mail endpoint.

For a real Shopify-like checkout, inventory, payment gateway, customer accounts, order database, analytics, and admin product management, add a backend/ecommerce platform. WhatsApp ordering remains usable without one.
