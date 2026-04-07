# ipa-archive

Archived/delisted iOS app metadata for ipaTool.

## Structure

- `delisted.json` — index of known delisted apps
- `data/{appId}.json` — per-app metadata with version history

## App JSON Format

```json
{
  "id": "389801252",
  "name": "Instagram",
  "icon_url": "https://...",
  "bundle_id": "com.burbn.instagram",
  "versions": [
    { "version_id": "895063712", "version": "312.1.2" }
  ],
  "delisted": false,
  "added_at": "2026-04-07T10:00:00Z",
  "added_by": "user"
}
```
