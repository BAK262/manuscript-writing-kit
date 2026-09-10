# Example: cite briefs

Synthetic snippets for `【cite:…】` handling. Not a real paper.

## Open brief (topic + count)

```latex
Prior ambulatory sleep datasets emphasized either clinic PSG or consumer wearables in isolation【cite: 2 empirical dataset papers; prefer IEEE/ACM venues; exclude pure actigraphy-only diaries】.
```

**Expected agent behavior:** triple-pool search inside brief bounds; keep marker until two acceptable keys; may place provisional `\cite{...}` after marker while **open-partial**.

## Closed after resolve

```latex
Prior ambulatory sleep datasets emphasized either clinic PSG or consumer wearables in isolation~\cite{Smith2020HomePSG,Lee2021WearableCohort}.
```

Marker removed; keys support **this sentence’s** claim only.

## Conditional no-cite

```latex
Wearable nights are not treated as drop-in PSG substitutes【cite: one strong methods paper on device inequivalence; otherwise no cite】.
```

If no strong hit → decision **E** or brief-closed no-cite per clause; do not widen to decorative reviews.

## Mandatory + fallback

```latex
Stage scoring follows AASM guidance【cite: must include Berry et al. AASM manual; if unavailable use Iber 2007 as fallback】.
```

Do not drop the mandatory work when a “better” secondary paper appears.
