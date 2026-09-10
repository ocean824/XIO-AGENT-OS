# ØMEGA Runtime Integration — XIO Under-the-Hood Intelligence

## Canonical relationship

XIO is an application/operating environment built **on top of ØMEGA**. XIO does not replace ØMEGA and must not duplicate ØMEGA's mature agent-harness capabilities.

Canonical upstream repository:
`ocean824/XYRASYSTEMS---OMEGA-AI` (default branch currently `master`).

Before materially implementing XIO BRAIN, SWARM, FORGE, FLOW, model routing, agent roles, tools, memory, browser/desktop control, or orchestration, planners must inspect the relevant canonical ØMEGA documents and reconcile XIO requirements against them.

## ØMEGA has two distinct meanings that coexist

### 1. ØMEGA MODEL
A locally/self-hosted foundation/model layer owned and controlled by Ø. Long-term ambition: frontier-class general intelligence comparable in practical usefulness to strong Qwen/Kimi-class open models for reasoning, coding, tool use, long context and agentic work.

The model may begin as a selected open-weight base model plus ØMEGA-specific post-training, fine-tuning/adapters, tool-use training, retrieval/memory integration and evaluation rather than training a frontier model from random initialization. The architecture must allow progressively replacing the underlying base weights with increasingly capable ØMEGA-owned/customized checkpoints.

Local means self-hostable/private and controlled by Ø; it does not require inference to occur physically on the laptop. ØMEGA may run on Ø's workstation, owned/rented GPU infrastructure, or ProjectX-style cloud GPU computers while remaining the local/private model path from the application's perspective.

### 2. ØMEGA RUNTIME / HARNESS
The large existing ØMEGA repository's orchestration, agents, prompts, skills, tools, memory, browser/desktop, model routing, governance and execution architecture.

XIO consumes this runtime as its native intelligence substrate.

Therefore:

```text
XIO APPLICATIONS / UI / BUSINESS CAPABILITIES
                 |
              ØMEGA SDK
                 |
+----------------+----------------+
| ØMEGA HARNESS / RUNTIME          |
| agents, swarm, tools, memory,    |
| context, routing, XYRA, browser, |
| execution, review, skills        |
+----------------+----------------+
                 |
        MODEL ROUTER / INFERENCE
          /              \
  ØMEGA LOCAL MODEL    OPTIONAL EXTERNAL MODELS
  preferred native     Codex/Qwen/etc by policy
```

## Model policy

- ØMEGA Local is the preferred sovereign/native intelligence path when capability is sufficient.
- XIO/ØMEGA remain model-agnostic so a role can use a stronger/specialized external or local model when configured.
- Planner/Reviewer/Implementer/etc. are **roles**, not model names.
- Role defaults can point to ØMEGA Local or another provider/model.
- Per-workspace/project/Epic/ticket/run overrides remain possible.
- Sensitive/private workflows can enforce local-only model policy.
- Evals decide whether ØMEGA Local meets the quality gate for a role before it becomes default there.

## Training / improvement architecture

ØMEGA MODEL program should support:
1. base-model evaluation/selection;
2. tokenizer/context/tool compatibility analysis;
3. supervised fine-tuning / LoRA/QLoRA where appropriate;
4. preference/reasoning/tool-use post-training where feasible;
5. coding and structured-tool datasets;
6. domain datasets derived from authorized ØMEGA/XIO workflows;
7. synthetic data with quality filters;
8. distillation where licensing/rights permit;
9. eval suites for coding, planning, tool use, retrieval, long-context, agent handoffs, safety/security and domain tasks;
10. checkpoint registry/versioning;
11. quantization/inference profiles;
12. distributed/high-GPU training/inference profiles;
13. regression gates before model promotion.

Do not equate 'custom model' with merely changing a system prompt. ØMEGA MODEL is a real model/checkpoint program, while ØMEGA HARNESS supplies tools/context/memory around it.

## Compute profiles

- LAPTOP: quantized smaller checkpoint, routing/control, local development.
- WORKSTATION: larger quantized/full local inference and adapter training.
- RENTED_GPU: ProjectX/cloud GPU for large-model inference, fine-tuning, eval batches, data generation and heavy builds.
- CLUSTER: future distributed training/inference.

Compute provider remains replaceable. Model artifacts/checkpoints/config/evals remain portable.

## Cross-repo reconciliation rules

1. ØMEGA repo owns generic intelligence-runtime primitives.
2. XIO repo owns Founder OS/application/product behavior.
3. XIO FORGE owns the XIO-facing software-factory experience; generic agent/runtime primitives should call/reuse ØMEGA rather than fork them.
4. If XIO needs a generic capability missing from ØMEGA, propose it upstream in ØMEGA and expose it through an SDK/API; avoid permanent duplicated implementations.
5. XIO-specific business agents may be defined in XIO but execute on ØMEGA Runtime.
6. XIO may use external models/providers through ØMEGA's router without changing its product architecture.
7. Version the ØMEGA SDK/runtime contract so XIO, ATLAS, LEVIATHAN, SONARA, AXIOM and future apps can pin compatible releases.

## XIO role

XIO is one flagship application of ØMEGA, not the container that defines all ØMEGA capability. Other applications can consume ØMEGA independently.
