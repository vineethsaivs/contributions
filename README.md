# Open-source contributions

_Vineeth Sai · [@vineethsaivs](https://github.com/vineethsaivs) · auto-updated after every contribution · last updated October 26, 2026 at 1:30 PM PT_

| PRs | Merged | Open | Merge rate | Projects | Streak |
|:--:|:--:|:--:|:--:|:--:|:--:|
| **468** | **209** | **194** | **76%** | **42** | **137 days** |

_1561 GitHub contributions in the last year · 64 in the last 7 days · 318 in the last 30._

## Bug reports

- [flax #5594](https://github.com/google/flax/issues/5594): nnx.GRUCell is missing the b_hn bias that its docstring and linen.GRUCell both specify.
- [trl #7221](https://github.com/huggingface/trl/issues/7221): Reproduced NaN entropy for valid zero-probability tokens, including finite float16 inputs; PyTorch categorical entropy remains finite.

## Recent activity

| Date | Project | What | Status |
|---|---|---|---|
| 2026-10-26 | [unsloth #15389](https://github.com/unslothai/unsloth/pull/15389) | Studio answered 500 instead of 422 for a request integer past signed 64-bit (createdAt/updatedAt on the chat history routes and /api/prompts, offset on /api/chat/attachments, since on /api/scheduled-tasks/runs) | Open |
| 2026-10-26 | [unsloth-zoo #2117](https://github.com/unslothai/unsloth-zoo/pull/2117) | The patched PEFT LoRA forward applied only the first adapter under set_adapter(["a", "b"]), so the second adapter had no effect and received no gradient | Open |
| 2026-10-26 | [Ray #67425](https://github.com/ray-project/ray/pull/67425) | Tuner.fit() crashed in resolve_placeholders with a TypeError when a search space mixed a non-primitive option with a primitive one, e.g. tune.grid_search([Act("relu"), 5]) | Open |
| 2026-10-25 | [unsloth #15282](https://github.com/unslothai/unsloth/pull/15282) | Studio /v1/messages with a Connection model answered 500 instead of 400 for an out-of-range sampling value | Merged |
| 2026-10-25 | [Ray #67408](https://github.com/ray-project/ray/pull/67408) | HyperOptSearch returned values off the grid for tune.qrandint and tune.qlograndint (0 for qrandint(1, 10, 3), 10 for qrandint(0, 9, 5)) | Open |
| 2026-10-25 | [unsloth-zoo #2086](https://github.com/unslothai/unsloth-zoo/pull/2086) | higher_precision_softmax rewrote a softmax with a compound first argument into a TypeError (Falcon) or a SyntaxError (SLANet, SLANeXt) in the generated module | Merged |
| 2026-10-24 | [Ray #67378](https://github.com/ray-project/ray/pull/67378) | CLIReporter and JupyterNotebookReporter with sort_by_metric=True crashed with a TypeError when a terminated trial never reported the metric | Open |
| 2026-10-24 | [unsloth #15176](https://github.com/unslothai/unsloth/pull/15176) | Studio training requests accepted a random_seed outside the numpy range, which only failed in set_seed after the model had loaded | Merged |
| 2026-10-24 | [vllm #63521](https://github.com/vllm-project/vllm/pull/63521) | Draft: An unsupported endpoint-load-metrics-format header logged the Python builtin "format" instead of the format name | Open |
| 2026-10-23 | [DeepSpeed #8896](https://github.com/deepspeedai/DeepSpeed/pull/8896) | Draft: With comms profiling on, the first all_gather_object or monitored_barrier printed "wrong comm_op specified" and exited the process with status 0 | Open |
| 2026-10-23 | [unsloth #14999](https://github.com/unslothai/unsloth/pull/14999) | Studio dropped a column mapped to the system role when the advisor mapping also carried metadata | Merged |
| 2026-10-23 | [Ray #67335](https://github.com/ray-project/ray/pull/67335) | Reusing a RunConfig with callbacks for a second Tuner.fit() errored the trials, because the default callbacks were appended to the caller's list | Open |
| 2026-10-22 | [unsloth #14726](https://github.com/unslothai/unsloth/pull/14726) | Studio vision training trained the word "None" for rows with a null caption | Merged |
| 2026-10-22 | [unsloth #14725](https://github.com/unslothai/unsloth/pull/14725) | Studio API key creation accepted an out-of-range expires_in_days | Open |
| 2026-10-22 | [Ray #67280](https://github.com/ray-project/ray/pull/67280) | OptunaSearch sampled off-grid values for tune.qrandint (and could return the exclusive upper bound with q=1) | Open |
| 2026-10-22 | [unsloth-zoo #1972](https://github.com/unslothai/unsloth-zoo/pull/1972) | add_new_tokens with method="interpolation" broke or wrote wrong vectors when new_tokens held a repeated entry | Open |
| 2026-10-22 | [unsloth #14721](https://github.com/unslothai/unsloth/pull/14721) | Studio training requests accepted a NaN weight_decay | Merged |
| 2026-10-22 | [DeepSpeed #8614](https://github.com/deepspeedai/DeepSpeed/pull/8614) | Add end-to-end BF16 stage 1 tests for zero and invalid gradient norms | Open |

_Showing the 18 most recent. Open `index.html` for the full visual dashboard._

---
_Statuses are refreshed straight from the GitHub API, so this page reflects the live state of every pull request._
