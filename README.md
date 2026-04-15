# ipa-archive

Community-driven archived/delisted iOS app metadata for ipaTool.

## Structure

- `data/{appId}.json` — per-app metadata with version history

## App JSON Format

```json
{
  "id": "389801252",
  "name": "Instagram",
  "icon_url": "https://...",
  "icon_bak_url": "data:image/png;base64,...",
  "bundle_id": "com.burbn.instagram",
  "versions": [
    {
      "version_id": "895063712",
      "version": "312.1.2",
      "description": "Last version with feature X"
    }
  ],
  "delisted": false,
  "added_at": "2026-04-07T10:00:00Z"
}
```

### Field Reference

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | ✅ | App Store app ID |
| `name` | string | ✅ | App display name |
| `icon_url` | string | ✅ | Icon URL from iTunes API |
| `icon_bak_url` | string | ❌ | Base64-encoded icon image (data URI), fallback when icon_url expires |
| `bundle_id` | string | ✅ | App bundle identifier |
| `versions` | array | ✅ | Version history (can be empty) |
| `versions[].version_id` | string | ✅ | External identifier (platform-specific version ID) |
| `versions[].version` | string | ✅ | Human-readable version string |
| `versions[].description` | string | ❌ | Notes about this specific version (e.g. notable features, jailbreak requirement) |
| `delisted` | boolean | ✅ | Whether the app has been removed from App Store |
| `added_at` | string | ✅ | ISO 8601 timestamp when archived |

## Contributing

1. Fork this repository
2. Add or update `data/{appId}.json`
3. Submit a Pull Request

ipaTool can auto-generate PRs from your local favorites via the "Publish" feature.
