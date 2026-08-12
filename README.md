# funnel-assets

Static assets for Funnelish funnels, served via jsDelivr.

    https://cdn.jsdelivr.net/gh/arcbites-cyber/funnel-assets@<sha>/<brand>-<market>/<slot>/<file>

**Always pin a commit SHA. Never use `@main`.** jsDelivr caches per URL and its
purge endpoint is unreliable, so `@main` can serve a stale file indefinitely.
Pinning also makes URLs immutable, so pushing new work here can never mutate a
funnel that is already live.

Images are WebP q82. Funnelish's own CDN transforms on the fly
(`?auto=webp&width=N`); jsDelivr does not, so anything committed here must
already be web-sized. q82 was visually indistinguishable from the PNG masters at
2x zoom and cut 6.2 MB to 458 KB.

## Layout

    <brand>-<market>/<slot>/   one folder per funnel page (adv, lander)
    shared/                    cross-funnel assets (payment chips, badges)
