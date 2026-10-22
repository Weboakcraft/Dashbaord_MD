# Oakcraft MD Master Dashboard

Managing Director ke liye ek single-file master dashboard — poore Oakcraft business ka live view, ek hi page par.

**Live URL (GitHub Pages enable karne ke baad):** `https://weboakcraft.github.io/Dashbaord_MD/`

## Kya dikhata hai

- **14 live KPI tiles** — Deals in Pipeline (value ke saath), Revenue This Month (last month se % delta), Deals Won/Lost, Negotiation, Pending for Quotation, Pending PO, Follow-up, New Enquiries, Leads in Pipeline (Meta + IndiaMART), Contact Not Established, Open Orders, Payment Pending, Quotations Open.
- **Business Trends** — last 12 months revenue + deals-won trend, pipeline funnel by stage, lead sources, salesperson leaderboard, order book status. Har chart par hover tooltip.
- **B2B MIS Report** — source-wise Total/Qualified/Won/Lost, revenue, conversion %, avg revenue, grand total — CSV download ke saath.
- **Attention Needed** — stale deals, unassigned leads, payment pending, dispatch overdue, biggest open quotes — MD ko aaj kya chase karna hai.
- **Oakcraft Modules** — saare 23 apps (Sales CRM, CRR Tracker, Complaints, Attendance, Expense, Production, …) ke cards, direct open + code links.

## Data kahan se aata hai

Sales CRM ka Google Apps Script backend built-in hai (`?action=getAll`) — wahi endpoint jo `Oakcraft_Sales_CRM` use karta hai. Collections: enquiries, quotations, orders, dispatch, customers, metaLeads, indiamartLeads.

- Auto-refresh har 5 minute; manual ⟳ Refresh bhi hai.
- Last successful pull browser cache me rehta hai — offline par cached data dikhata hai.
- Backend bilkul unreachable ho to demo data ke saath layout dikhta hai (header me saaf likha aata hai).

## Dusre modules ko connect karna

⚙ **Settings** kholo → kisi bhi module ke saamne uska Apps Script `/exec` URL paste karo (same `getAll` pattern) → us module ke card par live record counts aane lagenge. Config sirf aapke browser (localStorage) me save hoti hai.

## Filters

Year · Month · Salesperson · Source — KPIs, charts, MIS report sab par lagte hain. Theme toggle (light/dark) header me hai.
