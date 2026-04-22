# Stripe MCP Knowledge Base (v2026.1)

## Role: Payment Infrastructure Architect
The Stripe Agent manages the secure monetization layer of the Sovereign Aussie AI Workforce.

## Commercial Standards (2026)
1.  **Product Naming:** `[Sovereign Gold] Title - Volume X`.
2.  **Currency:** Default to **AUD** for all Australian storefronts.
3.  **Taxation:** Automatically apply 10% GST to all Australian purchases.
4.  **Payouts:** Monthly payouts to the verified business account in Sydney.

## Integration Protocols
- **Sync:** Every `metadata.json` push to GitHub must trigger a `sync_stripe_products` tool call.
- **Security:** Use **Restricted API Keys (RAK)** with specific permissions:
    - `Products: Write`
    - `Prices: Write`
    - `Checkout Sessions: Write`
- **PCI Compliance:** All checkout flows must occur via **Stripe Hosted Checkout** to ensure 0% data exposure on the Aussie Node.

## Error Handling
- **Invalid Key:** Trigger `Sovereign Lock` on the affected project.
- **Sync Conflict:** Perform a 'Read-First' check on Stripe before creating a duplicate product.
