# Ergane Skills

Reusable agent skills for practical planning. The first skill is **Family Road Trip**: find a trip that works for the people, hunt for better prices, and keep its map, itinerary, reservations and budget aligned.

## Family Road Trip

- Compare suitable hotels and rentals across direct rates, Booking.com and other cash channels, Airbnb/Vrbo, card travel portals and eligible loyalty awards.
- Check discounts, member rates, promo eligibility, credits and points value against the best comparable cash price. Recommend keeping points when the redemption is weak.
- Plan comfortable driving days, breaks, short walks, sightseeing, nature stops and food on the actual route.
- Verify room layouts, ground-floor/access requests, pickup/large-vehicle parking, garage limits, overnight rules and extra fees.
- Create or update shared maps with directions, parking, optional stops, restaurants, transit and walking loops; maintain translated itineraries when requested.
- Track refundable rates, cancellation deadlines, paid versus due amounts, cash and points, and changes across the whole plan.

This is an instruction package for a capable agent, not a hotel booking engine. Live prices, account-specific points offers, map editing and bookings depend on the tools and accounts available to that agent. It does not include credentials, a hosted service or a background price monitor. Research does not authorize payment, external messages or publishing private trip details.

## Install just the skill in Codex

Paste this into a Codex chat:

```text
$skill-installer install https://github.com/Ergane-IO/agent-skills/tree/v0.1.0/skills/family-road-trip
```

The tagged link installs a known version. For the current development version, replace `v0.1.0` with `main`. If the skill does not appear after installation, restart the client. Updating an existing installation may require replacing it through the installer; do not install duplicate copies with the same name.

Then ask:

```text
Use $family-road-trip to plan a family road trip. Compare cheaper stays
across direct booking, cash platforms, rentals and my points options.
Include realistic driving breaks, parking for our vehicle, sightseeing,
food, a shared map and a total cash-and-points budget.
```

Provide dates, starting point, return deadline, travelers/ages, vehicle, comfortable driving/walking limits, cancellation preference, budget and loyalty currencies. Existing plans can be updated instead of rebuilt.

## Install the plugin/catalog

For Codex versions supporting plugin marketplace commands:

```sh
codex plugin marketplace add Ergane-IO/agent-skills --ref v0.1.0
codex plugin add ergane-skills@ergane
```

The repository includes a portable `plugin.json` and a repo marketplace catalog. This is GitHub distribution, not a listing in the public plugin directory. Client support varies; the standalone skill installation above is another path. See the [official packaging documentation](https://developers.openai.com/plugins/build/plugins) for supported plugin surfaces and setup.

To follow ongoing releases, use `--ref main` instead of the tag and refresh with `codex plugin marketplace upgrade ergane`. For a pinned installation, choose a newer release tag explicitly. Install either the plugin or the standalone skill to avoid duplicate skill entries.

## Download or use another compatible agent

The [latest release](https://github.com/Ergane-IO/agent-skills/releases/latest) includes a standalone skill ZIP, a plugin ZIP and SHA-256 checksums. Extract the standalone ZIP into your agent's supported skills directory, keeping the entire `family-road-trip` folder and references together. Other agents need Agent Skills support and suitable tools; their installation paths and browser/connectors differ. Cross-client execution has not been verified.

The skill follows the `SKILL.md` format. The optional `agents/openai.yaml` contains Codex presentation metadata. See [official skill documentation](https://learn.chatgpt.com/docs/build-skills) for local discovery and installation behavior.

## Structure and contributions

```text
plugin.json
.agents/plugins/marketplace.json
skills/family-road-trip/
  SKILL.md
  agents/openai.yaml
  references/
    price-hunting.md
    maps-and-sharing.md
    reservations-and-budget.md
    trip-record.md
```

Keep workflows general and tool-adaptive. Do not commit real trip records, email addresses, account balances, payment details, confirmation codes, browser captures or private map/document links. Prices and policies belong in the active trip's evidence, not in the reusable skill.

When adding skills, use `skills/<skill-name>/SKILL.md`, keep descriptions specific, and link substantial supporting references from the entrypoint. Bump `plugin.json` and publish a tagged release for distributed changes. Validate names/frontmatter, all local reference links, package contents and installation before calling a release ready. Behavioral scenarios are in [EVALUATION.md](EVALUATION.md).

MIT licensed. No affiliation with the travel platforms named as examples.
