# Buying an Electric Car in France (2026)

<style>
  .ev-chart {
    --page:          #f4f5f3;
    --surface:       #ffffff;
    --ink:           #14171a;
    --ink-secondary: #4d5560;
    --muted:         #8b9099;
    --rule:          #dde1e4;
    --rule-strong:   #c7ccd1;
    --accent:        #2a78d6;
    --s-budget:      #2a78d6;
    --s-main:        #eb6834;
    --s-premium:     #1baf7a;
    --t-base:        #2a78d6;
    --t-lr:          #eb6834;
    --t-perf:        #b23a55;
    --series-1:      #2a78d6;
    --series-2:      #eb6834;
    --series-3:      #1baf7a;
    --frontier:      #14171a;
    --tag-bg:        #eef2f6;
    --open-hatch:    #c7ccd1;
    color-scheme: light;
  }
  @media (prefers-color-scheme: dark) {
    :root:where(:not([data-theme="light"])) .ev-chart {
      --page:          #0f1113;
      --surface:       #17191c;
      --ink:           #f2f3f1;
      --ink-secondary: #b9bec4;
      --muted:         #82878e;
      --rule:          #2a2d31;
      --rule-strong:   #383c41;
      --accent:        #3987e5;
      --s-budget:      #3987e5;
      --s-main:        #d95926;
      --s-premium:     #199e70;
      --t-base:        #3987e5;
      --t-lr:          #d95926;
      --t-perf:        #d95b76;
      --series-1:      #3987e5;
      --series-2:      #d95926;
      --series-3:      #199e70;
      --frontier:      #f2f3f1;
      --tag-bg:        #1d2b3a;
      --open-hatch:    #383c41;
      color-scheme: dark;
    }
  }
  :root[data-theme="dark"] .ev-chart {
    --page:          #0f1113;
    --surface:       #17191c;
    --ink:           #f2f3f1;
    --ink-secondary: #b9bec4;
    --muted:         #82878e;
    --rule:          #2a2d31;
    --rule-strong:   #383c41;
    --accent:        #3987e5;
    --s-budget:      #3987e5;
    --s-main:        #d95926;
    --s-premium:     #199e70;
    --t-base:        #3987e5;
    --t-lr:          #d95926;
    --t-perf:        #d95b76;
    --series-1:      #3987e5;
    --series-2:      #d95926;
    --series-3:      #199e70;
    --frontier:      #f2f3f1;
    --tag-bg:        #1d2b3a;
    --open-hatch:    #383c41;
    color-scheme: dark;
  }

  .ev-chart {
    background: var(--page);
    color: var(--ink);
    font-family: ui-sans-serif, system-ui, -apple-system, "Segoe UI", "Helvetica Neue", Arial, sans-serif;
    line-height: 1.5;
    margin: 24px 0;
    padding: 20px;
    border-radius: 12px;
  }
  .ev-chart .card {
    background: var(--surface);
    border: 1px solid var(--rule);
    border-radius: 10px;
    padding: 20px 18px 16px;
  }
  .ev-chart .card + .card { margin-top: 16px; }
  .ev-chart .card h3 {
    font-size: 13px;
    font-weight: 600;
    letter-spacing: 0.03em;
    text-transform: uppercase;
    color: var(--ink-secondary);
    margin: 0 0 4px;
  }
  .ev-chart .card .sub {
    font-size: 12.5px;
    color: var(--muted);
    margin: 0 0 16px;
  }
  .ev-chart .chart-scroll { overflow-x: auto; }
  .ev-chart svg.chart { width: 100%; min-width: 620px; height: auto; display: block; overflow: visible; }
  .ev-chart .axis-label { fill: var(--muted); font-size: 11px; font-variant-numeric: tabular-nums; }
  .ev-chart .axis-title { fill: var(--ink-secondary); font-size: 12px; font-weight: 600; }
  .ev-chart .row-label { fill: var(--ink); font-size: 12px; }
  .ev-chart .row-sub { fill: var(--muted); font-size: 10.5px; }
  .ev-chart .section-label { fill: var(--ink-secondary); font-size: 11px; font-weight: 700; letter-spacing: 0.04em; text-transform: uppercase; }
  .ev-chart .gridline { stroke: var(--rule); stroke-width: 1; }
  .ev-chart .baseline { stroke: var(--rule-strong); stroke-width: 1; }
  .ev-chart .grouprule { stroke: var(--rule); stroke-width: 1; stroke-dasharray: 2 3; }
  .ev-chart .frontier-line { stroke: var(--frontier); stroke-width: 1.5; stroke-dasharray: 3 4; fill: none; opacity: 0.55; }
  .ev-chart .zone-label { fill: var(--muted); font-size: 10.5px; font-style: italic; }

  .ev-chart .pt { cursor: pointer; }
  .ev-chart .pt circle.mainmark { stroke-width: 2; transition: r 0.12s ease; }
  .ev-chart .pt:hover circle.mainmark, .ev-chart .pt:focus circle.mainmark { r: 8.5; }
  .ev-chart .pt:focus { outline: none; }
  .ev-chart .pt .ptlabel { font-size: 11px; font-weight: 600; fill: var(--ink-secondary); pointer-events: none; }
  .ev-chart .pt .ring { fill: var(--surface); }
  .ev-chart .pt .mark { transition: transform 0.12s ease; transform-origin: center; transform-box: fill-box; }
  .ev-chart .pt:hover .mark, .ev-chart .pt:focus .mark { transform: scale(1.25); }
  .ev-chart .pt.frontier .mark { stroke: var(--frontier); stroke-width: 1.5; }
  .ev-chart .pt-year { font-size: 9.5px; font-weight: 600; fill: var(--ink-secondary); pointer-events: none; font-variant-numeric: tabular-nums; }

  .ev-chart .bar { cursor: pointer; }
  .ev-chart .bar rect.range { transition: opacity 0.12s ease, filter 0.12s ease; }
  .ev-chart .bar:hover rect.range, .ev-chart .bar:focus rect.range { filter: brightness(1.08); }
  .ev-chart .bar:focus { outline: none; }
  .ev-chart .bar-label { font-size: 10.5px; font-weight: 600; fill: var(--ink-secondary); font-variant-numeric: tabular-nums; pointer-events: none; }

  .ev-chart .tooltip {
    position: absolute;
    pointer-events: none;
    background: var(--ink);
    color: var(--page);
    font-size: 12.5px;
    line-height: 1.45;
    padding: 8px 11px;
    border-radius: 6px;
    box-shadow: 0 6px 20px rgba(0,0,0,0.18);
    opacity: 0;
    transform: translate(-50%, calc(-100% - 12px));
    transition: opacity 0.1s ease;
    white-space: nowrap;
    z-index: 5;
  }
  .ev-chart .tooltip.show { opacity: 1; }
  .ev-chart .tooltip .t-name { font-weight: 700; margin-bottom: 2px; }
  .ev-chart .tooltip .t-flag { color: var(--muted); font-size: 11px; }

  .ev-chart .legend { display: flex; flex-wrap: wrap; gap: 18px; margin: 14px 2px 4px; font-size: 12.5px; color: var(--ink-secondary); }
  .ev-chart .legend .grp { display: flex; align-items: center; gap: 14px; }
  .ev-chart .legend .item { display: flex; align-items: center; gap: 6px; }
  .ev-chart .swatch { width: 10px; height: 10px; border-radius: 50%; display: inline-block; }
  .ev-chart .swatch.square { border-radius: 3px; }
  .ev-chart .swatch.hollow { background: transparent; border: 2px solid var(--muted); box-sizing: border-box; }
  .ev-chart .swatch.filled { border: 2px solid; }
  .ev-chart .swatch.hatched { background-image: repeating-linear-gradient(135deg, var(--open-hatch), var(--open-hatch) 2px, transparent 2px, transparent 4px); border: 1px solid var(--rule-strong); }
  .ev-chart .shape-key { width: 12px; height: 12px; display: inline-flex; align-items: center; justify-content: center; }
  .ev-chart .divider-v { width: 1px; align-self: stretch; background: var(--rule); }

  .ev-chart details.data-table { margin-top: 16px; }
  .ev-chart details.data-table summary {
    cursor: pointer;
    font-size: 12.5px;
    font-weight: 600;
    color: var(--accent);
    padding: 4px 0;
  }
  .ev-chart table { width: 100%; border-collapse: collapse; font-family: ui-monospace, "SF Mono", "Cascadia Mono", "Roboto Mono", monospace; font-size: 12.5px; margin-top: 8px; }
  .ev-chart th { text-align: left; font-family: ui-sans-serif, system-ui, sans-serif; font-size: 11px; font-weight: 600; text-transform: uppercase; letter-spacing: 0.04em; color: var(--muted); padding: 8px 10px; border-bottom: 1px solid var(--rule-strong); }
  .ev-chart td { padding: 7px 10px; border-bottom: 1px solid var(--rule); font-variant-numeric: tabular-nums; color: var(--ink); white-space: nowrap; }
  .ev-chart td.model { font-family: ui-sans-serif, system-ui, sans-serif; font-weight: 600; }
  .ev-chart td.num { text-align: right; }
  .ev-chart .seg-dot { width: 8px; height: 8px; border-radius: 50%; display: inline-block; margin-right: 7px; }
  .ev-chart .flag { font-size: 10.5px; padding: 1px 6px; border-radius: 999px; font-family: ui-sans-serif, system-ui, sans-serif; font-weight: 600; }
  .ev-chart .flag.confirmed { background: var(--tag-bg); color: var(--accent); }
  .ev-chart .flag.estimated, .ev-chart .flag.thin { color: var(--muted); border: 1px solid var(--rule-strong); }
  .ev-chart .flag.frontier-flag { background: var(--tag-bg); color: var(--accent); }
  .ev-chart .table-scroll { overflow-x: auto; }
