# Buy a Car

The umbrella page for car-buying research on CompareThe＿ — facts and figures over reviews and opinions, a real price-vs-quality frontier instead of "it depends on your needs." One project lives here so far; more can land here as they happen (other countries, other vehicle types, whatever comes up next).

<style>
  .car-hub {
    --page:          #f4f5f3;
    --surface:       #ffffff;
    --ink:           #14171a;
    --ink-secondary: #4d5560;
    --muted:         #8b9099;
    --rule:          #dde1e4;
    --rule-strong:   #c7ccd1;
    --accent:        #2a78d6;
    --tag-bg:        #eef2f6;
    color-scheme: light;
  }
  @media (prefers-color-scheme: dark) {
    :root:where(:not([data-theme="light"])) .car-hub {
      --page:          #0f1113;
      --surface:       #17191c;
      --ink:           #f2f3f1;
      --ink-secondary: #b9bec4;
      --muted:         #82878e;
      --rule:          #2a2d31;
      --rule-strong:   #383c41;
      --accent:        #3987e5;
      --tag-bg:        #1d2b3a;
      color-scheme: dark;
    }
  }
  :root[data-theme="dark"] .car-hub {
    --page:          #0f1113;
    --surface:       #17191c;
    --ink:           #f2f3f1;
    --ink-secondary: #b9bec4;
    --muted:         #82878e;
    --rule:          #2a2d31;
    --rule-strong:   #383c41;
    --accent:        #3987e5;
    --tag-bg:        #1d2b3a;
    color-scheme: dark;
  }

  .car-hub {
    font-family: ui-sans-serif, system-ui, -apple-system, "Segoe UI", "Helvetica Neue", Arial, sans-serif;
    margin: 8px 0 28px;
  }
  .car-hub .eyebrow {
    font-size: 11px;
    font-weight: 700;
    letter-spacing: 0.06em;
    text-transform: uppercase;
    color: var(--accent);
    margin: 0 0 6px;
  }
  .car-hub .lede-card {
    display: block;
    background: var(--surface);
    border: 1px solid var(--rule);
    border-radius: 12px;
    padding: 22px 22px 20px;
    text-decoration: none;
    color: inherit;
    margin: 10px 0 24px;
  }
  .car-hub .lede-card:hover { border-color: var(--accent); }
  .car-hub .lede-card h3 {
    margin: 0 0 6px;
    font-size: 19px;
    font-weight: 700;
    color: var(--ink);
  }
  .car-hub .lede-card p {
    margin: 0;
    font-size: 14px;
    line-height: 1.55;
    color: var(--ink-secondary);
  }
  .car-hub .status-row {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
    margin-top: 14px;
  }
  .car-hub .pill {
    font-size: 11px;
    font-weight: 600;
    padding: 3px 10px;
    border-radius: 999px;
    background: var(--tag-bg);
    color: var(--accent);
  }
  .car-hub .grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(230px, 1fr));
    gap: 14px;
    margin: 10px 0 24px;
  }
  .car-hub .card {
    display: block;
    background: var(--surface);
    border: 1px solid var(--rule);
    border-radius: 10px;
    padding: 16px 16px 14px;
    text-decoration: none;
    color: inherit;
  }
  .car-hub .card:hover { border-color: var(--accent); }
  .car-hub .card .card-label {
    font-size: 10.5px;
    font-weight: 700;
    letter-spacing: 0.04em;
    text-transform: uppercase;
    color: var(--muted);
    margin: 0 0 6px;
  }
  .car-hub .card h4 {
    margin: 0 0 6px;
    font-size: 15px;
    font-weight: 700;
    color: var(--ink);
  }
  .car-hub .card p {
    margin: 0;
    font-size: 13px;
    line-height: 1.5;
    color: var(--ink-secondary);
  }
  .car-hub h2 {
    font-size: 13px;
    font-weight: 700;
    letter-spacing: 0.04em;
    text-transform: uppercase;
    color: var(--ink-secondary);
    margin: 28px 0 4px;
  }
</style>

<div class="car-hub">

<p class="eyebrow">Current project</p>

<a class="lede-card" href="../Buying%20an%20Electric%20Car%20in%20France%20(2026)/">
  <h3>Buying an Electric Car in France (2026) →</h3>
  <p>New or secondhand, open budget, no segment preference. Charts, a real secondhand-vs-new comparison, tax incentives, Euro NCAP safety data, and a running verdict on what to actually buy — for a budget short-range family runabout and a nicer everyday family car.</p>
  <div class="status-row">
    <span class="pill">in progress</span>
    <span class="pill">13 sub-pages</span>
    <span class="pill">5 interactive charts</span>
  </div>
</a>

<h2>Highlights from that project</h2>

<div class="grid">
  <a class="card" href="../Buying%20an%20Electric%20Car%20in%20France%20(2026)/10-budget-ev-shortlist-comparison.md">
    <p class="card-label">Comparison table</p>
    <h4>Budget/family EV shortlist</h4>
    <p>New + secondhand, price with and without incentive, safety, range, running costs — sorted cheapest first.</p>
  </a>
  <a class="card" href="../Buying%20an%20Electric%20Car%20in%20France%20(2026)/07-reading-a-real-listing.md">
    <p class="card-label">Case study</p>
    <h4>Reading a real listing</h4>
    <p>Model Y vs. Model 3 secondhand, plus an actual LeBonCoin ad priced against the research.</p>
  </a>
  <a class="card" href="../Buying%20an%20Electric%20Car%20in%20France%20(2026)/09-ev-vs-ice-total-cost.md">
    <p class="card-label">Analysis</p>
    <h4>Is EV actually better value than petrol?</h4>
    <p>Purchase price and depreciation folded in with running costs, not just running costs alone.</p>
  </a>
  <a class="card" href="../Buying%20an%20Electric%20Car%20in%20France%20(2026)/04-secondhand-market-survey.md">
    <p class="card-label">Research</p>
    <h4>Secondhand market + safety survey</h4>
    <p>Real used-listing price bands and Euro NCAP ratings — the safety data alone reshuffled the shortlist twice.</p>
  </a>
</div>

<h2>What's next</h2>

<p style="font-size:14px; color:var(--ink-secondary); line-height:1.55;">A real weighted price-vs-quality frontier (not just range/mileage as a stand-in), and a final purchase decision — tracked in <a href="../Buying%20an%20Electric%20Car%20in%20France%20(2026)/plan.md">the project's plan.md</a>. More car-buying research lands here as it happens.</p>

</div>
