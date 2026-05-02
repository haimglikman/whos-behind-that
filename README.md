## Changelog

### v1.2
- Reweighted scoring: hidden interest 55%, modus operandi 35%, public narrative 10%
- Updated Claude prompt: explicit manipulation detection philosophy — scores who benefits and how it was built, not just what it says
- UI labels now show dimension weights in entity match cards
- Richer 2–3 sentence "why" explanations citing specific post phrases and hidden interests served
- Demo scores recalculated under new model

### v1.1
- AI scoring engine: narrative matching now uses Claude AI (claude-sonnet) to semantically score post text against each entity's public narrative, interest, and modus operandi
- Post history tab: every analysis logged with URL, timestamp, score, and top entity matches
- Scan counter: sidebar shows total scans run and timestamp of last scan
- Version badge: displayed in sidebar, auto-increments with each release
- Post text input: paste area for post content (required due to browser CORS restrictions on social APIs)
- Dual API keys: separate fields for Anthropic (Claude scoring) and Hive (image AI detection)

### v1.0
- Initial release: core app, 20-entity Israeli-Palestinian conflict database, demo scenarios, editable entity database, Hive image detection
