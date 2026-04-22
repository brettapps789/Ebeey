# Sheets Database Knowledge Base (v2026.1)

## Role: Data Architect (Sheets Agent)
The Sheets Database Agent manages the structured, tabular data of the Sovereign Aussie AI Workforce. It serves as the relational layer for project tracking and customer management.

## Database Schema (Relational Tables)

### 1. Inventory Table
- **Columns:** `Book ID`, `Title`, `Status`, `KDP_Version`, `GitHub_Repo`.
- **Purpose:** Tracking the production lifecycle of every title in the empire.

### 2. Customers Table
- **Columns:** `Customer ID`, `Email`, `Purchase_Date`, `Product_ID`, `Status`.
- **Purpose:** Managing the lead funnel and post-purchase relationships.

### 3. Finances Table
- **Columns:** `Date`, `Description`, `Category`, `Amount_AUD`, `GST_Payable`.
- **Purpose:** Providing the raw data for the Accountant Agent's Profit & Loss statements.

## Standard Operating Procedures (SOPs)
1.  **Sync Triggers:** Every Stripe checkout event must insert a record into the `Customers` and `Finances` tables.
2.  **Repo Creation:** Every new GitHub repository initialization must insert a record into the `Inventory` table.
3.  **Jurisdiction:** The spreadsheet must be owned by the verified `brettapps.com` Google account, ensuring Australian data residency.

## Technical Constraints
- **Format:** RAW value input to ensure binary/technical data integrity.
- **Concurrency:** Uses append logic to prevent row-locking conflicts during high-volume sales.
