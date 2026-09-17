# Scar and stitch

**Standing rule for this tree.**

Adversarial review without a repair path is incomplete. It does not ship.

## Rule

Every adversarial leaf (`KS-*`, `MD-*`, and any later attack tier) **must** include:

1. **The scar** — what fails, who can land it, why it matters.
2. **The stitch** — concrete remediation options the Steward can pick (or reject with reason).
3. **The self-check** — how the subject (city, client, Steward) verifies the stitch held — without us in the room.

A leaf that only says “this sucks” is **not** a valid adversarial leaf here. Close it, rewrite it, or don’t merge it.

## Why

Attack alone is cruelty with a clipboard. Hidden Door’s product is the pair: find the wound, show how to close it — and leave a way to **check your own work** so the fix isn’t theater.

## Checklist (PR / commit)

- [ ] Leaf has `Remediation options` (or equivalent) with at least one actionable path
- [ ] Leaf has `Self-check` steps (observable pass/fail — not vibes)
- [ ] Options are Steward-choosable (not “feel better”)
- [ ] Status stays `open` until Steward Decision — remediation text ≠ auto-closed
- [ ] Genre stays named `adversarial` — stitches don’t launder critique into praise

## Survives tier

`survives/` leaves document what holds. They need no stitch. They are not attacks.

## Related

- Self-check method (full): [`CHECK-YOUR-OWN-WORK.md`](CHECK-YOUR-OWN-WORK.md)
- Sellable bar: [`../demands/sellable-bar.md`](../demands/sellable-bar.md)
