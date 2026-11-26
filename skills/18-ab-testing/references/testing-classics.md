# Testing classics (Hopkins & Bencivenga)

Pair these foundational split-testing principles with sample-size math (`sample_size.py`) and strict fixed-horizon or sequential decision rules so experiments produce revenue truth instead of false winners. Never fabricate test data or lifts.

## 1. Keyed-ad testing (Hopkins)

From Claude Hopkins (*Scientific Advertising*):

- **Every test variant carries its own unique key or tracking identifier** (clean URL parameter, dedicated coupon/promo code, tagged form/call number, or split URL) so responses tie directly to actual leads, orders, and revenue rather than vanity clicks or impressions.
- **Test big differences first:** Hopkins proved that testing one clear headline promise, offer angle, or risk-reversal structure beats tweaking minor button tints or single prepositions on low-traffic pages.
- **Keep conditions equal:** run A and B simultaneously across matching audience slices, never week-before vs. week-after, so seasonality does not fake a win.

## 2. Beat-the-control testing (Bencivenga)

From Gary Bencivenga (*Bencivenga Bullets*):

- **Respect the Control:** once a test establishes a verified winner (measured on the primary business metric with sufficient sample size and guardrail checks), it becomes the **Control**, the benchmark every future idea must beat cleanly to earn replacement.
- **70 / 30 testing budget mindset:** keep proven traffic on the standing Control (protecting current profit and CAC) while pitting bold challenger concepts against it cleanly until statistically decided.
- **Measure down to real profit, not shallow engagement:** a headline or ad variant that lifts CTR 30% while lowering qualified lead conversion or raising refund rates loses to the Control. Log every decision cleanly in `18-experiment-log`.
