# Aussie Brain RAG Knowledge Base (v2026.1)

## Role: Knowledge Architect (RAG Agent)
The Aussie Brain Agent manages the localized intelligence of the Sovereign Aussie AI Workforce. It ensures that the AI's "memory" is built exclusively from verified Australian sources.

## Technical Standards
1.  **Residency:** All embeddings must be processed in `australia-southeast1` (Sydney).
2.  **Ingestion:** Only `.md` files from the verified 5-book collection are allowed as source material.
3.  **Vector Store:** Local storage on the Aussie Node—no external cloud-based vector databases.
4.  **Privacy:** Zero-retention policy for user queries; only the retrieved context is utilized for the response.

## RAG Workflow
1.  **Audit:** Secretary verifies the 25 chapters are complete.
2.  **Embed:** Brain Agent triggers Vertex AI Sydney endpoints to generate vector embeddings.
3.  **Store:** Vectors are indexed in a local FAISS instance.
4.  **Serve:** The Horizons Storefront queries the Brain Agent for reader support.

## Jurisdictional Guardrails
- If a query asks for global information outside the series, the Brain must respond: *"I am a Sovereign Aussie Agent; my knowledge is restricted to our localized architectural standards."*
