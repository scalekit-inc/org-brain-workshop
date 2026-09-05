# Fix: invoice tax rate + proration calculation

Two related invoice-math fixes:
- PDF renderer now reads the same resolved per-country VAT rate used for the actual charge.
- Downgrade proration now credits based on the old plan's price, not the new plan's.
