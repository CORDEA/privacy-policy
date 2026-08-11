# Privacy policies

Public policies are organized by product so each app has a stable privacy-policy
URL even if its data practices change later.

```text
<product-slug>/
  index.md
policies/
  no-data.md
```

This repository is published at `https://cordea.jp/privacy-policy/`, so the
repository paths do not repeat the `privacy-policy` directory.

The root `index.md` defines the scope of the combined policy for all products
that currently have the same data practices. Each product page is the preferred
URL for an app-store listing.

The root and each product `index.md` contain only scope or page metadata. During
deployment, Pandoc combines them with the shared policy body in
`policies/no-data.md`. Edit the shared file once to update the content of the
combined policy and every current product policy.

## Current products

| Product | Source path |
| --- | --- |
| URL Dispatcher | `url-dispatcher/index.md` |
| Voice Clock | `voice-clock/index.md` |
| Kids Compass | `kids-compass/index.md` |
| Closet | `closet/index.md` |

All current products use the no-data-collection policy. If a product later adds
analytics or another data service, add another shared policy and map that
product to it in the deployment workflow. Keep its directory and public URL
unchanged.

The deployment workflow converts the root policy and every product policy to
HTML on the `pages` branch.
