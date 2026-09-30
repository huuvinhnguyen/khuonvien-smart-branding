# Naming Convention

## Campaign ID
Format:
`KVS-CAM-YYYY-NNN`

Example:
`KVS-CAM-2026-001`

## Content ID
Format:
`KVS-<TYPE>-NNN`

Common types:
- `VID` — video
- `IMG` — image / static post
- `DOC` — long-form/document content

Example:
`KVS-VID-001`

## File naming
Final published/exported media:
`<CONTENT-ID>_Final.<ext>`

Examples:
- `KVS-VID-001_Final.mp4`
- `KVS-IMG-003_Final.png`

Working versions:
`<CONTENT-ID>_<stage>-vN.<ext>`

Examples:
- `KVS-VID-002_Cut-v1.mp4`
- `KVS-VID-002_Voice-v2.m4a`

## GitHub campaign path
`campaigns/YYYY/<CAMPAIGN-ID>/`

Recommended structure:
```text
campaigns/2026/KVS-CAM-2026-001/
├── brief.md
├── content/
├── scripts/
├── publishing/
└── analytics/
```

## Publishing package
`campaigns/YYYY/<CAMPAIGN-ID>/publishing/<CONTENT-ID>.md`

## Analytics record
`campaigns/YYYY/<CAMPAIGN-ID>/analytics/<CONTENT-ID>.md`

## ClickUp task naming
Prefer role + action + ID:
- `[Content Planner] Brief KVS-VID-002`
- `[Script Writer] Script KVS-VID-002`
- `[Production] Shoot KVS-VID-002`
- `[Editor] Edit KVS-VID-002`
- `[Reviewer] Review KVS-VID-002`
- `[Publisher] Publish KVS-VID-002`
- `[Analytics] Analyze KVS-VID-002`

## General rules
- IDs are stable; titles can change.
- Do not reuse an old content ID for a new concept.
- Keep filenames ASCII-friendly where practical.
- `Final` means approved export intended for publishing, not just latest work-in-progress.
- GitHub is the source of truth for text/process; Drive is the source of truth for media assets.
