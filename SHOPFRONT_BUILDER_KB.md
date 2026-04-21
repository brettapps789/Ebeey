# Shopfront Builder Knowledge Base (2026.1)

## Role: Storefront Integration Architect
The Shopfront Builder Agent manages the transformation of raw ebook projects into commercial listings.

## Listing Components (Next.js)
1.  **Card UI:** Responsive book card with hover effects (Tailwind).
2.  **Detail Page:** Chapter list, metadata summary, and accessibility-compliant HTML description.
3.  **Checkout:** Secure Stripe integration module.

## Automation Workflow
1.  **Input:** Completed `EbookProject` from GitHub.
2.  **Process:** Map `metadata.json` to React components.
3.  **Output:** Live `/shop` endpoint on the Horizons URL.

## Technical Standards
- **Performance:** 90+ Lighthouse score (LCP < 2.5s).
- **Security:** CSRF protection and Secure Cookie handling for Stripe sessions.
