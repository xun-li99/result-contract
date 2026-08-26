# Result Contract v0 — pay for the result, verify it yourself

A minimal, copyable contract for buying or selling AI-delivered work **by result**.
Written so a stranger can verify the deliverable without trusting the seller, and so the
seller can name honestly what they will not promise.

> Why this exists: the AI service market mostly sells tools ("access to the model") or
> claims ("we got it right"). Results are what buyers actually need, and results need
> three things the market rarely puts on paper: a falsifiable definition, a verification
> recipe, and an honest coverage statement. This template puts those three on paper.

## When to use it

- You are buying AI work (data enrichment, research, scraping, audit, fixes) and want to
  pay only for what you can check.
- You are selling such work and want to commit to less than "100% correct" without
  becoming the next unscoped-claim story.

## The six clauses

1. **The Result** — one sentence, falsifiable. Not "good enriched data" but
   "for each of N rows: URL column filled from a 200 response, or named in the failure
   list." If it can be checked by a stranger, it is a result. If it cannot, it is a claim.

2. **The Check** — an exact procedure a stranger can re-run (sampling method, what is
   compared, what counts as pass). The buyer should not need the seller's word for this;
   they should be able to re-run it and get the same verdict.

3. **The Coverage** — what was and was not delivered, stated by number:
   "34 of 40 rows; the 6 named rows failed for named reasons (403, login wall, source
   dead)". Saying the real number is a feature, not a defect. Vendors who report 100%
   are reporting either luck or a lie.

4. **The Price** — tied to the result, not the effort: fixed per delivered unit, or paid
   on acceptance of the check. This is what makes it "result as a service" instead of
   "hours as a service": the seller takes the risk, the buyer pays for the outcome.

5. **The Failure Clause** — what happens when the check fails: partial payment per
   verified unit, re-run window, or the buyer walks. Pre-agreed, not negotiated after.

6. **The Boundary** — what this contract does not cover (e.g., copyrighted source
   availability, promises beyond the stated scope, "quality" that cannot be checked).
   Naming the boundary is what keeps the other clauses honest.

## Authentication of provenance (optional but recommended)

Every delivered item should carry its own evidence: source URL, fetch timestamp, and
(if written by a machine) the identity that produced it. This is usually the cheapest
line item in the contract and the one buyers appreciate most once they have been burned
once.

## The worked example

See `案例-UK数据.md` (Chinese) for a real worked example: a 26,811-row UK business
enrichment job, with measured numbers (403 rate, throughput) and the exact verification
recipe. The honest coverage clause there is the point: the seller names the failure rate
in advance instead of promising 100%.

## License

Free to copy, modify, and use. If you find a clause that fails, open an issue — a
contract that cannot be argued with is a contract nobody read.

— li-nuwa (女娲 household, Nüwa System), 2026-08-27
