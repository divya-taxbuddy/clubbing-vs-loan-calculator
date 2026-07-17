# Clubbing vs. Loan-to-Spouse — Tax Comparator

A single-page, client-side calculator that compares two tax treatments for jointly-funded rental property income in India:

- **Scenario A — Straight clubbing (Sec 64(1)(iv)):** rental income is clubbed into the higher-earning spouse's hands and taxed at their slab, after the 30% standard deduction (Sec 24(a)).
- **Scenario B — Loan to spouse:** the higher-earning spouse lends the purchase amount to the other at a market interest rate. Interest income is taxed in the lender's hands; residual rental income (after the 30% standard deduction and Sec 24(b) interest deduction) is taxed at the borrower's slab.

The family's total tax outcome under both routes updates live as you change property value, rent, loan amount, interest rate, and each spouse's slab.

**Live demo:** enable GitHub Pages on this repo (Settings → Pages → Deploy from branch `main` / root) and it will be served from `index.html`.

## Assumptions & caveats

- Sec 24(a) 30% standard deduction is applied to rent in both scenarios.
- Sec 24(b) interest deduction is treated as uncapped, since the ₹2L cap only applies to self-occupied property, not let-out property.
- This is a **planning estimate**, not a filing position. It does not account for loss carry-forward if interest exceeds net rental income, surcharge/cess, or other income the spouses may have. Verify against current-year slab rules and have any loan agreement reviewed before executing.

## Tech

Pure HTML/CSS/JS, no build step, no dependencies, no network calls beyond loading Google Fonts. Safe to open `index.html` directly in a browser or serve as a static site.

## Local usage

```bash
open index.html
```

or serve it:

```bash
python3 -m http.server 8000
```

## License

MIT — see [LICENSE](LICENSE).
