# photos-media

Image bytes and manifest shards for [marcusklaas.nl/photos](https://marcusklaas.nl/photos).
Written by the upload page, not by hand.

**No code lives here, deliberately.** The upload token is scoped to this
repository only, so a leaked token cannot modify the site's JavaScript — and this
history can be flattened and force-pushed without endangering anything.

```
index.json                # shard table
m/0000.json 0001.json …   # 100 photos each, oldest-first; only the last is mutated
p/<id>-400.avif  <id>-800.avif  <id>-1600.avif
```

To remove a photo, see `scripts/delete.mjs` in the app repo.
