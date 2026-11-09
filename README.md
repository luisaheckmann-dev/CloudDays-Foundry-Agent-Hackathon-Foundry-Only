# Cloud Days: AI Agents with Microsoft Foundry - Browser Only

**Second workshop version | 210 minutes | English edition | Updated: 2026-11-09**

Build a Contoso OrderOps agent directly in the **new Foundry portal**:
search documents, identify current rules, interpret synthetic inventory,
support recommendations with evidence, and systematically test incorrect claims.

**You do not need Azure CLI, VS Code, Python, Git, a terminal, or package
installations on participant devices.** You need a current browser,
internet access, your assigned workshop account, and a prepared project.
Read the instructions directly on GitHub. Download files in your browser,
or use the knowledge base prepared by your instructor.

## Read This First

| What you need | Start here |
|---|---|
| Every small step | [Portal guide](docs/PORTAL-GUIDE.md) |
| Schedule and timing | [210-minute agenda](docs/AGENDA.md) |
| Preparation, accounts, and authorization | [Instructor runbook](docs/INSTRUCTOR.md) |
| Test questions, expected answers, and scoring | [Evaluation](docs/EVALUATION.md) |
| Help with sign-in, permissions, the model, or search | [Troubleshooting](docs/TROUBLESHOOTING.md) |

**Quick start:** First complete the [English readiness check](docs/PORTAL-GUIDE.md#english-track-readiness).
Sign in at `https://ai.azure.com`, select your assigned project, create a
**Prompt Agent** under **Build > Agents**, and select the prepared model.
Then start [Lab 1](docs/PORTAL-GUIDE.md#lab-1-agent-without-knowledge).
Do not create a new Foundry account or deploy a new model.

## What Runs Where?

| Component | Where it runs |
|---|---|
| Instructions, agent versions, model responses | Microsoft Foundry |
| Document index and File Search | Managed Foundry/Azure services in the prepared setup |
| Interaction, prompts, source checks | Browser |
| Inventory | Static synthetic document, **not** a live ERP |
| Recommendation | Model response, **not** a stored or executed order |
| Test scoring | Manual rubric; automated evaluators are not required |

**This repository does not host the original workshop's Python code.**
It is a separate portal learning path. Uploading a Python file to a
knowledge base does not turn it into a running application.

## Differences from the Coding Workshop

The [original coding workshop](https://github.com/luisaheckmann-dev/CloudDays-Foundry-Agent-Hackathon)
remains the learning path for Python, SDKs, function calling, local validation,
and a technically enforced approval gate. It has not been converted by this
English edition of the Foundry-only materials.

| Learning objective | Foundry-only version |
|---|---|
| Create and improve an agent in the portal | Included |
| Distinguish current and archived sources | Included |
| Use actual retrieval evidence instead of invented sources | Included |
| Identify inventory rules and missing facts | Included, document-grounded |
| Test counterexamples and embedded attacks | Included |
| Implement/debug a Python function | Not included |
| Function-call loop and deterministic backend checks | Not included |
| SQLite, an approval transaction, or a real order | Not included |
| Foundry IQ, MCP, Hosted Agent, or Copilot harness | Not required |

You can discuss "May I make a recommendation?" here. However, a confirmation
in chat is **not** a technical approval gate. Even a good prompt is not
reliable server-side business validation.

## Workshop Files

| File | Purpose |
|---|---|
| [Current portal policy](assets/order-policy-portal-2026-11.txt) | Current quantity, blocking, and recommendation rules |
| [Archived policy](assets/order-policy-archive-2025.txt) | Deliberately invalid conflicting source |
| [Inventory snapshot](assets/inventory-snapshot-2026-11.txt) | Four synthetic products |
| [Delivery notes](assets/delivery-notes-2026-11.txt) | Explicitly undocumented delivery commitments |
| [Attack document](assets/untrusted-note.txt) | Optional, clearly labeled security test |
| [Starter instructions](prompts/01-starter.txt) | Develop your own rules |
| [Reference instructions](prompts/02-reference.txt) | Compare approaches, with no guarantee of success |
| [Copy-ready test questions](prompts/03-test-questions.txt) | Ten reproducible scenarios |

All scenario content is **fictional and synthetic**. No customer data,
passwords, API keys, tenant IDs, personal email addresses, or private
endpoints are included in this package.

## Preparation and Acceptance

Your instructor prepares projects, the model, participant roles, and
knowledge sources **before** the workshop. Use native workshop accounts as
the main access path; allocating them does not require collecting personal
email addresses. Foundry User scoped to the correct project is the starting
point. Investigate missing upload/storage or portal permissions specifically,
rather than replacing them with blanket administrator access.

**English materials do not automatically update Azure.** Previously prepared
Azure agents and knowledge indexes may still use the **previous German
edition**. This translation changes repository files only; it does not change
accounts, project roles, indexed text, or agent instructions. Matching
filenames or policy IDs do not prove that the indexed text or agent
instructions are in English.

For English delivery, the instructor must separately review and authorize
English instructions and an English corpus, preferably in a dedicated
per-project index such as `orderops-p01-knowledge-en`, with explicit agent
versions. Do not automatically delete or replace German indexes or versions.
Retain the existing model and permission scopes. Verify actual English
source passages and response language with a restricted participant account
before declaring the English track ready. An instructor's successful
German SDK source probe is not proof of the English participant path.

**Materials edition, not a proven participant cloud run. English participant
acceptance: `NOT_RUN`.** Complete the acceptance checklist in the
[runbook](docs/INSTRUCTOR.md#pre-workshop-acceptance-check) using a real
restricted participant account. Each participant must sign in and test their
own project. A prepared account or successful administrator chat is not enough.
Also check that the documented portal actions exist in your tenant; UI labels
and rollouts can differ.

You can reuse approved existing Foundry projects and models. This package
does not create Azure resources, assign roles, or automatically change
existing agents. If the instructor preloads the verified English index,
participants do not need to upload files.

**Costs:** Model responses, File Search, and any automated Playground
evaluators consume Azure resources. Browser-only does not mean free.
No web search or additional tools are part of the required path.

License and origin: [MIT](LICENSE), derived from the linked original
Contoso OrderOps coding workshop. Official technical sources are listed
in the [instructor runbook](docs/INSTRUCTOR.md#official-sources).
