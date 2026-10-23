# Thornbyte website: deployment guide for thornbyte.in

Files: index.html, robots.txt, sitemap.xml, 404.html, og-image.png, CNAME
Everything is already set to https://thornbyte.in. Do these steps once GoDaddy shows the domain as Active.

## 1. Upload to GitHub
Repo: beingvikasbhadu/thornbyte-website- . Upload ALL files to the repo root (replace the old index.html), commit.
Do this only when the domain is Active: the CNAME file makes GitHub Pages redirect the github.io address to thornbyte.in.

## 2. Turn on the custom domain
Repo > Settings > Pages > Custom domain: enter thornbyte.in > Save.

## 3. Add DNS records in GoDaddy
GoDaddy > Domain Portfolio > thornbyte.in > DNS. First DELETE the default parked "A" record for @ and any default "www" CNAME. Then add:
- A    @    185.199.108.153
- A    @    185.199.109.153
- A    @    185.199.110.153
- A    @    185.199.111.153
- CNAME  www  beingvikasbhadu.github.io
Save. DNS can take from a few minutes to a few hours.

## 4. Enable HTTPS
Back in Repo > Settings > Pages, wait for the DNS check to pass, then tick "Enforce HTTPS" (the certificate can take up to an hour).

## 5. Enquiry form
Open index.html and find FORM_ENDPOINT=''. Create a free form at web3forms.com or formspree.io, paste its URL there, commit.
While it is empty, the form opens a pre-filled WhatsApp chat to +91 7676309983 instead.

## 6. Get found on Google
- Add https://thornbyte.in in Google Search Console, verify, and submit https://thornbyte.in/sitemap.xml
- Create a Google Business Profile and a LinkedIn company page that link to the site.
- Test at pagespeed.web.dev and the social preview at opengraph.xyz.
