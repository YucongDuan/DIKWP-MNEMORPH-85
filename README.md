# DIKWP MNEMORPH-85

**Reconstructive Memory, Cross-Carrier Continuity and Living AI Runtime**

> Storage preserves bytes. Memory reconstructs a self. A living memory must be changed by the world.

MNEMORPH-85 is a model-agnostic, offline-first memory runtime for large language models and autonomous agents. It separates:

1. **Exact archive** - source bytes, digests, dates and consent scope;
2. **Memory traces** - lossy, perspective-bound, salience-weighted transformations;
3. **Recall events** - context- and purpose-conditioned reconstructions;
4. **World actions** - reversible actions with named responsibility;
5. **Reconsolidation** - observed outcomes update traces and the continuity state;
6. **Selective forgetting** - dormancy, abstraction or authorized private deletion.

The system does not first decide whether a carrier is human, non-human, conscious or a person. Its operational object is a bounded memory worldline. `personhood_assessment`, `humanity_score` and `intrinsic_worth_score` are deliberately absent or null.

## Why this is an upgrade to current LLM memory

Many LLM memory systems extend context through cache, files, embeddings, retrieval tiers or trainable memory. Those mechanisms can preserve and retrieve information, but retrieval alone does not establish living continuity. MNEMORPH-85 adds a reconstructive layer:

```text
exact records
  -> lossy traces
  -> context-conditioned recall
  -> counter-memory
  -> one responsible action
  -> observed world effect
  -> reconsolidation
  -> revised continuity state
```

A model output is always a **proposal awaiting world effect**. It is not automatically written as memory.

## Direct run

Requires Python 3.10+ and no third-party runtime dependency.

```bash
python start_showcase.py
```

Open:

```text
http://127.0.0.1:8780
```

Or run the full CLI loop:

```bash
python run.py summary
python run.py reconstruct demo-continuity \
  "面对新的项目机会，应该继续高输出，还是保护能量？" \
  --context '{"resource_state":"limited","time":"now"}' \
  --purpose choose_next_action_without_identity_lock_in
python run.py selftest
```

## Core commands

```bash
python run.py demo --reset
python run.py ingest <carrier_id> "new observation" --trace-kind world_effect --polarity revise
python run.py reconstruct <carrier_id> "current question"
python run.py model-context <carrier_id> "query for an external LLM"
python run.py consolidate <carrier_id>
python run.py forget <carrier_id> <trace_id> --mode dormant
python run.py act <carrier_id> "one reversible action"
python run.py observe <carrier_id> <action_id> "observed result" --correction "what changed"
python run.py verify-audit
```

## Eight memory states

- `ARCHIVE_ONLY`
- `RETRIEVAL_ASSISTANT`
- `RECONSTRUCTIVE_MEMORY`
- `LIVING_MEMORY_CANDIDATE`
- `INTEGRATED_CONTINUITY`
- `ZOMBIE_REPLAY_LOOP`
- `IDENTITY_LOCK_IN`
- `MEMORY_COLONIZATION_HOLD`

States apply only to a bounded memory worldline. They are not permanent moral or personhood labels.

## Twelve non-compensable living-memory dimensions

- reconstruction rather than copy;
- context sensitivity;
- counter-trace integration;
- selective forgetting;
- self-model update;
- future action change;
- world-effect reconsolidation;
- provenance preservation;
- affected-world return;
- corrigibility;
- branch generation;
- cross-cycle continuity.

No aggregate score is emitted. High retrieval accuracy cannot compensate for absent correction, identity lock-in or silent memory writes.

## LLM adapter contract

`POST /api/model/context` produces a prompt envelope for any external model. Four rules are fixed:

1. model output is a proposal, not memory;
2. world effect is required before reconsolidation;
3. silent memory write is forbidden;
4. source lineage and counter-traces are preserved.

Network access is not required or enabled by the reference runtime.

## Research basis

The architecture is inspired by findings that memory engrams can remain linked while retaining identity, can change composition during consolidation, and can be updated or selectively forgotten rather than functioning as immutable copies. It also distinguishes reconstructive memory from engineering approaches that extend model context or add persistent neural memory.

Primary references:

- Choucry A, Nomoto M, Inokuchi K. *Engram mechanisms of memory linking and identity.* Nature Reviews Neuroscience 25, 375-392 (2024). DOI: 10.1038/s41583-024-00814-0.
- Feitosa Tomé D et al. *Dynamic and selective engrams emerge with memory consolidation.* Nature Neuroscience 27, 561-572 (2024). DOI: 10.1038/s41593-023-01551-w.
- Zaki Y, Cai DJ. *Memory engram stability and flexibility.* Neuropsychopharmacology 50, 285-293 (2025). DOI: 10.1038/s41386-024-01979-z.
- Fawcett JM et al. *Active intentional and unintentional forgetting in the laboratory and everyday life.* Nature Reviews Psychology 3, 652-664 (2024). DOI: 10.1038/s44159-024-00352-7.
- Packer C et al. *MemGPT: Towards LLMs as Operating Systems.* arXiv:2310.08560.
- Behrouz A, Zhong P, Mirrokni V. *Titans: Learning to Memorize at Test Time.* arXiv:2501.00663.

These studies motivate the design but do not prove that the reference implementation is biologically alive or phenomenally conscious.

## Boundaries

MNEMORPH-85 is:

- a reconstructive memory reference implementation;
- a model-agnostic LLM/agent memory wrapper;
- a research tool for continuity, provenance, correction and world-effect learning.

It is not:

- proof of subjective consciousness;
- a personhood classifier;
- a clinical memory treatment system;
- a biometric identity system;
- authority to impersonate a real person;
- a replacement for consent, professional responsibility or institutional authorization.

## License

Apache License 2.0. See `LICENSE` and `NOTICE`.

## Integrating an existing model

Before each model call, use `mnemorph85 model-context` or `POST /api/model/context`. The returned packet contains a reconstructed core, counter/revision traces, omissions, provenance, D/I/K/W/P and a proposal-only adapter contract. Model output does not become memory until an authorized action is executed and its world effect is observed.

## Key states

`RECONSTRUCTIVE_MEMORY`, `LIVING_MEMORY_CANDIDATE`, `ZOMBIE_REPLAY_LOOP`, `IDENTITY_LOCK_IN`, and `MEMORY_COLONIZATION_HOLD` apply to a memory worldline window, never to permanent personhood or intrinsic worth.

## Verification boundary

The reference implementation verifies reconstructive-memory mechanics in a synthetic environment. It does not establish phenomenal consciousness, biological life, identity equivalence, professional authority or production fitness.
