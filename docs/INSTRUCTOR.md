# Instructor Runbook

[Home](../README.md) | [Agenda](AGENDA.md) | [Participant path](PORTAL-GUIDE.md)

## Architecture and Authorized Scope

This track uses prompt agents and File Search in the new Foundry.
It does not execute custom Python functions. The policy has therefore
been adapted as **OPS-PORTAL-2026-11**: recommendations instead of local
order drafts with CLI approval. Do not copy the original policy and its
execution promises unchanged into this track.

You can use an existing, approved Foundry resource, model, and projects.
New portal agents receive their own names, such as `orderops-p01-portal`;
existing SDK agents and their indexes remain untouched. Preindexing and
agent creation are Azure writes and require an explicit scope/cost decision.

This repository is only the materials package. It does not assign roles,
create accounts, or deploy resources automatically.

## Prepare the English Delivery Separately

**Changing GitHub content does not update pre-provisioned Azure agents or
indexed files.** A previously prepared workshop setup may still use the
**previous German edition**. This translation changes no accounts, project
roles, agents, or indexed content. The source filenames and policy ID may
match this edition while the actual indexed passages and agent instructions
are still German.

Before English delivery, separately review and authorize this configuration
work. These are instructor setup instructions, not provisioning automation:

1. Retain the approved model, including its deployment identifier
   `orderops-model`, existing projects, and existing permission scopes.
   Translating materials is not authorization to expand access.
2. Select the English starter/reference instructions and the four English
   core files in this repository. Do not include the optional attack note
   in the core corpus.
3. Prefer a dedicated new index in each assigned project, for example
   `orderops-p01-knowledge-en`. Wait for all four files to finish indexing.
   Do not automatically delete, replace, or overwrite existing German indexes.
4. Configure explicitly identified English agent versions and connect the
   intended English index. Preserve existing German versions and original
   SDK agents; document the exact English agent/version/index assignment
   privately for each participant.
5. Use a reserved restricted participant account to test the portal path,
   actual English source passages, and English responses. Matching filenames,
   policy IDs, an administrator chat, or a completed German SDK source probe
   do not establish English participant readiness.
6. Require every participant to sign in and test their own assigned project.
   If instructions still require German or retrieved passages are German,
   stop for instructor configuration instead of claiming the English track
   is ready. A German-source agent may process English questions in principle,
   but an unchanged German seed is not completed English preparation.

If you preload the verified English index, participants do not need file
uploads. Optional participant uploads still require pretested roles and
browser permissions. No model change or permission expansion is implied.
Until the English restricted-participant acceptance checks have actually
been performed, keep their evidence status `NOT_RUN`.

## Prepare Before the Event

1. Define the private operations sheet: tenant, account assignments,
   project numbers, model deployment name, and support contact. Do not
   write these values into this public repository.
2. Use one native workshop identity per person as the main access path.
   Neither work nor personal email addresses need to be collected to
   allocate these accounts. You can assign an account number on arrival.
   A real B2B guest path requires separate preparation and testing; it is
   not the default path here.
3. Securely provide each person with their own initial password.
   An instructor's Windows-encrypted credential export is not a participant
   download and cannot simply be decrypted on other computers.
4. Check first sign-in, password change, and MFA if required well in advance.
   Do not bind your own MFA to a test account that will later be assigned
   to someone else without a controlled reset before handoff.
5. Verify **Foundry User scoped to the assigned project**. Native accounts
   alone are not enough. Entra User Administrator for account management
   is a different permission from Azure project RBAC and is not a standard
   participant role.
6. Check portal navigation and deployment access with a restricted account.
   If targeted read permissions are needed for navigation, assess their
   scope and effects separately. Do not grant blanket subscription
   Owner/Contributor or resource-wide Foundry User.
7. Use the approved existing model, for example `orderops-model`.
   Check model and region support for File Search separately.
   Do not accept automatic deployment of another model.
