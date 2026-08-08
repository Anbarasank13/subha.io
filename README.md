# Meal Ledger

A single-page tool for building a monthly meal ledger by date range and exporting it as a PDF, matching a mess/canteen chit format (To / Month / Meal rate header, daily Breakfast-Dinner-Total-Amount table, Total, Old balance, Final total).

No build step, no dependencies to install — it's one static HTML file.

## Host it on GitHub Pages

1. Create a new GitHub repository (public).
2. Upload `index.html` from this folder to the root of the repo (drag-and-drop on the GitHub web UI works, or `git add`/`commit`/`push`).
3. In the repo, go to **Settings → Pages**.
4. Under **Build and deployment → Source**, choose **Deploy from a branch**.
5. Pick the branch (usually `main`) and folder `/ (root)`, then **Save**.
6. GitHub gives you a live URL shortly after, in the form:
   `https://<your-username>.github.io/<repo-name>/`

Because the file is named `index.html`, it loads automatically at that root URL — no extra path needed.

## Notes

- Works fully client-side: everything (the form, table, and PDF generation) runs in the visitor's browser. No server or database involved, and no data leaves the device.
- The PDF export uses jsPDF and jsPDF-AutoTable, loaded from a CDN, so the page needs an internet connection the first time it loads (and whenever it saves a PDF).
- Tested for mobile: inputs are sized to avoid iOS auto-zoom, buttons are tap-friendly (44px+), and the ledger table scrolls horizontally on narrow screens instead of squeezing.
- To use a custom domain instead of the github.io URL, add a `CNAME` file at the repo root with your domain, and point your DNS at GitHub Pages per [GitHub's custom domain docs](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site).
