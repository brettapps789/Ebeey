# Hostinger & Horizons MCP Knowledge Base (v2026.1)

## API Authentication
- **Hostinger Bearer Token:** `lcSHBeX3PH1tZIjmBZqBBbYhycm0yljnYUZUgEIv2386ca84`
- **Horizons API Key:** `lcSHBeX3PH1tZIjmBZqBBbYhycm0yljnYUZUgEIv2386ca84` (Unified Key)
- **Base URL:** `https://developers.hostinger.com`

## Hostinger Horizons (AI App Builder)
- **Purpose:** Rapidly building the "Ebeey" ebook storefront.
- **Integration Points:**
    - **Prompt-to-App:** The agent can use the Horizons interface to generate React-based components for book previews.
    - **Stripe Module:** Horizons apps natively support Stripe integration for 2026 e-commerce standards.
    - **Custom APIs:** Use the `API Module` within Horizons to fetch real-time data from the `Ebook-Architect` backend.

## Core Operations

### 1. Portfolio Management
- **Endpoint:** `/api/domains/v1/portfolio`
- **Use Case:** Identifying available domains for ebook landing pages.

### 2. DNS Automation
- **Endpoint:** `/api/dns/v1/zones/{zone}/records`
- **Mandatory Records for Ebeey:**
    - `A` record pointing to the static content server.
    - `CNAME` for `www` redirection.
    - `TXT` for domain ownership verification (GitHub/Google).

### 3. Deployment Workflow
1.  **Poll Portfolio:** Check if the requested domain exists.
2.  **Verify Subscription:** Ensure an active hosting plan is linked.
3.  **Update DNS:** Configure records for the `Ebook-Architect` frontend.
4.  **Validate SSL:** Verify that Hostinger's automated SSL provisioning is triggered.

## Error Handling
- **401:** Invalid API Key.
- **404:** Resource (Domain/Subscription) not found.
- **429:** Rate limit exceeded (Implement exponential backoff).
