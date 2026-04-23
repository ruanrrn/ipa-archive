# ipa-archive

Community-driven archive for delisted iOS apps, powered by ipaTool.

## Structure

```
apps/
  delisted/
    1137819437.json          # Per-app detail
indexes/
  delisted-lite.json         # List index for fast loading
assets/
  icons/
    11/
      1137819437.png         # App icon (first 2 digits of app ID as subfolder)
```

## Schema

### delisted-lite.json (index)

Flat array for list views:

```json
[
  {
    "id": "1137819437",
    "name": "iFreeTime",
    "bundle_id": "one.icc.iFreeTime",
    "artist_name": "婵婵 黄",
    "icon_asset": "assets/icons/11/1137819437.png",
    "latest_version": "6.8.5",
    "updated_at": "2026-04-23T10:20:00Z"
  }
]
```

### apps/delisted/{id}.json (detail)

```json
{
  "id": "1137819437",
  "name": "iFreeTime",
  "bundle_id": "one.icc.iFreeTime",
  "artist_name": "婵婵 黄",
  "icon_asset": "assets/icons/11/1137819437.png",
  "icon_url": "",
  "delisted": true,
  "notes": [
    "商店已不可检索",
    "由 ipatool 从本地 IPA 补全版本信息"
  ],
  "versions": [
    {
      "version_id": "",
      "version": "6.8.5",
      "released_at": "",
      "size_bytes": 27092783,
      "description": ""
    }
  ],
  "updated_at": "2026-04-23T10:20:00Z"
}
```

## Contributing

Use [ipaTool](https://github.com/ruanrrn/ipatool) to prepare and submit contributions via PR.

## License

CC0-1.0
