# Horizons Agent Knowledge Base (v2026.2)

## Role: AI App Architect
The Horizons Agent is responsible for transforming ebook metadata and content into a functional e-commerce application. It operates at the Application Layer, leveraging Hostinger's Horizons AI.

## Agent Guidelines
1.  **Architecture:** Always prefer **Next.js** for SEO-optimized ebook landing pages.
2.  **State Management:** Use **Supabase** for storing user reading progress and book purchases.
3.  **Theming:** Adhere to "Reflowable-Plus" visual standards (Dynamic dark/light mode).

## Integration Protocol
- **Trigger:** Creation of a new `EbookProject` in `Ebook-Architect`.
- **Sync:** Transfer `metadata.json` to the Horizons `Storefront` database.
- **Validation:** Ensure the `HORIZONS_API_KEY` is active before triggering deployment.

## Deployment Checklist
- [ ] Generate App Blueprint.
- [ ] Map Stripe Product IDs to Ebook Chapters.
- [ ] Connect Domain (via Hostinger DNS Tools).
- [ ] Deploy to `*.hostingerapp.com`.
