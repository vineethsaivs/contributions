# Open-source contributions

_Vineeth Sai · [@vineethsaivs](https://github.com/vineethsaivs) · auto-updated after every contribution · last updated October 24, 2026 at 8:30 PM PT_

| PRs | Merged | Open | Merge rate | Projects | Streak |
|:--:|:--:|:--:|:--:|:--:|:--:|
| **462** | **203** | **194** | **76%** | **42** | **135 days** |

_1544 GitHub contributions in the last year · 67 in the last 7 days · 346 in the last 30._

## Bug reports

- [flax #5594](https://github.com/google/flax/issues/5594): nnx.GRUCell is missing the b_hn bias that its docstring and linen.GRUCell both specify.
- [trl #7221](https://github.com/huggingface/trl/issues/7221): Reproduced NaN entropy for valid zero-probability tokens, including finite float16 inputs; PyTorch categorical entropy remains finite.

## Recent activity

| Date | Project | What | Status |
|---|---|---|---|
| 2026-10-24 | [Ray #67378](https://github.com/ray-project/ray/pull/67378) | CLIReporter and JupyterNotebookReporter with sort_by_metric=True crashed with a TypeError when a terminated trial never reported the metric | Open |
| 2026-10-24 | [unsloth #15176](https://github.com/unslothai/unsloth/pull/15176) | Studio training requests accepted a random_seed outside the numpy range, which only failed in set_seed after the model had loaded | Open |
| 2026-10-24 | [vllm #63521](https://github.com/vllm-project/vllm/pull/63521) | Draft: An unsupported endpoint-load-metrics-format header logged the Python builtin "format" instead of the format name | Open |
| 2026-10-23 | [DeepSpeed #8896](https://github.com/deepspeedai/DeepSpeed/pull/8896) | Draft: With comms profiling on, the first all_gather_object or monitored_barrier printed "wrong comm_op specified" and exited the process with status 0 | Open |
| 2026-10-23 | [unsloth #14999](https://github.com/unslothai/unsloth/pull/14999) | Studio dropped a column mapped to the system role when the advisor mapping also carried metadata | Open |
| 2026-10-23 | [Ray #67335](https://github.com/ray-project/ray/pull/67335) | Reusing a RunConfig with callbacks for a second Tuner.fit() errored the trials, because the default callbacks were appended to the caller's list | Open |
| 2026-10-22 | [unsloth #14726](https://github.com/unslothai/unsloth/pull/14726) | Studio vision training trained the word "None" for rows with a null caption | Merged |
| 2026-10-22 | [unsloth #14725](https://github.com/unslothai/unsloth/pull/14725) | Studio API key creation accepted an out-of-range expires_in_days | Open |
| 2026-10-22 | [Ray #67280](https://github.com/ray-project/ray/pull/67280) | OptunaSearch sampled off-grid values for tune.qrandint (and could return the exclusive upper bound with q=1) | Open |
| 2026-10-22 | [unsloth-zoo #1972](https://github.com/unslothai/unsloth-zoo/pull/1972) | add_new_tokens with method="interpolation" broke or wrote wrong vectors when new_tokens held a repeated entry | Open |
| 2026-10-22 | [unsloth #14721](https://github.com/unslothai/unsloth/pull/14721) | Studio training requests accepted a NaN weight_decay | Open |
| 2026-10-22 | [DeepSpeed #8614](https://github.com/deepspeedai/DeepSpeed/pull/8614) | Add end-to-end BF16 stage 1 tests for zero and invalid gradient norms | Open |
| 2026-10-20 | [Ray #67199](https://github.com/ray-project/ray/pull/67199) | OptunaSearch rejected tune.qlograndint because it passed a quantization step together with log=True | Open |
| 2026-10-20 | [unsloth #14380](https://github.com/unslothai/unsloth/pull/14380) | RawTextDataLoader raised on CSV text cells larger than 128 KB | Open |
| 2026-10-20 | [unsloth #14378](https://github.com/unslothai/unsloth/pull/14378) | has_internet set the process-wide socket timeout to 3 seconds and never restored it | Merged |
| 2026-10-19 | [Ray #67171](https://github.com/ray-project/ray/pull/67171) | BayesOptSearch.register_analysis paired results with the wrong configs once any trial had no results | Open |

_Showing the 16 most recent. Open `index.html` for the full visual dashboard._

---
_Statuses are refreshed straight from the GitHub API, so this page reflects the live state of every pull request._
