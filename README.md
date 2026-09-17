# Alpha Insights — Final Front-End Prototype

This package represents the approved front-end direction for the production WordPress build.

## Portfolio backend requirements

1. **Manual ordering / priority** — every portfolio item has a display priority. Production WordPress should expose drag-and-drop ordering (plus Move Up / Move Down as a fallback), so newly improved work can be moved to the top without code changes.
2. **Platform taxonomy** — items can belong to Excel, Power BI, n8n / Automation, or future applications. New platform terms must be addable from WordPress. A project may belong to multiple platforms.
3. **Capability + industry filters** — projects can be tagged by capability (e.g. Working Capital, Cash Flow, FP&A, Valuation, Dashboards) and industry (e.g. SaaS, Multi-location Retail, F&B). Visitors can combine filters.
4. **Access status** — every item visibly states Interactive, Preview only, or Available on request.
5. **Media + model fields** — each item should accept homepage thumbnail, gallery screenshots, short description, business challenge, approach, business value, platform(s), capability tags, industry tags, access status, display priority, and OneDrive / Excel Online / Power BI embed URL.
6. **Future growth** — the same taxonomy can later support separate Excel, Power BI, n8n and other application sections without rebuilding the portfolio.

The current ZIP is a static prototype. The WordPress production build will implement these as editable admin fields/taxonomies rather than JavaScript data.

## Final refinements
- Added Alpha Insights favicon (`assets/favicon.svg`).
- About image now uses a different user-supplied portrait from the hero image.
- Added a free-text portfolio search box on the public site, so visitors are not limited to predefined dropdown terms.
- Production WordPress taxonomies (Platform, Capability, Industry) must allow selecting existing terms OR typing/creating a new term manually.
- Included `portfolio-admin-demo.html` to demonstrate where projects will be uploaded in production. The static prototype cannot persist uploads; production workflow will be **WordPress Admin → Portfolio → Add New**.


## Final admin refinements
- Platform, Capability and Industry are designed as growing multi-select tag libraries in production.
- Users can select an existing title or type a new title; new titles persist for future projects.
- Multiple tags can be assigned to one project (e.g. Excel + Power BI; Working Capital + Cash Flow + Forecasting).
- About section now uses the genuine IMG_1799 photograph, distinct from the hero image.
