
# ArchSpace

[中文](README.md) | English

> Make every architecture exploration reusable knowledge for the community.

ArchSpace is an open experiment for large language model (LLM) architecture innovation. We place architecture hypotheses proposed by the community into transparent, traceable, and reproducible training and evaluation workflows, then turn successful findings, negative results, and design trade-offs into shared knowledge assets.

Each generation of open foundation models brings new architectural ideas. Yet their actual gains across a full training lifecycle, their operating boundaries, and the lessons from failed attempts are rarely reusable by the broader field. ArchSpace provides a public experimental ground: from a proposal issue on GitHub through peer review, implementation, training, evaluation, and publication of conclusions.

## What We Do

- **Open proposals**: Community members can submit architecture ideas worth validating.
- **Peer review**: A review committee assesses proposals for novelty, feasibility, and experimental rigor.
- **Full validation**: Approved proposals enter a unified workflow covering pretraining, instruction tuning, and reinforcement learning.
- **Open records**: Training and evaluation logs are continuously recorded and published through platforms such as Weights & Biases (W&B).
- **Shared knowledge**: Implementations, experiment records, and conclusions are made available whether results are positive, negative, or conditional.

## Current Proposals

ArchSpace has collected nearly ten architecture proposals, including Next Concept Prediction (NCP), Depth-Attention, SiameseNorm, Artificial Hippocampus Networks, MorphNorm, and Looped Transformers. They are awaiting validation or currently in progress.

Browse existing proposals, join discussions, or submit a new `architecture proposal` through [Issues](../../issues).

## Submit an Architecture Proposal

Open an [issue](../../issues/new/choose) using the `architecture proposal` template. Please provide:

1. **Problem and motivation**: What limitation in the current architecture or training paradigm does this address?
2. **Core design**: Describe the architectural change, key components, and differences from the baseline.
3. **Hypothesis**: Which capabilities or metrics do you expect to improve? What are the likely costs or risks?
4. **Implementation notes**: Include pseudocode, a reference implementation, or relevant paper links where possible.
5. **Validation plan**: Propose control experiments, benchmarks, and essential ablations.
6. **References**: Link papers, repositories, technical reports, or other relevant material.

Proposals should focus on implementable and testable LLM architecture innovations. Please avoid broad directions without a concrete technical design or falsifiable hypothesis.

## Proposal Lifecycle

```text
Community member proposes an architecture hypothesis
        ↓
Submit an architecture proposal issue
        ↓
Committee peer review / community discussion
        ↓
Approved → Fork and implement on a branch → Incremental implementation and experiments
         → Submit / update a PR → Maintainer merge
Not approved → Close the issue while retaining review comments
```

Issues and pull requests use the following status labels:


| Label                   | Meaning                                                                   |
| ------------------------- | --------------------------------------------------------------------------- |
| `architecture proposal` | An architecture innovation proposal                                       |
| `under review`          | Under committee review or community discussion                            |
| `in-progress`           | Approved and under implementation or experimentation                      |
| `done`                  | Implementation, validation, or conclusion is complete                     |
| `declined`              | Not entering validation at this time; review comments remain in the issue |

## Review Committee

The review committee brings together experts from academia and industry, including Professor Qi Zhang of Fudan University, Associate Professor Zhouhan Lin of Shanghai Jiao Tong University, and Young Researcher XXX of the Shanghai Artificial Intelligence Laboratory, among others.

The committee reviews community proposals through peer review, with particular attention to:

- The research value and clarity of the problem definition;
- Technical feasibility, including reasonable resource and engineering requirements;
- Whether the experimental design can test the hypothesis through appropriate baselines, evaluations, and ablations;
- Whether expected benefits, operating boundaries, and risks are clearly articulated.

The committee selects proposals that merit public validation; it does not replace community discussion. Proposal discussions, states, and review outcomes will be retained on GitHub whenever possible for traceability and reuse.

## Validation Workflow

Approved proposals are validated using a full training workflow aligned with the fully open [Olmo 3](https://arxiv.org/abs/2512.13961) model flow:

- **Model sizes**: 1B, 3B, and 8B;
- **Training stages**: pretraining, instruction tuning, and reinforcement learning;
- **Training scale**: approximately 6T tokens across the full workflow;
- **Process records**: training and evaluation logs are recorded and published on W&B;
- **Outputs**: implementations, configurations, metrics, experiment records, and conclusions, including architecture trade-offs and operating conditions where possible.

We value negative results. An architecture attempt that does not deliver the expected gain is still valuable when it has been clearly and rigorously validated, because it helps the community avoid redundant trial and error.

## How to Contribute

You can participate in ArchSpace by:

1. Submitting or discussing architecture proposals in Issues.
2. Contributing implementations, tests, evaluations, or documentation for approved proposals.
3. Sending pull requests with incremental implementations and experiment updates.
4. Helping reproduce, review, or interpret public experimental results.
5. Sharing relevant papers, code, data, or engineering experience.

Before opening a pull request, describe the related issue, the scope of the change, how to run it, and current experimental results. Please do not submit large, difficult-to-review refactors without prior discussion.

## References

- [Next Concept Prediction in Discrete Latent Space Leads to Stronger Language Models](https://arxiv.org/abs/2602.08984)
- [Olmo 3](https://arxiv.org/abs/2512.13961)
- [Keynote Address at the Opening Ceremony of the 2026 World Artificial Intelligence Conference and High-level Meeting on Global AI Governance](https://www.news.cn/politics/leaders/20260717/72728b6f94154d63b3eaaaf9808b51eb/c.html)

## Contact and Discussion

Please use GitHub Issues for public discussion whenever possible. Discuss proposal-specific questions in the corresponding issue so that the conversation and conclusions remain fully documented.
