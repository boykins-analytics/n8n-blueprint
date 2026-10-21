# Security and responsible disclosure

This is a **non-operational public case study**. It intentionally excludes original n8n exports and production portal code because those contain internal routing references, IDs, integration settings, and embedded assets.

Never post authentication secrets, OAuth tokens, API keys, customer information, real policy records, internal webhook URLs, insurer templates without permission, or production system identifiers.

Before any importable workflow or live demo is released: replace all endpoints and credentials with placeholders, strip execution and pinned data, remove embedded assets unless licensed, review each Code node for hardcoded information, inspect version-control history for leaked values, and test with synthetic records only.

Do not use the case study to issue or represent binding insurance coverage. Report suspected security problems privately to the repository owner rather than opening a public issue containing sensitive details.
