# Off-site authority plan

On-page SEO is done. What limits rankings now is authority from other sites: links, mentions, and verifiable identity. This file is the working checklist.

## Rules

- **Publish a note about every 2 weeks.** Use the real publish date. Never backdate.
- **Bump `dateModified` and the sitemap `lastmod` only when a page has real content changes.** Don't touch them for a deploy, a CSS tweak, or a nav change.
- **Excerpt, don't duplicate.** LinkedIn articles can't set a canonical tag. Post a 300–500 word excerpt with the core framework and link to the full note.
- **Add schema only for mentions that already exist.** Record each one in the tracker below first.

## Per-note syndication

Work through these from the top. The first four target the most competitive queries.

| Note | LinkedIn article angle | Community targets |
|---|---|---|
| [Tech debt audit](../salesforce-tech-debt-audit.html) | The scoring model: how to rank debt by risk × effort | Salesforce Ben guest post; user-group talk (below) |
| [Flow migration](../salesforce-flow-migration.html) | Migration order, and what breaks when you skip testing | Salesforce Admins blog pitch; Trailblazer Community Flow group |
| [Data readiness for AI](../salesforce-data-readiness-for-ai.html) | What to fix before you turn on Agentforce | Salesforce Ben; r/salesforce Agentforce threads |
| [Lead routing](../salesforce-lead-routing.html) | Speed-to-lead benchmarks and the routing rules that matter | RevOps Co-op; Wizard Ops newsletter |
| [Quote-to-cash audit](../salesforce-quote-to-cash-audit.html) | Why Closed Won data drifts from what finance sees | RevOps Co-op; CPQ groups in the Trailblazer Community |
| [Center of Excellence](../center-of-excellence.html) | The first 90 days of a CoE | Salesforce Admins podcast pitch |
| [Data stewardship](../data-stewardship.html) | Ownership before tooling | Trailblazer Community data quality group |
| [Building brianhong.com](../building-brianhong-com.html) | Design decisions for a one-person consulting site | Web design communities (low priority for Salesforce authority) |

### Community etiquette
- On r/salesforce and in Trailblazer groups, answer the question in the thread first. Link to a note only when it adds something the answer doesn't already cover.
- For guest posts, pitch an angle that isn't already on the site. The goal is a byline and an author-bio link, not duplicate content.

## User-group talk pitch

**Title:** Finding and paying down Salesforce tech debt without stopping the business

**Abstract:** Most orgs carry years of unused fields, overlapping automation, and permission sprawl that nobody wants to touch. This session walks through a repeatable audit: inventory what's in the org, score each item by risk and effort, and sequence the cleanup so the business keeps running. Attendees leave with a scoring worksheet and a 30-day starter plan.

**Contact:** the Columbus, OH Salesforce Admin/Trailblazer Community Group organizers. Nearby Ohio groups (Cleveland, Cincinnati) and virtual groups are second.

## Schema snippets (add only after a mention goes live)

**Article republished or covered elsewhere.** Add to that note's `BlogPosting`:

```json
"subjectOf": [
  { "@type": "Article", "url": "https://example.com/the-mention", "publisher": { "@type": "Organization", "name": "Salesforce Ben" } }
]
```

**Guest post by Brian.** Add the author-page URL to `sameAs` in the Person node on every page that has `"@id": "https://brianhong.com/#person"`.

**Talk given.** Add to the Person node on about.html:

```json
"performerIn": [
  { "@type": "Event", "name": "Finding and paying down Salesforce tech debt", "startDate": "YYYY-MM-DD", "location": { "@type": "Place", "name": "Columbus Salesforce Admin Group" }, "url": "https://trailblazercommunitygroups.com/events/..." }
]
```

## Tracker

| Note | Venue | URL | Date | Schema added? |
|---|---|---|---|---|
| | | | | |