</style>

I'm in the market for an electric car in France — new or secondhand, open budget, no segment preference. Rather than wade through spammy SEO listicles and manufacturer marketing, I'm doing this the CompareThe＿ way: facts and figures, sourced, with a real price-vs-quality efficient frontier instead of "it depends on your needs."

## So what should I actually buy?

Here's the honest current read, based on the research below. It's not a final decision — the weighted frontier (charging speed, safety, boot space, brand reliability, not just range/mileage) and a deeper pass on individual used listings still need to happen — but two clear leading options have emerged, for two different priorities:

**Optimizing for lowest total cost:** a new **Renault Twingo E-Tech** (€19,990) or **Peugeot e-208** (€21,950). Both are eligible for the bonus écologique (up to €5,700 off for lower-income households, more with the EU-battery surbonus), and the e-208 in particular holds its resale value unusually well — around 62% after 3 years, better than its petrol equivalent — so buying new barely costs more than buying "used," and you skip the used-car uncertainty entirely.

**Optimizing for range and charging speed at a reasonable price:** a **secondhand Tesla Model 3**, specifically a base Propulsion/SR+ trim from around 2021-2022 with 50-90,000km on the clock — roughly €19,000-25,000. That lands inside the price band of several *new* mainstream cars while very likely beating them on real-world range and charging network, which is the strongest argument in this research so far for going used rather than new. The caveat: trim matters enormously here — a Grande Autonomie or Performance Model 3 is a meaningfully different (and pricier) car, so this only holds for the base trim specifically.

