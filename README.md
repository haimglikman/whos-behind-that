## Changelog

### v1.7.3 — bug fix
- Instagram/Facebook actor research now works: a handle input field appears
  automatically when an Instagram or Facebook URL is detected
- Actor research prompt now correctly triggers after analyzing Instagram posts

### v1.7.2 — bug fix
- Fixed actor research prompt not appearing after analyzing Instagram posts
- Instagram handle now extracted from server's oEmbed author_url, not the post URL

### v1.7.1 — bug fix
- Hardcoded default server URL so app works out of the box on any device
- Users no longer need to manually enter the server URL on first visit

### v1.7.0
- Server version badge added to sidebar below main version
- Fetched live from server health check on load — always reflects what's actually deployed
- Updates automatically when server URL changes

### v1.6.2 — bug fix
- Rebuilt entire JavaScript section from scratch after cascading corruption from prior edits
- Fixed: nav tabs not working, analyze button non-functional, version showing incorrectly
- All 50 entities, actor profiles, history, and analysis functions fully restored and verified

### v1.6.1 — bug fix
- Removed DEMOS data object and runDemo() function (260 lines of dead code from v1.5.0)
- Removed orphaned .demo-chip and .demo-label CSS styles
- Fixed entity database badge hardcoded to "20" — now shows correct count of 50
- Fixed wrong syntax in server file

### v1.6.0
- Actor profiles: Claude researches social media actors via OSINT, cached by handle
- Actors tab: browse, view, and delete all profiled actors
- Entity database expanded from 20 to 50 entities
- Media outlets (Al Jazeera, Al-Manar, Press TV) captured as MO instruments of patron entities

### v1.5.1 — bug fix
- Fixed undefined% alignment score when server response omits pre-computed pct field
- Added NaN guard in showResults to prevent rendering errors on malformed scores

### v1.5.0
- Auto-clear analyze tab when navigating away — URL and results reset automatically
- Removed demo scenario buttons from analyze tab
  
### v1.4.0
- Clickable history: every Post History entry opens the full analysis view
- Reframed from "manipulation detection" to "narrative alignment" — whose agenda does this serve?
- New "What this post leaves out" field on each entity match — the missing context
- Alignment color spectrum: cool blue → purple → amber → red-orange (intensity, not danger)
- Overall dial now shows strongest entity name and alignment score, not "manipulation probability"
- Server prompt updated: Claude now identifies missing context per match

### v1.3.0
- Proxy server: post text now fetched automatically from X, Facebook, Instagram
- API keys moved server-side: Anthropic key stored securely as env variable, never in browser
- Users just paste a URL — no setup or keys required
- Graceful fallback: manual text paste if auto-fetch fails (private/deleted posts)

### v1.2.0
- Reweighted scoring: hidden interest 55%, modus operandi 35%, public narrative 10%
- Updated Claude prompt: explicit manipulation detection philosophy — scores who benefits and how it was built, not just what it says
- UI labels now show dimension weights in entity match cards
- Richer 2–3 sentence "why" explanations citing specific post phrases and hidden interests served
- Demo scores recalculated under new model

### v1.1.0
- AI scoring engine: narrative matching now uses Claude AI (claude-sonnet) to semantically score post text against each entity's public narrative, interest, and modus operandi
- Post history tab: every analysis logged with URL, timestamp, score, and top entity matches
- Scan counter: sidebar shows total scans run and timestamp of last scan
- Version badge: displayed in sidebar, auto-increments with each release
- Post text input: paste area for post content (required due to browser CORS restrictions on social APIs)
- Dual API keys: separate fields for Anthropic (Claude scoring) and Hive (image AI detection)

### v1.0.0
- Initial release: core app, 20-entity Israeli-Palestinian conflict database, demo scenarios, editable entity database, Hive image detection
