# zeroarc-report-assets

Public asset hosting for ZeroArc weekly report charts.

**This repo contains only chart images** — no source data, no business context, no client information beyond what's already public on the web. The reports themselves live in private Notion teamspaces and hot-link these images via `raw.githubusercontent.com` URLs.

## Structure

```
charts/
  {brand}/
    {YYYY-MM-DD}/
      sessions-12wk.png
      mrr-90d.png
      gsc-clicks-90d.png
      geo-by-engine.png
      content-cadence-8wk.png
      top-sources.png
```

## Why public?

Notion image blocks need a publicly-fetchable URL. The images themselves don't contain identifying business detail — they're traffic curves, engagement charts, generic visual summaries. The URLs are hot-linked from inside private Notion pages that only authorised teamspace members can see.

## Hot-link pattern

```
https://raw.githubusercontent.com/jennifer509/zeroarc-report-assets/main/charts/{brand}/{date}/{name}.png?v={timestamp}
```

The `?v={timestamp}` cache-buster forces Notion to fetch fresh images on each weekly run.

## Maintained by

Auto-pushed by `scripts/weekly_brief.py` in the [zeroarc-aios](https://github.com/jennifer509/zeroarc-aios) workspace.
