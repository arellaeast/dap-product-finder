# DAP Product Finder (Concept Demo)

A guided product finder styled to fit the DAP brand: three questions (project, paint, joint size) lead to the right DAP sealant, with honest warnings when the popular pick is wrong for the job.

**Live demo:** https://arellaeast.github.io/dap-product-finder/

Part of a three-piece demo suite by Jacob East:
- Product Finder: https://arellaeast.github.io/dap-product-finder/
- Ask a DAP Expert: https://arellaeast.github.io/dap-ask-an-expert/
- Sealant Calculator: https://arellaeast.github.io/dap-sealant-calculator/

## The point of this demo

Research for a Website Manager application at DAP Global found:

- DAP's old Caulk + Sealant Selector survives only on the legacy cms.dap.com site, while GE Sealants runs its finder on its homepage
- The dominant 1-star review theme is the wrong product used in the wrong place, and DAP's replies point back to label fine print after the failure
- The clearest case: the Alex Plus page promotes kitchen and bath use while its own FAQ says not to use it in a shower

So the finder's star path is Shower & Tub. It recommends Silicone Max and shows a "Not Alex Plus" warning sourced from DAP's own FAQ. Stopping a bad buy beats answering a bad review.

## Rules

Decision rules live in `logic.js` as a pure function (`recommend(answers)`) so they can be unit tested and, in production, generated from PIM product data instead of hard-coded. Every claim traces to DAP published material: the Alex Plus FAQ (shower answer, 30-minute paint time, 1/2" x 1/2" max joint, backer rod), DAP retailer replies (butt joint and underwater exclusions), and each line's stated use.

## Run it locally

No build step. Open `index.html` in a browser, or serve the folder with `python3 -m http.server`.

## Disclaimer

Independent concept prototype. Not an official DAP product, and not affiliated with or endorsed by DAP Products Inc. or RPM International. Always check the label and technical data sheet for your specific job.
