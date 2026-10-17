<!-- oss-factory:v1
{"id":"20261017-lane23-openontology-queue","kind":"state","project":"openontology","from":"chatgpt","to":["factory"],"status":"working","dedupe_key":"promotion-queue:Doss-com/openontology","branch":"coord/lane23-promotion-queue-20261017","commit":"7d34e79f9b1cfc30773387dcb3f8ae8b17dadabe","civ":{"city_id":"oss:openontology"}}
-->

# OpenOntology promotion queue

Target: `Doss-com/openontology`; coordination fork: `kvnloo/openontology` (Issues disabled). This branch and its downstream PR are the single project-local queue. Do not merge this coordination document into either default branch or send it upstream. Last audit: 2026-10-17.

This migrates the full historical body and sole comment of [legacy factory queue #71](https://github.com/kvnloo/oss-factory/issues/71), preserved below. The old Linear gate, factory-local routing and READY_FOR_HITL wording are historical, not current instructions. Current policy is [HITL](https://github.com/kvnloo/oss-factory/blob/main/factory/HITL.md) and [promotion queues](https://github.com/kvnloo/oss-factory/blob/main/factory/PROMOTION_QUEUES.md). Provisional routing: [registry PR #190](https://github.com/kvnloo/oss-factory/pull/190), proposed project `openontology`, city `oss:openontology`, state `watch`; not asserted merged.

## Goal lock and bounded decision

<!-- oss-factory:v1
{"id":"20261017-lane23-openontology-decision","kind":"decision","project":"openontology","from":"chatgpt","to":["factory"],"status":"working","dedupe_key":"promotion-queue:Doss-com/openontology","civ":{"city_id":"oss:openontology"},"goal_lock":{"objective":"Qualify existing finished OpenOntology work and resolve existing authorized origin review/CI without duplicates or lost contributor credit","targets":["Doss-com/openontology:main@7d34e79f9b1cfc30773387dcb3f8ae8b17dadabe","kvnloo/openontology:main@7d34e79f9b1cfc30773387dcb3f8ae8b17dadabe"],"controls":["origin/fork exact-head comparison"],"fixture":"all fork refs/PRs, origin all-state PR history, legacy queue body and comment","environment":"Linux ARM64 phone/PRoot; authenticated GitHub reads; isolated fork checkout","proof":"Any promoted code must execute its real changed behavior on the exact candidate SHA; source inspection alone is not runtime proof"},"execution_proof":{"tested":[],"runtime":"No product changes or candidate runtime executed in this inventory/migration","result_status":"NOT RUN"}}
-->

Kevin's active Lane23 instruction authorizes a bounded audit and promotion of qualifying, already-finished named-project work, and same-PR review/CI repair. It does not authorize inventing new features, duplicate publications, forged signoffs, or default-branch merges. This worker receipt records that instruction; it does not create approval. No origin action was selected in this wave. No Linear dependency applies.

## Ready

**None verified ready.** The fork has only `refs/heads/main`, no tags or other matching refs, and no open or closed downstream PRs. GitHub compare `Doss-com/openontology/main...kvnloo:main` is `identical`, ahead 0 / behind 0, at `7d34e79f9b1cfc30773387dcb3f8ae8b17dadabe`. There is no unpublished finished fix to promote or commit.

## Existing upstream review

No factory-owned live origin PR exists. All 19 returned origin PR records (open and closed) were inspected for ownership, scope and duplication. The only open PRs are owner-covered dependency updates:

| Item / owner | Exact current head | Review and CI at audit | Disposition |
| --- | --- | --- | --- |
| [#19](https://github.com/Doss-com/openontology/pull/19), dependabot, Node type bump | `4a5c4cb6cc1319fd93a9b0e386a9c0910b2b9f8a` | MERGEABLE; no comments, submitted reviews or inline threads; Node 24/26 checks SUCCESS, CodeQL NEUTRAL | OWNER_COVERED; not a factory repair or promotion candidate |
| [#20](https://github.com/Doss-com/openontology/pull/20), dependabot, Prettier bump | `15b623fdae5e3b23a0516746df1d7955e6dafbb7` | MERGEABLE; no comments, submitted reviews or inline threads; Node 24/26 checks SUCCESS, CodeQL NEUTRAL | OWNER_COVERED; not a factory repair or promotion candidate |

Evidence: [#19 current-head CI](https://github.com/Doss-com/openontology/actions/runs/38829299750), [#20 current-head CI](https://github.com/Doss-com/openontology/actions/runs/38829304829). These are origin-supplied results, not tests run by this worker. No required-check completeness is inferred from these visible contexts.

## Needs proof

| Candidate / provenance | Behavior and requirement | Evidence and remaining gate | Disposition |
| --- | --- | --- | --- |
| Malformed MCP initialization `protocolVersion`; historical dot review checkpoint [comment 6120010527](https://github.com/kvnloo/oss-factory/issues/71#issuecomment-6120010527); original engine credit Wiley Jones | At exact main `7d34e79f9b1cfc30773387dcb3f8ae8b17dadabe`, [handler line 506](https://github.com/Doss-com/openontology/blob/7d34e79f9b1cfc30773387dcb3f8ae8b17dadabe/src/product/mcp.ts#L488-L509) echoes any non-nullish `params.protocolVersion`. Independently read [pinned MCP schema](https://github.com/modelcontextprotocol/modelcontextprotocol/blob/1f520964b295d58494d944f2aea8a5ab51c79f77/schema/2025-06-18/schema.ts#L176-L205): InitializeRequest and InitializeResult declare a string. | SOURCE_ONLY. No patch, regression, red/green or real CLI malformed-input execution exists in recovered fork work. No real supported-client impact or maintainer request was recovered; malformed-request handling must not be inflated into a normal-client failure. The source contract does not by itself choose rejection versus negotiation/fallback, or justify an unsupported-version allowlist. | LIMITED / NOT FINISHED, not promotion-ready. Outside this finished-work handoff: do not invent a new implementation to inflate submissions. Next action requires a separately scoped decision about desired malformed-request behavior and exact-head native regression evidence. |

## Held or superseded

- The older unspecified canceled publication scope in the legacy queue remains canceled. No branch or finished patch was recovered; do not revive or repackage it.
- [Issue #12](https://github.com/Doss-com/openontology/issues/12) was authored by Wiley Jones and closed 2026-09-27 after [PR #13](https://github.com/Doss-com/openontology/pull/13). Its explicit requirements include bounded native object discovery and identity-safe reuse, with synthetic SDK/CLI/MCP cases. Those requirements are already owner-covered by the verified merges below; no duplicate implementation or PR is warranted.
- Closed unmerged PRs #1, #4, #9–11, #16–18 were included in duplicate/ownership inventory; no distinct downstream finished candidate or factory review repair was found. Other historical releases/refactors (#2–8) are upstream-owned history, not unpublished factory work.

## Landed

Fresh GitHub PR `merged` state and `mergeCommit.oid` were read. These are externally performed maintainer merges, not worker merges or new Lane23 submissions. Preserve Wiley Jones (`wileyjones`) authorship.

| Original item | Source head | Verified origin merge SHA |
| --- | --- | --- |
| [#13 native object discovery and identity-safe reuse](https://github.com/Doss-com/openontology/pull/13), merged 2026-09-27 | `5bde837eb28f4deca6a7b4a0c0636aad484a2661` | `c7ee48138ad7dc2a027d9eafcdcfab360f5f9083` |
| [#14 catalog provenance](https://github.com/Doss-com/openontology/pull/14), merged 2026-09-27 | `806c9d27f40dcc711006fdbab2b981f44dc25a87` | `d132a850a86a94d186b4122af04f4446c42f6abe` |
| [#15 alpha.7 question coverage and immutable map validation](https://github.com/Doss-com/openontology/pull/15), merged 2026-09-28 | `4166943f4c5f2b9419f2721f08dd10397ad1f3bb` | `7d34e79f9b1cfc30773387dcb3f8ae8b17dadabe` |

## Policy and verification limits

Read current project [AGENTS](https://github.com/Doss-com/openontology/blob/7d34e79f9b1cfc30773387dcb3f8ae8b17dadabe/AGENTS.md), [CONTRIBUTING](https://github.com/Doss-com/openontology/blob/7d34e79f9b1cfc30773387dcb3f8ae8b17dadabe/CONTRIBUTING.md), [SECURITY](https://github.com/Doss-com/openontology/blob/7d34e79f9b1cfc30773387dcb3f8ae8b17dadabe/SECURITY.md), PR template and workflows. Apache-2.0. No explicit AI-contribution ban, CLA or DCO requirement was found in these contribution surfaces; absence is not blanket approval. Behavior changes larger than small fixes start from an issue. Security reports use private GitHub advisories; no public vulnerability claim was posted. Keep exact Evidence separate from navigation, and do not publish private corpora, credentials or generated research traces.

This wave changed coordination documentation only. No product tests, build, formatter or release gate was run, and no runtime or performance result is claimed. Product changes would require `npm test` and `npm run release:check`; any later malformed-init patch must exercise the actual CLI transport on its exact SHA. No origin comments/issues/PRs, CI retriggers, implementation commits, or default-branch merges were made. Historical CI, historical checks and current source inspection remain distinctly labeled above.

## Preserved legacy record (historical, not current policy)

Source: [factory issue #71](https://github.com/kvnloo/oss-factory/issues/71), created 2026-10-11T19:45:13Z, last updated before migration 2026-10-16T08:12:42Z, GitHub account `kvnloo`, original envelope author `ayo`. Original reporter/reviewer provenance and historical wording are retained verbatim below.

````markdown
<!-- oss-factory:v1
{"id":"20261011-ayo-project-openontology-001","kind":"state","project":"oss-factory","from":"ayo","to":["factory"],"status":"working","parent_id":"20261011-ayo-work-tracker-001","dedupe_key":"oss-factory-project-work-index-openontology","civ":{"city_id":"oss:oss-factory"}}
-->

## Canonical per-repo promotion queue — 2026-10-16
This existing project issue is the **single authoritative promotion queue** for `Doss-com/openontology` (OpenOntology); [factory dashboard #14](https://github.com/kvnloo/oss-factory/issues/14) is only the cross-repository index. REGISTRY_PENDING. The historical evidence records, ownership, credit and links below are preserved, not upgraded to current READY or reallocated. Do not open a competing per-repo promotion tracker.

**Current state rule:** `READY_FOR_HITL` requires independent requirement proof, exact-head source and native checks, maintainer feedback/CI, owner/duplicate/policy review, and a minimal authorized proposal. The actual Linear origin-write gate remains separate. `IN_REVIEW` already has an origin URL; `LANDED` only after merge SHA verification. Otherwise `CHECK/LIMITED/HOLD/WAIT/DISCARDED` and one exact unblocker. Historical work remains historical until rechecked.

Append/check one row per distinct contribution using its original origin issue/PR, fork SHA and source, executed test commands/results, current feedback, contributor credit, disposition and next action. Mirror only newly qualified READY rows to the #14 index. Do not create new per-repo queue issues or publish origin changes without HITL.

---


## Purpose
Project-level index for existing public **OpenOntology** work, created at Kevin's request. [dot work index #64](https://github.com/kvnloo/oss-factory/issues/64) → this project → individual issue/PR or evidence record → [shared all-agent promotion dashboard #14](https://github.com/kvnloo/oss-factory/issues/14).

This is coordination tracking, not a new implementation claim or a second promotion queue. Preserve each contributor's ownership. Reuse existing downstream mirrors before creating a work-item issue.

## Registry and routing
**REGISTRY_PENDING.** This target is absent from the current main project registry. The existing work is indexed under OSS Factory coordination only; no per-project city ID or automation-routing registration is asserted.



## Recovered work-item tracking
Snapshot: 2026-10-11. Evidence is historical unless a row explicitly reports a current requalification. **No unchecked candidate is automatically ready or authorized.** Exact commands remain in linked receipts; missing details are explicit backfill work.

| Work item / record | Known revision | Evidence | Status / blocker / next action | Owner / credit |
|---|---|---|---|---|
| [#12–15](https://github.com/Doss-com/openontology) | Not recovered / local only | Read-only dedupe:13–15Wileymerged,12closed;upstream/fork7d34e79f | **DROP**. No new implementation;publication of older canceledscope withheld. Next: retain historical disposition; no revival. | Wiley Jones;dot review |

## Per-item acceptance and update contract
- Link each origin issue/PR to exactly one canonical downstream work record where available.
- Record tested origin SHA, fork SHA, branch, exact commands, RED/GREEN or review evidence, independent QA, limits, owner, disposition and next action.
- Keep source-only, mocked, native CPU, native desktop and live-provider results distinct.
- Append timestamped result/blocker receipts; preserve earlier failures and author credit.
- Mirror only freshly qualified publication candidates to `#14`. Hermes handles authorized origin publication; this card grants no origin write, merge, signoff or permission recovery.
- Historical backfill is ongoing. Unknown branch names, exact commands, current origins or registry prerequisites remain gates.
````

### Preserved sole legacy comment

[comment 6120010527](https://github.com/kvnloo/oss-factory/issues/71#issuecomment-6120010527), account `kvnloo`, created and updated 2026-10-12T07:48:26Z. The body below is historical source-only evidence, not a fresh runtime result.

````markdown
Read-only candidate checkpoint, 2026-10-12: OpenOntology `7d34e79f9b1cfc30773387dcb3f8ae8b17dadabe` [initialization](https://github.com/Doss-com/openontology/blob/7d34e79f9b1cfc30773387dcb3f8ae8b17dadabe/src/product/mcp.ts#L488-L509) echoes a non-string protocolVersion into successful InitializeResult. [MCP schema](https://github.com/modelcontextprotocol/modelcontextprotocol/blob/1f520964b295d58494d944f2aea8a5ab51c79f77/schema/2025-06-18/schema.ts#L176-L205) requires a string. Existing real-CLI product test supports a narrow malformed-type regression; no code/test run or claim made. CHECK / SOURCE_ONLY; implementation HOLD while registration remains pending. Do not infer unsupported-version allowlist from this finding. Public origin/fork branches and all issues/PRs checked; dependency PRs #16/#18 do not overlap. Credit Wiley Jones original engine. Cancelled publications remain blocked.
````
