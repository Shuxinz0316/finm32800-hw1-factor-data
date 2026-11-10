# HW1 replicated Fama–French factors

This data-only upstream contains monthly SMB and HML factor returns computed by
Shuxin Zhang's FINM 32800 HW1 implementation. The private homework source and
licensed security-level data are not included. The CSV contains `date`, `SMB`,
and `HML`; returns are decimals (0.01 means 1%).

The published observation window is July 2025 through June 2026, with a fixed
cutoff of 2026-06-30. For this snapshot, monthly CRSP CIZ data were pulled on
2026-11-10 for the period beginning December 2022; Compustat annual observations
were read from the existing HW1 cache and limited to accounting dates no later
than the cutoff. The existing CRSP–Compustat link-table cache was also used.
The HW1 implementation at private commit `a73e09c132c50863efe77331ea3f4bc9b3e85b17`
formed six size and book-to-market portfolios and computed the two factors.
The caches and current CRSP extract may contain later vendor revisions: this is
a cutoff by observation date, not a point-in-time historical vintage.

`chartbook.toml` declares the committed derived series for a consumer to pin.
The snapshot has no build script and contains no security-level data or keys.
