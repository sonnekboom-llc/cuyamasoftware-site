# cuyamasoftware.com

Static company page for Cuyama Software, served as a DigitalOcean App Platform static site.
No build step, forms, cookies or tracking.

The app clones this repository by URL, so pushing to `main` does not deploy. After pushing a
change to the site, start a deployment manually:

```sh
doctl apps create-deployment "$(doctl apps list --format ID,Spec.Name --no-header | awk '$2=="cuyamasoftware-site"{print $1}')" --wait
```