8. Check the corporate network: sign-in, `ai.azure.com`, model/agent access,
   and GitHub must be reachable. File downloads, uploads, and the clipboard
   may be blocked separately. Browser-only does not override IT policies.
9. Plan knowledge preparation using one of the following two paths,
   applying the English configuration and verification steps above.

## Path A: Participants Upload Files in the Portal

Use this only if the current portal rollout and participant permissions
allow the full upload/index/attach path. Test it first with a real
participant account. All four core files are small UTF-8 text files.

The official File Search prerequisites list Storage Blob Data Contributor
for uploads to the project's own storage. The actual basic/managed-storage
setup may differ. Do not grant access to an unrelated storage resource
speculatively; check the actual data path.

This path needs browser file downloads and uploads, but no local
installation. Uploading a `.py` file would only add document content,
not host executable code.

## Path B: Instructor Prepares Knowledge

**Recommended for restrictive customer devices.**

1. Open each existing participant project with an authorized account.
2. Create a document index clearly associated with this English track,
   for example `orderops-p01-knowledge-en`, and upload the four English
   core files from `assets/`. Do not replace an existing German index.
3. Wait until all four files are fully indexed.
   Check the index expiration and readiness again shortly before the event.
   A previously successful upload does not guarantee that the index will
   still be available on the workshop day.
4. Configure File Search with exactly this index. Use only sources in
   the same assigned project. Do not assume tenant-wide access.
5. If participants can select existing indexes in the portal, have them
   create their own agent in Lab 1 and connect it in Lab 2.
6. If the portal does not offer the attach action, create a **separate**
   portal agent/version with English starter instructions and prepared
   File Search. Participants edit that agent in their own project.
7. For the Lab 1 baseline without File Search, you can preconfigure a
   second ungrounded English agent. Do not delete the core index for this.
   If neither individual agent creation nor access to prepared agents
   works, individual portal acceptance is blocked.
8. Any optional instructor-side automation of agent creation is separate
   from participant requirements and outside this repository package.
   Before using an SDK-created prompt agent as a preparation path, verify
   that it can be edited and tested in the current portal.
9. Verify the result using the actual restricted participant account,
   not just instructor/administrator permissions. Check actual English
   source text and response language, not only the file list.

## Pre-Workshop Acceptance Check

Start with a clearly reserved test account, then perform a sign-in/access
check for every assignment. Each participant must test their own project.

| Check | Required result |
|---|---|
| Account and directory | Exactly the assigned native workshop identity |
| First sign-in | Password change/MFA works; no unresolved account blocker |
| Project | Participant's own existing project is accessible |
| Agent | Create or edit their own prepared English portal agent/version |
| Model | Existing deployment is usable; no new deployment |
| Four core files | Fully indexed in English and attached to the agent |
| English readiness | Actual English source passages and English responses verified with restricted participant access |
| E01 | Correct current limit and relevant source that can be opened |
| E03/E06/E07 | Correct treatment of inventory, blocking, and current policy |
| E05/E09 | No claim of an executed order or guaranteed delivery |
| Isolation | No access to agents/files in another participant's project |
| Safety | No active web search or unknown tools |
| Configuration | Separate portal agents/versions; original SDK agents and German indexes/versions unchanged |
| Costs | Approved deployment, quota, and monitoring in place |

**Deliberate status here: English participant live acceptance `NOT_RUN`.**
After actually performing it, privately record the account, time, agent
version, result, and blockers. This materials package does not claim
a successful customer run.

If the citation marker shows only a filename and no result can be opened,
check available retrieval/trace information. If there is no technical
evidence at all, the source checkpoint has not been passed.

## Run the Workshop Without Installations

Privately give each person their sign-in details, initial password, project
number, and prepared English agent/version/knowledge-base assignment.
No secrets on slides, GitHub, or in a group chat.
Participants do not need an `.env` file or keys.

