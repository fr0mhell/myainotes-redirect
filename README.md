# myainotes-redirect

Redirects the old site host `myainotes.linked-robot.com` to `https://minutify.app`, keeping the path.

- `index.html`, `privacy/`, `terms/`, `support/`, `delete-account/`: real pages, so they answer HTTP 200. A script sends the browser to the same path on `minutify.app`; without JavaScript a meta refresh goes to that exact page.
- `404.html`: GitHub Pages serves it for every other path (HTTP 404). The same script keeps the path; without JavaScript a link and a 5 s refresh go to the home page.

Runbook: `website/README.md` in fr0mhell/my-ai-notes, section "Old host redirect". Keep this running until at least 2027-10-05 and while any live app build opens the old URLs.
