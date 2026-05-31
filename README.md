# Conklin Medical Centre Website

A self-contained static website. Ready to deploy on GitHub Pages.

## Files to upload
- index.html
- images/ (logo, pharmacy logo, and facility photos)
- .nojekyll
- README.md (optional, for your reference)

## Deploy on GitHub Pages
1. Create a new repository on GitHub.
2. Upload index.html and the images folder. Keep the folder named "images".
3. In the repo go to Settings, then Pages.
4. Under Build and deployment set Source to "Deploy from a branch", Branch to "main", folder "/ (root)", then Save.
5. The site goes live at https://USERNAME.github.io/REPONAME/ within a minute or two.
6. Optional custom domain: Settings, Pages, Custom domain, then point your DNS to GitHub.

## Registration form
The form sends submissions to info@conklinmedicalcentre.com using FormSubmit.
The first time the live form is submitted, FormSubmit emails that address a one-time
activation link. Click it once and submissions will arrive automatically after that.

## Notes before launch
- Two photos load from Pexels (free for commercial use): the family image in the
  registration section and the doctor image in the languages section. To host them
  yourself, download each, drop the files into images/, and update those two URLs in index.html.
- Address, phone, and map point to 360 Conklin Road, Unit A1, Brantford ON N3T 0N5.
- Confirm the clinic hours and email address shown in the footer before going live.

Website by revmedia (revmedia.ca)

## Custom domain: www.conklinmedicalcentre.com
A CNAME file is already included (contains www.conklinmedicalcentre.com), so GitHub Pages
will use the custom domain automatically once the repo is published.

Steps:
1. Publish the site on GitHub Pages (Settings, Pages, deploy from main at root).
2. In Settings, Pages, Custom domain: enter www.conklinmedicalcentre.com and Save.
3. At your DNS provider, add these records (values confirmed from GitHub Docs):

   www subdomain (primary):
     Type CNAME   Host www   Value USERNAME.github.io   (replace USERNAME with your GitHub account or org)

   Apex / root (conklinmedicalcentre.com) so the bare domain also works:
     Type A   Host @   Value 185.199.108.153
     Type A   Host @   Value 185.199.109.153
     Type A   Host @   Value 185.199.110.153
     Type A   Host @   Value 185.199.111.153
   Optional IPv6 (AAAA), Host @:
     2606:50c0:8000::153
     2606:50c0:8001::153
     2606:50c0:8002::153
     2606:50c0:8003::153

4. Wait for DNS to propagate (a few minutes up to 24 hours), then in Settings, Pages
   enable "Enforce HTTPS" once the certificate is issued.

Tip: add both www and the apex domain so the certificate covers both and the bare
domain redirects to www.