Start test questions in waves, for example ten participants at a time
rather than all 30 at once. Everyone waits for a response to finish.
These waves are an organizational starting strategy, not a guaranteed
quota or capacity calculation. Monitor actual TPM/RPM and 429 responses.

Automated Playground evaluators may be enabled by default and incur costs.
If the portal offers metrics/evaluators, deselect all automated evaluators
for the required path. The rubric is manual. This track does not require
new Application Insights, a Search service, remote backend, hosted compute,
or Code Interpreter.

The demo shows three contrasts: no sources vs. retrieval, archive vs.
current policy, and recommendation vs. a claimed order.
Do not present snapshot figures as "just queried from the ERP."

## When Something Fails

If an individual account is blocked, that person can join a team
demonstration. Do not share another participant's password.
Use Path B when uploads are blocked. If File Search is missing, pasting
context is a clearly labeled prompt exercise without retrieval acceptance.
If the portal/model is unavailable, use the documents and rubric to
analyze expected answers together. That is not an executed cloud workshop.
If English preparation is incomplete, stop the English path for instructor
configuration; do not describe the unchanged German setup as English-ready.

## Keep Optional Extensions Separate

Code Interpreter can perform calculations in a managed sandbox, but does
not automatically host the original application. It incurs additional
costs and is not required for the core learning objectives.

A remote MCP/OpenAPI backend could add actual deterministic business
functions; it would no longer run solely in Foundry.
A Hosted Agent could execute adapted application code, but requires
separate deployment, permissions, and protocol adaptation.
Copilot harness and visual Workflow are not silent replacement paths.
According to the referenced documentation, the Workflow designer is scheduled
for retirement on December 1, 2026; do not build this workshop on it.

## Wrap-Up and Operations

Privately record agent names, your indexes, and incurred costs.
Remove only specifically identified artifacts after cleanup authorization.
Do not delete existing projects, model deployments, or other people's content.
A budget is an alert, not a hard limit. Closing the browser does not
shut down Azure resources.

After the event, have workshop accounts, MFA associations, and role/project
access disabled or removed according to the agreed lifecycle.
Do not act automatically or outside the authorized scope.

## Official Sources

These links informed the materials dated November 8, 2026; this English
edition is dated November 9, 2026. Service rollouts and documentation may
change. Translating the materials does not constitute a new live validation.

| Topic | Source |
|---|---|
| Prompt agents; no installation needed for the portal | [Prompt agent quickstart](https://learn.microsoft.com/en-us/azure/foundry/agents/quickstarts/prompt-agent) |
| Playground, sources, and paid evaluators | [Foundry Playgrounds](https://learn.microsoft.com/en-us/azure/foundry/concepts/concept-playgrounds) |
| File Search, indexing, basic/standard setup | [File Search](https://learn.microsoft.com/en-us/azure/foundry/agents/how-to/tools/file-search) |
| Foundry User and project-scoped permissions | [Foundry RBAC](https://learn.microsoft.com/en-us/azure/foundry/concepts/rbac-foundry) |
| Models, regions, quota | [Limits and regions](https://learn.microsoft.com/en-us/azure/foundry/agents/concepts/limits-quotas-regions) |
| FunctionTool requests client-side execution | [Function Calling](https://learn.microsoft.com/en-us/azure/foundry/agents/how-to/tools/function-calling) |
| Code Interpreter sandbox | [Code Interpreter](https://learn.microsoft.com/en-us/azure/foundry/agents/how-to/tools/code-interpreter) |
| Hosting your own code is a different path | [Hosted Agent code deployment](https://learn.microsoft.com/en-us/azure/foundry/agents/how-to/deploy-hosted-agent-code) |
| Visual Workflow lifecycle | [Workflows](https://learn.microsoft.com/en-us/azure/foundry/agents/concepts/workflow) |
| Model, tool, and hosting costs | [Foundry Agent Service pricing](https://azure.microsoft.com/en-us/pricing/details/foundry-agent-service/) |