Both are genuine shortlist candidates, not a final answer — see [what's still open](plan.md).

## Price vs. range: the new-car market

Range (WLTP) stands in for "quality" here because it's the one spec reported consistently across the market — not a weighted score. Price is the new sticker price, before incentives, depreciation or running costs. Twenty-two trims, city car to premium SUV. The Twingo E-Tech, e-208 and Tesla Model 3 are the three flagged as an early shortlist — cheap-and-decent-range, mid-price-and-strong-range, and expensive-but-dominant-range respectively.

<div class="ev-chart" id="embed-new">
  <div class="card">
    <h3>Price vs. range</h3>
    <p class="sub">€16.9k–€65k · 220–701km WLTP · bubble labels mark the three shortlisted models</p>
    <div class="chart-scroll">
      <svg class="chart" id="chart-new" viewBox="0 0 900 540" role="img" aria-label="Scatter plot of starting price against WLTP range for 22 electric vehicles sold in France, coloured by price segment"></svg>
    </div>
    <div class="legend">
      <div class="grp">
        <span class="item"><span class="swatch filled" style="border-color:var(--s-budget)"></span>Budget / city (&lt;€25k)</span>
        <span class="item"><span class="swatch filled" style="border-color:var(--s-main)"></span>Mainstream (€25–40k)</span>
        <span class="item"><span class="swatch filled" style="border-color:var(--s-premium)"></span>Premium (€40k+)</span>
      </div>
      <div class="divider-v"></div>
      <div class="grp">
        <span class="item"><span class="swatch filled" style="border-color:var(--muted)"></span>Sourced</span>
        <span class="item"><span class="swatch hollow"></span>Estimated</span>
      </div>
    </div>
    <details class="data-table">
      <summary>Show full data (22 rows) ▾</summary>
      <div class="table-scroll"><table id="table-new"></table></div>
    </details>
  </div>
</div>

<script>
(function () {
  var root = document.getElementById("embed-new");
  var data = [
    { name: "Dacia Spring",        price: 16900, range: 220, seg: "budget",  priceOk: true,  rangeOk: false },
    { name: "Leapmotor T03",       price: 17900, range: 265, seg: "budget",  priceOk: true,  rangeOk: false },
    { name: "BYD Dolphin Surf (Active)", price: 19990, range: 220, seg: "budget", priceOk: true, rangeOk: true },
    { name: "BYD Dolphin Surf (Boost)",  price: 24490, range: 322, seg: "budget", priceOk: true, rangeOk: true },
    { name: "Renault Twingo E-Tech", price: 19990, range: 263, seg: "budget", priceOk: true, rangeOk: true, shortlist: true },
    { name: "Citroën ë-C3",        price: 23300, range: 320, seg: "budget",  priceOk: true,  rangeOk: true },
    { name: "Fiat 500e",           price: 23900, range: 320, seg: "budget",  priceOk: true,  rangeOk: true },
    { name: "Peugeot e-208",       price: 21950, range: 433, seg: "budget",  priceOk: true,  rangeOk: true, shortlist: true },
    { name: "Renault 5 E-Tech",    price: 24000, range: 400, seg: "budget",  priceOk: true,  rangeOk: true },
    { name: "BYD Dolphin",         price: 27990, range: 340, seg: "main",    priceOk: true,  rangeOk: true },
    { name: "MG4 Standard",        price: 29990, range: 350, seg: "main",    priceOk: true,  rangeOk: true },
    { name: "Mini Cooper Electric",price: 33000, range: 402, seg: "main",    priceOk: false, rangeOk: true },
    { name: "BYD Atto 3",          price: 33990, range: 420, seg: "main",    priceOk: true,  rangeOk: true },
    { name: "Renault Megane E-Tech",price:35200, range: 450, seg: "main",    priceOk: true,  rangeOk: false },
    { name: "Kia EV3 (Air)",             price: 35990, range: 436, seg: "main",    priceOk: true, rangeOk: true },
    { name: "Kia EV3 (Earth Long Range)",price: 44990, range: 571, seg: "premium", priceOk: true, rangeOk: true },
    { name: "Hyundai Ioniq 5",     price: 42000, range: 570, seg: "premium", priceOk: false, rangeOk: false },
    { name: "Tesla Model 3",       price: 42990, range: 629, seg: "premium", priceOk: true,  rangeOk: true, shortlist: true },
    { name: "Tesla Model Y",       price: 45000, range: 550, seg: "premium", priceOk: false, rangeOk: true },
    { name: "Peugeot E-3008",      price: 45000, range: 701, seg: "premium", priceOk: false, rangeOk: true },
    { name: "Kia EV6",             price: 48000, range: 490, seg: "premium", priceOk: false, rangeOk: false },
    { name: "BMW iX3 (Neue Klasse)",price:65000, range: 685, seg: "premium", priceOk: false, rangeOk: true }
  ];
  var segMeta = {
    budget:  { label: "Budget / city",  varName: "--s-budget" },
    main:    { label: "Mainstream",     varName: "--s-main" },
    premium: { label: "Premium",        varName: "--s-premium" }
  };
  var svgNS = "http://www.w3.org/2000/svg";
  var svg = document.getElementById("chart-new");
  var cs = getComputedStyle(root);
  var W = 900, H = 540, ML = 66, MR = 24, MT = 20, MB = 56;
  var plotW = W - ML - MR, plotH = H - MT - MB;
  var xMin = 15000, xMax = 68000, yMin = 180, yMax = 730;
  function xPix(p) { return ML + (p - xMin) / (xMax - xMin) * plotW; }
  function yPix(r) { return MT + (yMax - r) / (yMax - yMin) * plotH; }
  function el(tag, attrs) {
    var e = document.createElementNS(svgNS, tag);
    for (var k in attrs) e.setAttribute(k, attrs[k]);
    return e;
  }
  var xTicks = [20000, 30000, 40000, 50000, 60000];
  xTicks.forEach(function (v) {
    var x = xPix(v);
    svg.appendChild(el("line", { class: "gridline", x1: x, x2: x, y1: MT, y2: MT + plotH }));
    var t = el("text", { class: "axis-label", x: x, y: MT + plotH + 20, "text-anchor": "middle" });
    t.textContent = "€" + (v / 1000) + "k";
    svg.appendChild(t);
  });
  var yTicks = [200, 300, 400, 500, 600, 700];
  yTicks.forEach(function (v) {
    var y = yPix(v);
    svg.appendChild(el("line", { class: "gridline", x1: ML, x2: ML + plotW, y1: y, y2: y }));
    var t = el("text", { class: "axis-label", x: ML - 10, y: y + 4, "text-anchor": "end" });
    t.textContent = v;
    svg.appendChild(t);
  });
  svg.appendChild(el("line", { class: "baseline", x1: ML, x2: ML + plotW, y1: MT + plotH, y2: MT + plotH }));
  svg.appendChild(el("line", { class: "baseline", x1: ML, x2: ML, y1: MT, y2: MT + plotH }));
  var xTitle = el("text", { class: "axis-title", x: ML + plotW / 2, y: H - 8, "text-anchor": "middle" });
  xTitle.textContent = "Starting price, new (€)";
  svg.appendChild(xTitle);
  var yTitle = el("text", { class: "axis-title", x: 0, y: 0, "text-anchor": "middle", transform: "translate(18," + (MT + plotH / 2) + ") rotate(-90)" });
  yTitle.textContent = "WLTP range (km)";
  svg.appendChild(yTitle);
  var tooltip = document.createElement("div");
  tooltip.className = "tooltip";
  var chartCard = svg.closest(".card");
  chartCard.style.position = "relative";
  chartCard.appendChild(tooltip);
  data.forEach(function (d) {
    var color = cs.getPropertyValue(segMeta[d.seg].varName).trim();
    var g = el("g", { class: "pt", tabindex: "0" });
    var estimated = !(d.priceOk && d.rangeOk);
    var circle = el("circle", {
      class: "mainmark",
      cx: xPix(d.price), cy: yPix(d.range), r: 6.5,
      fill: estimated ? "transparent" : color,
      stroke: color
    });
    g.appendChild(circle);
    if (d.shortlist) {
      var label = el("text", { class: "ptlabel", x: xPix(d.price) + 10, y: yPix(d.range) - 10 });
      label.textContent = d.name;
      g.appendChild(label);
    }
    function show() {
      var flagText = estimated
        ? (!d.priceOk && !d.rangeOk ? "price & range estimated" : (!d.priceOk ? "price estimated" : "range estimated"))
        : "sourced";
      tooltip.innerHTML = '<div class="t-name">' + d.name + '</div>' +
        '€' + d.price.toLocaleString('en-GB') + ' &middot; ' + d.range + 'km WLTP' +
        '<div class="t-flag">' + segMeta[d.seg].label + ' &middot; ' + flagText + '</div>';
      var r = circle.getBoundingClientRect();
      var cardR = chartCard.getBoundingClientRect();
      tooltip.style.left = (r.left - cardR.left + r.width / 2) + "px";
      tooltip.style.top = (r.top - cardR.top) + "px";
      tooltip.classList.add("show");
    }
    function hide() { tooltip.classList.remove("show"); }
    g.addEventListener("mouseenter", show);
    g.addEventListener("mouseleave", hide);
    g.addEventListener("focus", show);
    g.addEventListener("blur", hide);
    svg.appendChild(g);
  });
  var order = { budget: 0, main: 1, premium: 2 };
  var sorted = data.slice().sort(function (a, b) { return order[a.seg] - order[b.seg] || a.price - b.price; });
  var table = document.getElementById("table-new");
  var thead = el("thead", {});
  var headRow = document.createElement("tr");
  ["Model", "Segment", "Price", "Range (km)", "Confidence"].forEach(function (h) {
    var th = document.createElement("th");
    th.textContent = h;
    headRow.appendChild(th);
  });
  thead.appendChild(headRow);
  table.appendChild(thead);
  var tbody = document.createElement("tbody");
  sorted.forEach(function (d) {
    var color = cs.getPropertyValue(segMeta[d.seg].varName).trim();
    var tr = document.createElement("tr");
    var estimated = !(d.priceOk && d.rangeOk);
    var tdModel = document.createElement("td");
    tdModel.className = "model";
    tdModel.textContent = d.name + (d.shortlist ? " ★" : "");
    tr.appendChild(tdModel);
    var tdSeg = document.createElement("td");
    tdSeg.innerHTML = '<span class="seg-dot" style="background:' + color + '"></span>' + segMeta[d.seg].label;
    tr.appendChild(tdSeg);
    var tdPrice = document.createElement("td");
    tdPrice.className = "num";
    tdPrice.textContent = "€" + d.price.toLocaleString('en-GB') + (d.priceOk ? "" : "*");
    tr.appendChild(tdPrice);
    var tdRange = document.createElement("td");
    tdRange.className = "num";
    tdRange.textContent = d.range + (d.rangeOk ? "" : "*");
    tr.appendChild(tdRange);
    var tdFlag = document.createElement("td");
    var flag = document.createElement("span");
    flag.className = "flag " + (estimated ? "estimated" : "confirmed");
    flag.textContent = estimated ? "estimated" : "sourced";
    tdFlag.appendChild(flag);
    tr.appendChild(tdFlag);
    tbody.appendChild(tr);
  });
  table.appendChild(tbody);
})();
</script>

One thing worth knowing if you're reading other sources on this: two entries above (Kia EV3, BYD Dolphin Surf) originally got plotted wrong, pairing one trim's price with a different trim's range — a "from €X, up to Ykm" marketing-copy trap. Full detail, running costs, and depreciation trends are in the [model & TCO survey](02-model-tco-survey.md).

## What that money actually gets you over time

Sticker price is the least important number here. Average depreciation is 50-60% over 3 years for EVs (vs. 30-40% for petrol) — battery health is the single biggest driver of resale value, and budget/city EVs tend to hold value best. Running costs are also lower than petrol (~€4,300/yr vs ~€5,250/yr combined maintenance, insurance and charging), *except* insurance, which now costs more for EVs since a tax exemption ended in 2025. Full breakdown, sourcing, and the trim-mismatch correction mentioned above: [02-model-tco-survey.md](02-model-tco-survey.md).

And before any of that: tax incentives can take €3,500-7,700 off a new EV under €47,000, or get you a lease under €200/month if you qualify for leasing social — worth checking before ruling new cars out on price alone. Detail: [01-tax-incentives.md](01-tax-incentives.md).

## The secondhand market — and why trim matters more than nameplate

This is where the Tesla Model 3 recommendation above comes from. A "used Tesla Model 3" isn't one market — Propulsion/SR+, Grande Autonomie, and Performance are different battery packs, different range, different drivetrain, and price bands that barely overlap. A 2022 Performance Model 3 can cost *more* used than a 2023 base Propulsion, despite being a year older — because it's a genuinely different car, not just an older one.

<div class="ev-chart" id="embed-used">
  <div class="card">
    <h3>Tesla Model 3 &amp; Model Y — price by trim &amp; year</h3>
    <p class="sub">Used listing price bands, France 2026 · grouped by trim tier, sorted oldest to newest within each</p>
    <div class="chart-scroll">
      <svg class="chart" id="chart-tesla-used" role="img" aria-label="Horizontal range-bar chart of used Tesla Model 3 and Model Y price bands by trim tier and year"></svg>
    </div>
    <div class="legend">
      <div class="grp">
        <span class="item"><span class="swatch square" style="background:var(--t-base)"></span>Propulsion / SR+</span>
        <span class="item"><span class="swatch square" style="background:var(--t-lr)"></span>Grande Autonomie / Long Range</span>
        <span class="item"><span class="swatch square" style="background:var(--t-perf)"></span>Performance</span>
      </div>
    </div>
  </div>
  <div class="card">
    <h3>Other used candidates surveyed</h3>
    <p class="sub">Aggregate price ranges (not trim-broken-out) · coloured by the same price segment used in the new-car chart</p>
    <div class="chart-scroll">
      <svg class="chart" id="chart-other-used" role="img" aria-label="Horizontal range-bar chart of price ranges for other used EV candidates"></svg>
    </div>
    <div class="legend">
      <div class="grp">
        <span class="item"><span class="swatch square" style="background:var(--s-budget)"></span>Budget / city</span>
        <span class="item"><span class="swatch square" style="background:var(--s-main)"></span>Mainstream</span>
      </div>
      <div class="divider-v"></div>
      <div class="grp">
        <span class="item"><span class="swatch hatched"></span>Only one bound confirmed / thin data</span>
      </div>
    </div>
    <details class="data-table">
      <summary>Show full data (19 rows) ▾</summary>
      <div class="table-scroll"><table id="table-used"></table></div>
    </details>
  </div>
</div>

<script>
(function () {
  var root = document.getElementById("embed-used");
  var teslaData = [
    { model: "Model 3", trim: "Propulsion / SR+", tier: "base", year: "2019",       mileage: "100-150k km", lo: 13000, hi: 17000, bothBounds: true },
    { model: "Model 3", trim: "Propulsion / SR+", tier: "base", year: "2020",       mileage: "70-120k km",  lo: 16000, hi: 21000, bothBounds: true },
    { model: "Model 3", trim: "Propulsion / SR+", tier: "base", year: "2021",       mileage: "50-90k km",   lo: 19000, hi: 25000, bothBounds: true },
    { model: "Model 3", trim: "Propulsion / SR+", tier: "base", year: "2022",       mileage: "30-70k km",   lo: 22000, hi: 28000, bothBounds: true },
    { model: "Model 3", trim: "Propulsion / SR+", tier: "base", year: "2023",       mileage: "20-50k km",   lo: 26000, hi: 32000, bothBounds: true },
    { model: "Model 3", trim: "Propulsion / SR+ (Highland facelift)", tier: "base", year: "2024", mileage: "<30k km", lo: 28000, hi: 35000, bothBounds: true },
    { model: "Model 3", trim: "Grande Autonomie", tier: "lr", year: "2019-2020",    mileage: "80-130k km",  lo: 18000, hi: 25000, bothBounds: true },
    { model: "Model 3", trim: "Grande Autonomie", tier: "lr", year: "2021",         mileage: "50-90k km",   lo: 24000, hi: 30000, bothBounds: true },
    { model: "Model 3", trim: "Grande Autonomie", tier: "lr", year: "2022-2023",    mileage: "20-60k km",   lo: 27000, hi: 36000, bothBounds: true },
    { model: "Model 3", trim: "Performance",       tier: "perf", year: "2020-2021", mileage: "40-80k km",   lo: 26000, hi: 33000, bothBounds: true },
    { model: "Model 3", trim: "Performance",       tier: "perf", year: "2022",      mileage: "20-50k km",   lo: 30000, hi: 37000, bothBounds: true },
    { model: "Model Y", trim: "Propulsion", tier: "base", year: "2022",             mileage: "40-80k km",   lo: 27000, hi: 33000, bothBounds: true },
    { model: "Model Y", trim: "Propulsion", tier: "base", year: "2023",             mileage: "20-50k km",   lo: 31000, hi: 38000, bothBounds: true },
    { model: "Model Y", trim: "Propulsion (Juniper facelift)", tier: "base", year: "2024", mileage: "<25k km", lo: 36000, hi: 43000, bothBounds: true },
    { model: "Model Y", trim: "Grande Autonomie AWD", tier: "lr", year: "2022",     mileage: "30-70k km",   lo: 33000, hi: 40000, bothBounds: true },
    { model: "Model Y", trim: "Grande Autonomie AWD", tier: "lr", year: "2023",     mileage: "15-45k km",   lo: 37000, hi: 44000, bothBounds: true },
    { model: "Model Y", trim: "Grande Autonomie AWD (Juniper facelift)", tier: "lr", year: "2024", mileage: "<20k km", lo: 42000, hi: 49000, bothBounds: true },
    { model: "Model Y", trim: "Performance",       tier: "perf", year: "2022-2023", mileage: "20-50k km",   lo: 38000, hi: 47000, bothBounds: true }
  ];
  var otherData = [
    { model: "Dacia Spring",           seg: "budget", note: "from €6,500 — no confirmed ceiling",             lo: 6500,  hi: 10000, bothBounds: false },
    { model: "Renault Zoe",            seg: "budget", note: "phase 2 (52kWh), 2020-22 cluster €14-19k",       lo: 9500,  hi: 19500, bothBounds: true },
    { model: "Nissan Leaf",            seg: "budget", note: "40kWh or 62kWh pack, 2019-2024",                 lo: 11500, hi: 22500, bothBounds: true },
    { model: "Peugeot e-208",          seg: "budget", note: "near-new (<10k km) cluster €24-31k",             lo: 18000, hi: 35000, bothBounds: true },
    { model: "Hyundai Kona Electric",  seg: "main",   note: "2022 facelift, ~40k km ≈ €20k",                  lo: 13000, hi: 20000, bothBounds: true },
    { model: "Volkswagen ID.3",        seg: "main",   note: "from €18,060 — no confirmed ceiling",            lo: 18060, hi: 24000, bothBounds: false },
    { model: "BYD Atto 3",             seg: "main",   note: "little discount off new (€37,990+) — too new to France for real depreciation yet", lo: 24990, hi: 36990, bothBounds: true },
    { model: "Renault Mégane E-Tech",  seg: "main",   note: "single example: 2022 EV60 220, 57k km, €15,990", lo: 14500, hi: 17500, bothBounds: false }
  ];
  var tierMeta = {
    base: { label: "Propulsion / SR+", varName: "--t-base" },
    lr:   { label: "Grande Autonomie / Long Range", varName: "--t-lr" },
    perf: { label: "Performance", varName: "--t-perf" }
  };
  var segMeta = {
    budget: { label: "Budget / city", varName: "--s-budget" },
    main:   { label: "Mainstream", varName: "--s-main" }
  };
  var svgNS = "http://www.w3.org/2000/svg";
  var cs = getComputedStyle(root);
  var tooltip = document.createElement("div");
  tooltip.className = "tooltip";
  function el(tag, attrs) {
    var e = document.createElementNS(svgNS, tag);
    for (var k in attrs) e.setAttribute(k, attrs[k]);
    return e;
  }
  function fmtE(v) { return "€" + v.toLocaleString("en-GB"); }

  function renderRangeChart(svgId, data, colorFn, xMin, xMax, xStep, groupKey, groupLabels) {
    var svg = document.getElementById(svgId);
    var chartCard = svg.closest(".card");
    chartCard.style.position = "relative";
    if (!tooltip.isConnected) chartCard.appendChild(tooltip);

    var W = 900, ML = 190, MR = 24, MT = 12, MB = 44;
    var rowH = 26, rowGap = 6, groupGapExtra = 16;
    var plotW = W - ML - MR;

    var rows = [];
    var y = MT;
    var lastGroup = null;
    data.forEach(function (d) {
      var g = groupKey ? d[groupKey] : null;
      if (groupKey && g !== lastGroup) {
        if (lastGroup !== null) y += groupGapExtra;
        rows.push({ type: "header", label: groupLabels[g] || g, y: y });
        y += 20;
        lastGroup = g;
      }
      rows.push({ type: "row", d: d, y: y });
      y += rowH + rowGap;
    });
    var plotH = y - rowGap + MB;
    var H = plotH + MT;
    svg.setAttribute("viewBox", "0 0 " + W + " " + H);

    function xPix(p) { return ML + (p - xMin) / (xMax - xMin) * plotW; }

    for (var v = xMin; v <= xMax; v += xStep) {
      var x = xPix(v);
      svg.appendChild(el("line", { class: "gridline", x1: x, x2: x, y1: MT, y2: y - rowGap }));
      var t = el("text", { class: "axis-label", x: x, y: y - rowGap + 20, "text-anchor": "middle" });
      t.textContent = "€" + (v / 1000) + "k";
      svg.appendChild(t);
    }
    svg.appendChild(el("line", { class: "baseline", x1: ML, x2: ML, y1: MT, y2: y - rowGap }));

    var xTitle = el("text", { class: "axis-title", x: ML + plotW / 2, y: H - 6, "text-anchor": "middle" });
    xTitle.textContent = "Used listing price (€)";
    svg.appendChild(xTitle);

    rows.forEach(function (r) {
      if (r.type === "header") {
        var hLabel = el("text", { class: "section-label", x: 0, y: r.y + 13 });
        hLabel.textContent = r.label;
        svg.appendChild(hLabel);
        svg.appendChild(el("line", { class: "grouprule", x1: ML, x2: ML + plotW, y1: r.y + 18, y2: r.y + 18 }));
        return;
      }
      var d = r.d;
      var cy = r.y;
      var color = colorFn(d);
      var x1 = xPix(d.lo), x2 = xPix(d.hi);

      var rowLabel = el("text", { class: "row-label", x: 8, y: cy + 12 });
      rowLabel.textContent = d.model + (d.year ? " — " + d.year : "");
      svg.appendChild(rowLabel);
      if (d.mileage) {
        var rowSub = el("text", { class: "row-sub", x: 8, y: cy + 23 });
        rowSub.textContent = d.mileage;
        svg.appendChild(rowSub);
      } else if (d.note) {
        var rowSub2 = el("text", { class: "row-sub", x: 8, y: cy + 23 });
        rowSub2.textContent = d.note.length > 40 ? d.note.slice(0, 38) + "…" : d.note;
        svg.appendChild(rowSub2);
      }

      var g = el("g", { class: "bar", tabindex: "0" });
      var rect = el("rect", { class: "range", x: x1, y: cy + 3, width: Math.max(x2 - x1, 3), height: rowH - 8, rx: 4, fill: color, opacity: d.bothBounds ? 0.88 : 0.55 });
      g.appendChild(rect);
      if (!d.bothBounds) {
        var hatchId = "hatch-used-" + Math.round(x1) + "-" + Math.round(cy);
        var pattern = el("pattern", { id: hatchId, width: 6, height: 6, patternTransform: "rotate(45)", patternUnits: "userSpaceOnUse" });
        pattern.appendChild(el("rect", { width: 3, height: 6, fill: cs.getPropertyValue("--open-hatch").trim() }));
        svg.appendChild(pattern);
        g.appendChild(el("rect", { x: x1, y: cy + 3, width: Math.max(x2 - x1, 3), height: rowH - 8, rx: 4, fill: "url(#" + hatchId + ")" }));
      }

      var loLabel = el("text", { class: "bar-label", x: x1 - 6, y: cy + rowH / 2 + 1, "text-anchor": "end" });
      loLabel.textContent = fmtE(d.lo);
      g.appendChild(loLabel);
      var hiLabel = el("text", { class: "bar-label", x: x2 + 6, y: cy + rowH / 2 + 1 });
      hiLabel.textContent = (d.bothBounds ? "" : "→ ") + fmtE(d.hi) + (d.bothBounds ? "" : "*");
      g.appendChild(hiLabel);

      function show() {
        tooltip.innerHTML = '<div class="t-name">' + d.model + (d.trim ? " · " + d.trim : "") + '</div>' +
          fmtE(d.lo) + '–' + fmtE(d.hi) + (d.bothBounds ? "" : " (upper bound unconfirmed)") +
          '<div class="t-flag">' + (d.year ? d.year + (d.mileage ? " · " + d.mileage : "") : "") + (d.note ? (d.year ? " · " : "") + d.note : "") + '</div>';
        var r2 = rect.getBoundingClientRect();
        var cardR = chartCard.getBoundingClientRect();
        tooltip.style.left = (r2.left - cardR.left + r2.width / 2) + "px";
        tooltip.style.top = (r2.top - cardR.top) + "px";
        tooltip.classList.add("show");
      }
      function hide() { tooltip.classList.remove("show"); }
      g.addEventListener("mouseenter", show);
      g.addEventListener("mouseleave", hide);
      g.addEventListener("focus", show);
      g.addEventListener("blur", hide);

      svg.appendChild(g);
    });
  }

  renderRangeChart("chart-tesla-used", teslaData, function (d) {
    return cs.getPropertyValue(tierMeta[d.tier].varName).trim();
  }, 10000, 50000, 10000, "model", { "Model 3": "Tesla Model 3", "Model Y": "Tesla Model Y" });

  renderRangeChart("chart-other-used", otherData, function (d) {
    return cs.getPropertyValue(segMeta[d.seg].varName).trim();
  }, 0, 40000, 10000, null, null);

  var table = document.getElementById("table-used");
  var thead = el("thead", {});
  var headRow = document.createElement("tr");
  ["Model", "Trim", "Year", "Mileage / note", "Price range", "Confidence"].forEach(function (h) {
    var th = document.createElement("th");
    th.textContent = h;
    headRow.appendChild(th);
  });
  thead.appendChild(headRow);
  table.appendChild(thead);
  var tbody = document.createElement("tbody");
  function addTableRow(model, trim, year, note, lo, hi, bothBounds) {
    var tr = document.createElement("tr");
    var tdModel = document.createElement("td");
    tdModel.className = "model";
    tdModel.textContent = model;
    tr.appendChild(tdModel);
    var tdTrim = document.createElement("td");
    tdTrim.textContent = trim || "—";
    tr.appendChild(tdTrim);
    var tdYear = document.createElement("td");
    tdYear.textContent = year || "—";
    tr.appendChild(tdYear);
    var tdNote = document.createElement("td");
    tdNote.textContent = note || "—";
    tr.appendChild(tdNote);
    var tdPrice = document.createElement("td");
    tdPrice.className = "num";
    tdPrice.textContent = fmtE(lo) + (bothBounds ? "–" : "+ ") + (bothBounds ? fmtE(hi) : "");
    tr.appendChild(tdPrice);
    var tdFlag = document.createElement("td");
    var flag = document.createElement("span");
    flag.className = "flag " + (bothBounds ? "confirmed" : "thin");
    flag.textContent = bothBounds ? "range sourced" : "one bound only";
    tdFlag.appendChild(flag);
    tr.appendChild(tdFlag);
    tbody.appendChild(tr);
  }
  teslaData.forEach(function (d) { addTableRow(d.model, d.trim, d.year, d.mileage, d.lo, d.hi, d.bothBounds); });
  otherData.forEach(function (d) { addTableRow(d.model, "—", "—", d.note, d.lo, d.hi, d.bothBounds); });
  table.appendChild(tbody);
})();
</script>

Other used candidates surveyed (Zoe, Leaf, Kona Electric, ID.3, Atto 3, Dacia Spring) mostly go well under new-car prices, except the Peugeot e-208 and BYD Atto 3, which barely discount at all. Full sourcing and caveats: [04-secondhand-market-survey.md](04-secondhand-market-survey.md).

**A real listing, checked against this:** a 2023 Model Y Performance near me on LeBonCoin, priced meaningfully below the band above — is it actually a good deal, and what would I check before trusting that? Full walkthrough, with the ad itself: [07-reading-a-real-listing.md](07-reading-a-real-listing.md). Getting to an answer took more than the ad could offer on its own, which is the whole subject of [08-why-buying-a-used-car-is-hard.md](08-why-buying-a-used-car-is-hard.md) (a stub for now).

## Price vs. mileage: a first Pareto cut

Putting price against mileage (as a rough stand-in for "quality" — lower mileage roughly means more life left) gives a first, imperfect version of the actual price-vs-quality frontier this project is aiming for. Worth being precise about what this is: each Tesla point below is the *midpoint* of a sourced price-and-mileage range from an aggregator article, not a real advertised car — there's no scraper here pulling live listings off La Centrale or LeBonCoin, just search results and the summary tables other sites have already built. So the frontier's overall shape (used Model 3 Propulsion trims dominating the lower-left) is a reasonable signal; the exact numbers aren't.

<div class="ev-chart" id="embed-mileage">
  <div class="card">
    <h3>Price vs. mileage</h3>
    <p class="sub">20 points · Tesla by trim tier + 2 other sourced examples · dashed line = Pareto frontier</p>
    <div class="chart-scroll">
      <svg class="chart" id="chart-mileage" viewBox="0 0 900 560" role="img" aria-label="Scatter plot of used EV price against mileage, coloured by model and shaped by Tesla trim tier, with a Pareto frontier line"></svg>
    </div>
    <div class="legend">
      <div class="grp">
        <span class="item"><span class="swatch" style="background:var(--series-1)"></span>Tesla Model 3</span>
        <span class="item"><span class="swatch" style="background:var(--series-2)"></span>Tesla Model Y</span>
        <span class="item"><span class="swatch" style="background:var(--series-3)"></span>Other (Kona Electric, Mégane E-Tech)</span>
      </div>
      <div class="divider-v"></div>
      <div class="grp">
        <span class="item"><span class="shape-key"><svg width="10" height="10"><circle cx="5" cy="5" r="4" fill="none" stroke="currentColor" stroke-width="1.5"/></svg></span>Propulsion / SR+ (or n/a)</span>
        <span class="item"><span class="shape-key"><svg width="10" height="10"><rect x="1" y="1" width="8" height="8" fill="none" stroke="currentColor" stroke-width="1.5"/></svg></span>Grande Autonomie</span>
        <span class="item"><span class="shape-key"><svg width="11" height="10"><polygon points="5.5,0 11,10 0,10" fill="none" stroke="currentColor" stroke-width="1.5"/></svg></span>Performance</span>
      </div>
    </div>
    <details class="data-table">
      <summary>Show full data (20 rows) ▾</summary>
      <div class="table-scroll"><table id="table-mileage"></table></div>
    </details>
  </div>
</div>

<script>
(function () {
  var root = document.getElementById("embed-mileage");
  var series = {
    model3: { label: "Tesla Model 3", varName: "--series-1" },
    modely: { label: "Tesla Model Y", varName: "--series-2" },
    other:  { label: "Other",         varName: "--series-3" }
  };
  var data = [
    { model: "Tesla Model 3", ser: "model3", trim: "Propulsion / SR+",  tier: "base", year: 2019, mileage: 125000, price: 15000,  src: "100-150k km × €13-17k" },
    { model: "Tesla Model 3", ser: "model3", trim: "Propulsion / SR+",  tier: "base", year: 2020, mileage: 95000,  price: 18500,  src: "70-120k km × €16-21k" },
    { model: "Tesla Model 3", ser: "model3", trim: "Propulsion / SR+",  tier: "base", year: 2021, mileage: 70000,  price: 22000,  src: "50-90k km × €19-25k" },
    { model: "Tesla Model 3", ser: "model3", trim: "Propulsion / SR+",  tier: "base", year: 2022, mileage: 50000,  price: 25000,  src: "30-70k km × €22-28k" },
    { model: "Tesla Model 3", ser: "model3", trim: "Propulsion / SR+",  tier: "base", year: 2023, mileage: 35000,  price: 29000,  src: "20-50k km × €26-32k" },
    { model: "Tesla Model 3", ser: "model3", trim: "Propulsion / SR+ (Highland)", tier: "base", year: 2024, mileage: 15000, price: 31500, src: "<30k km × €28-35k" },
    { model: "Tesla Model 3", ser: "model3", trim: "Grande Autonomie",  tier: "lr",   year: 2020, mileage: 105000, price: 21500,  src: "2019-20, 80-130k km × €18-25k" },
    { model: "Tesla Model 3", ser: "model3", trim: "Grande Autonomie",  tier: "lr",   year: 2021, mileage: 70000,  price: 27000,  src: "50-90k km × €24-30k" },
    { model: "Tesla Model 3", ser: "model3", trim: "Grande Autonomie",  tier: "lr",   year: 2023, mileage: 40000,  price: 31500,  src: "2022-23, 20-60k km × €27-36k" },
    { model: "Tesla Model 3", ser: "model3", trim: "Performance",       tier: "perf", year: 2021, mileage: 60000,  price: 29500,  src: "2020-21, 40-80k km × €26-33k" },
    { model: "Tesla Model 3", ser: "model3", trim: "Performance",       tier: "perf", year: 2022, mileage: 35000,  price: 33500,  src: "20-50k km × €30-37k" },
    { model: "Tesla Model Y", ser: "modely", trim: "Propulsion",        tier: "base", year: 2022, mileage: 60000,  price: 30000,  src: "40-80k km × €27-33k" },
    { model: "Tesla Model Y", ser: "modely", trim: "Propulsion",        tier: "base", year: 2023, mileage: 35000,  price: 34500,  src: "20-50k km × €31-38k" },
    { model: "Tesla Model Y", ser: "modely", trim: "Propulsion (Juniper)", tier: "base", year: 2024, mileage: 12500, price: 39500, src: "<25k km × €36-43k" },
    { model: "Tesla Model Y", ser: "modely", trim: "Grande Autonomie AWD", tier: "lr", year: 2022, mileage: 50000, price: 36500,  src: "30-70k km × €33-40k" },
    { model: "Tesla Model Y", ser: "modely", trim: "Grande Autonomie AWD", tier: "lr", year: 2023, mileage: 30000, price: 40500,  src: "15-45k km × €37-44k" },
    { model: "Tesla Model Y", ser: "modely", trim: "Grande Autonomie AWD (Juniper)", tier: "lr", year: 2024, mileage: 10000, price: 45500, src: "<20k km × €42-49k" },
    { model: "Tesla Model Y", ser: "modely", trim: "Performance",       tier: "perf", year: 2023, mileage: 35000,  price: 42500,  src: "2022-23, 20-50k km × €38-47k" },
    { model: "Hyundai Kona Electric", ser: "other", trim: null, tier: "base", year: 2022, mileage: 40000, price: 20000, src: "sourced example, not a band" },
    { model: "Renault Mégane E-Tech", ser: "other", trim: "EV60 220", tier: "base", year: 2022, mileage: 57202, price: 15990, src: "sourced example, not a band" }
  ];
  var svgNS = "http://www.w3.org/2000/svg";
  var svg = document.getElementById("chart-mileage");
  var cs = getComputedStyle(root);
  var W = 900, H = 560, ML = 66, MR = 24, MT = 20, MB = 56;
  var plotW = W - ML - MR, plotH = H - MT - MB;
  var xMin = 0, xMax = 160000, yMin = 10000, yMax = 50000;
  function xPix(m) { return ML + (m - xMin) / (xMax - xMin) * plotW; }
  function yPix(p) { return MT + (yMax - p) / (yMax - yMin) * plotH; }
  function el(tag, attrs) {
    var e = document.createElementNS(svgNS, tag);
    for (var k in attrs) e.setAttribute(k, attrs[k]);
    return e;
  }
  function fmtE(v) { return "€" + v.toLocaleString("en-GB"); }
  function fmtKm(v) { return v.toLocaleString("en-GB") + "km"; }

  var xTicks = [0, 25000, 50000, 75000, 100000, 125000, 150000];
  xTicks.forEach(function (v) {
    var x = xPix(v);
    svg.appendChild(el("line", { class: "gridline", x1: x, x2: x, y1: MT, y2: MT + plotH }));
    var t = el("text", { class: "axis-label", x: x, y: MT + plotH + 20, "text-anchor": "middle" });
    t.textContent = (v / 1000) + "k";
    svg.appendChild(t);
  });
  var yTicks = [10000, 20000, 30000, 40000, 50000];
  yTicks.forEach(function (v) {
    var y = yPix(v);
    svg.appendChild(el("line", { class: "gridline", x1: ML, x2: ML + plotW, y1: y, y2: y }));
    var t = el("text", { class: "axis-label", x: ML - 10, y: y + 4, "text-anchor": "end" });
    t.textContent = "€" + (v / 1000) + "k";
    svg.appendChild(t);
  });
  svg.appendChild(el("line", { class: "baseline", x1: ML, x2: ML + plotW, y1: MT + plotH, y2: MT + plotH }));
  svg.appendChild(el("line", { class: "baseline", x1: ML, x2: ML, y1: MT, y2: MT + plotH }));
  var xTitle = el("text", { class: "axis-title", x: ML + plotW / 2, y: H - 8, "text-anchor": "middle" });
  xTitle.textContent = "Mileage (km) — lower is fresher";
  svg.appendChild(xTitle);
  var yTitle = el("text", { class: "axis-title", x: 0, y: 0, "text-anchor": "middle", transform: "translate(18," + (MT + plotH / 2) + ") rotate(-90)" });
  yTitle.textContent = "Price (€)";
  svg.appendChild(yTitle);
  var zoneLabel = el("text", { class: "zone-label", x: xPix(3000), y: yPix(12500), "text-anchor": "start" });
  zoneLabel.textContent = "← better value";
  svg.appendChild(zoneLabel);

  var byMileage = data.slice().sort(function (a, b) { return a.mileage - b.mileage; });
  var frontier = [];
  var minPriceSoFar = Infinity;
  byMileage.forEach(function (d) {
    if (d.price < minPriceSoFar) {
      frontier.push(d);
      minPriceSoFar = d.price;
    }
  });
  var frontierIds = {};
  frontier.forEach(function (d) { frontierIds[d.model + d.year + d.trim] = true; });

  if (frontier.length > 1) {
    var pathD = "M " + xPix(frontier[0].mileage) + " " + yPix(frontier[0].price);
    for (var i = 1; i < frontier.length; i++) {
      pathD += " L " + xPix(frontier[i].mileage) + " " + yPix(frontier[i-1].price);
      pathD += " L " + xPix(frontier[i].mileage) + " " + yPix(frontier[i].price);
    }
    svg.appendChild(el("path", { class: "frontier-line", d: pathD }));
  }

  var tooltip = document.createElement("div");
  tooltip.className = "tooltip";
  var chartCard = svg.closest(".card");
  chartCard.style.position = "relative";
  chartCard.appendChild(tooltip);

  function shapeMark(tier, cx, cy, color, isFrontier) {
    var g = el("g", { class: "mark" });
    var r = 6;
    if (tier === "lr") {
      g.appendChild(el("rect", { x: cx - r * 0.85, y: cy - r * 0.85, width: r * 1.7, height: r * 1.7, fill: color, stroke: isFrontier ? "var(--frontier)" : "none", "stroke-width": isFrontier ? 1.5 : 0 }));
    } else if (tier === "perf") {
      var s = r * 1.15;
      g.appendChild(el("polygon", { points: cx + "," + (cy - s) + " " + (cx + s) + "," + (cy + s * 0.8) + " " + (cx - s) + "," + (cy + s * 0.8), fill: color, stroke: isFrontier ? "var(--frontier)" : "none", "stroke-width": isFrontier ? 1.5 : 0 }));
    } else {
      g.appendChild(el("circle", { cx: cx, cy: cy, r: r, fill: color, stroke: isFrontier ? "var(--frontier)" : "none", "stroke-width": isFrontier ? 1.5 : 0 }));
    }
    return g;
  }

  data.forEach(function (d) {
    var color = cs.getPropertyValue(series[d.ser].varName).trim();
    var cx = xPix(d.mileage), cy = yPix(d.price);
    var isFrontier = !!frontierIds[d.model + d.year + d.trim];
    var g = el("g", { class: "pt" + (isFrontier ? " frontier" : ""), tabindex: "0" });
    g.appendChild(el("circle", { class: "ring", cx: cx, cy: cy, r: 9 }));
    g.appendChild(shapeMark(d.tier, cx, cy, color, isFrontier));
    var yearLabel = el("text", { class: "pt-year", x: cx + 9, y: cy - 8 });
    yearLabel.textContent = d.year;
    g.appendChild(yearLabel);
    function show() {
      tooltip.innerHTML = '<div class="t-name">' + d.model + (d.trim ? " · " + d.trim : "") + '</div>' +
        fmtE(d.price) + ' &middot; ' + fmtKm(d.mileage) +
        '<div class="t-flag">' + d.year + (isFrontier ? " · on frontier" : "") + '</div>' +
        '<div class="t-flag">' + d.src + '</div>';
      var r2 = chartCard.getBoundingClientRect();
      tooltip.style.left = (cx / W) * r2.width + "px";
      tooltip.style.top = (cy / H) * (r2.height - 40) + "px";
      tooltip.classList.add("show");
    }
    function hide() { tooltip.classList.remove("show"); }
    g.addEventListener("mouseenter", show);
    g.addEventListener("mouseleave", hide);
    g.addEventListener("focus", show);
    g.addEventListener("blur", hide);
    svg.appendChild(g);
  });

  var sorted = data.slice().sort(function (a, b) { return a.mileage - b.mileage; });
  var table = document.getElementById("table-mileage");
  var thead = el("thead", {});
  var headRow = document.createElement("tr");
  ["Model", "Trim", "Year", "Mileage", "Price", "Frontier?"].forEach(function (h) {
    var th = document.createElement("th");
    th.textContent = h;
    headRow.appendChild(th);
  });
  thead.appendChild(headRow);
  table.appendChild(thead);
  var tbody = document.createElement("tbody");
  sorted.forEach(function (d) {
    var isFrontier = !!frontierIds[d.model + d.year + d.trim];
    var tr = document.createElement("tr");
    var tdModel = document.createElement("td");
    tdModel.className = "model";
    tdModel.textContent = d.model;
    tr.appendChild(tdModel);
    var tdTrim = document.createElement("td");
    tdTrim.textContent = d.trim || "—";
    tr.appendChild(tdTrim);
    var tdYear = document.createElement("td");
    tdYear.textContent = d.year;
    tr.appendChild(tdYear);
    var tdMileage = document.createElement("td");
    tdMileage.className = "num";
    tdMileage.textContent = fmtKm(d.mileage);
    tr.appendChild(tdMileage);
    var tdPrice = document.createElement("td");
    tdPrice.className = "num";
    tdPrice.textContent = fmtE(d.price);
    tr.appendChild(tdPrice);
    var tdFlag = document.createElement("td");
    if (isFrontier) {
      var flag = document.createElement("span");
      flag.className = "flag frontier-flag";
      flag.textContent = "frontier";
      tdFlag.appendChild(flag);
    } else {
      tdFlag.textContent = "—";
    }
    tr.appendChild(tdFlag);
    tbody.appendChild(tr);
  });
  table.appendChild(tbody);
})();
</script>

Replacing these midpoints with real individual listings is the next research step.

## What's next

The weighted frontier (real feature weights, not range/mileage as a stand-in), a deeper pass on actual used listings, and a final purchase decision. Also underway: [07-reading-a-real-listing.md](07-reading-a-real-listing.md), a worked example of pricing a real ad against this research, and [08-why-buying-a-used-car-is-hard.md](08-why-buying-a-used-car-is-hard.md), the start of a piece on why that's hard in general — it may eventually outgrow this folder and become its own piece. Tracked in [plan.md](plan.md).
