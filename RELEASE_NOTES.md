# Release Notes

## v1.2.0
GH#863 (K-045 intent/output-mismatch) — wire the `ad-copy-generator` prompt into the workflow so the pipeline actually produces ad copy. Previously the prompt was declared but never invoked: the flow built a campaign brief, then ran A/B and conversion analysis on nothing, then polished nothing. Added an `Ad Copy Generation` step (new backing skill `ad-copy-generation`) after audience segmentation and before the analysis/optimisation/polish stages, bound to the segmentation output. Converted the generator's positional `{{steps.Audience Segmentation.output}}` reference to a `context_params` binding. Re-pinned `polish-language`→1.0.6 and bound its `source` ← the ad-copy step so the output step polishes the real deliverable. Skills 2→3, total 7→8.

## v1.1.23
GH#845 — republish with American English (en-US) content, completing the source-only GH#805 flip that never reached the Hub. Copy only — no functional or behaviour change.

## v1.1.22
GH#745 — declare per-step `output: {name, type}` on every execution step (campaign_brief/text, ab_test_analysis/text, conversion_recommendations/text, polished_ad_copy/text). Lights up the #744 rich flow-map with named, typed outputs. Content-only; no bindings or logic changes.

## v1.1.21
GH#645 Row 3b — migrate to K-037 dep-referenced schema. Strip 9 inline shared-content files and declare 9 hub-shared deps (UUID id + slug name + version + checksum from `gen-dep-checksums.mjs`). Closes pre-Step-3 inline-vendoring for this bundle.

## v1.1.20
Wave 2: re-signed with canonical engine signing pipeline.

## v1.1.19
Tags migrated inline into manifest (GH#586). tags.yaml retired.

## v1.1.18
Bundle re-signed with canonical engine signing pipeline (Wave 2 migration).

## v1.1.17
Signature fix — RELEASE_NOTES.md now included in integrity checksum.

## v1.1.16
Initial catalog release with full structural and content-quality validation. All scanner checks pass.
