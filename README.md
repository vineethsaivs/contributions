# Open-source contributions

_Vineeth Sai · [@vineethsaivs](https://github.com/vineethsaivs) · auto-updated after every contribution · last updated October 23, 2026 at 2:05 PM PT_

| PRs | Merged | Open | Merge rate | Projects | Streak |
|:--:|:--:|:--:|:--:|:--:|:--:|
| **459** | **202** | **192** | **76%** | **42** | **134 days** |

_1535 GitHub contributions in the last year · 59 in the last 7 days · 345 in the last 30._

## Bug reports

- [flax #5594](https://github.com/google/flax/issues/5594): nnx.GRUCell is missing the b_hn bias that its docstring and linen.GRUCell both specify.
- [trl #7221](https://github.com/huggingface/trl/issues/7221): Reproduced NaN entropy for valid zero-probability tokens, including finite float16 inputs; PyTorch categorical entropy remains finite.

## Recent activity

| Date | Project | What | Status |
|---|---|---|---|
| 2026-10-23 | [DeepSpeed #8896](https://github.com/deepspeedai/DeepSpeed/pull/8896) | Draft: With comms profiling on, the first all_gather_object or monitored_barrier printed "wrong comm_op specified" and exited the process with status 0 | Open |
| 2026-10-23 | [unsloth #14999](https://github.com/unslothai/unsloth/pull/14999) | Studio dropped a column mapped to the system role when the advisor mapping also carried metadata | Open |
| 2026-10-23 | [Ray #67335](https://github.com/ray-project/ray/pull/67335) | Reusing a RunConfig with callbacks for a second Tuner.fit() errored the trials, because the default callbacks were appended to the caller's list | Open |
| 2026-10-22 | [unsloth #14726](https://github.com/unslothai/unsloth/pull/14726) | Studio vision training trained the word "None" for rows with a null caption | Open |
| 2026-10-22 | [unsloth #14725](https://github.com/unslothai/unsloth/pull/14725) | Studio API key creation accepted an out-of-range expires_in_days | Open |
| 2026-10-22 | [Ray #67280](https://github.com/ray-project/ray/pull/67280) | OptunaSearch sampled off-grid values for tune.qrandint (and could return the exclusive upper bound with q=1) | Open |
| 2026-10-22 | [unsloth-zoo #1972](https://github.com/unslothai/unsloth-zoo/pull/1972) | add_new_tokens with method="interpolation" broke or wrote wrong vectors when new_tokens held a repeated entry | Open |
| 2026-10-22 | [unsloth #14721](https://github.com/unslothai/unsloth/pull/14721) | Studio training requests accepted a NaN weight_decay | Open |
| 2026-10-22 | [DeepSpeed #8614](https://github.com/deepspeedai/DeepSpeed/pull/8614) | Add end-to-end BF16 stage 1 tests for zero and invalid gradient norms | Open |
| 2026-10-20 | [Ray #67199](https://github.com/ray-project/ray/pull/67199) | OptunaSearch rejected tune.qlograndint because it passed a quantization step together with log=True | Open |
| 2026-10-20 | [unsloth #14380](https://github.com/unslothai/unsloth/pull/14380) | RawTextDataLoader raised on CSV text cells larger than 128 KB | Open |
| 2026-10-20 | [unsloth #14378](https://github.com/unslothai/unsloth/pull/14378) | has_internet set the process-wide socket timeout to 3 seconds and never restored it | Merged |
| 2026-10-19 | [Ray #67171](https://github.com/ray-project/ray/pull/67171) | BayesOptSearch.register_analysis paired results with the wrong configs once any trial had no results | Open |
| 2026-10-18 | [sentence-transformers #4225](https://github.com/huggingface/sentence-transformers/pull/4225) | fit() with several train objectives trained everything after the first 1/k of the run at learning rate 0 | Merged |
| 2026-10-18 | [unsloth #14150](https://github.com/unslothai/unsloth/pull/14150) | FastSentenceTransformer.get_peft_model silently ignored layers_to_transform, layers_pattern, use_rslora and modules_to_save on the fast encoder path | Merged |
| 2026-10-17 | [Ray #67137](https://github.com/ray-project/ray/pull/67137) | HyperBand could keep a trial reporting NaN and stop the best trial of its bracket | Open |
| 2026-10-17 | [unsloth #14112](https://github.com/unslothai/unsloth/pull/14112) | GRPO compute_loss filed kl, completion_length and clip_ratio metrics under the wrong train/eval bucket for eval_on_start and standalone evaluate() | Merged |
| 2026-10-17 | [tunix #2961](https://github.com/google/tunix/pull/2961) | PPO evaluation sampled with the TRAIN rollout config, ignoring the eval temperature, top_p and top_k | Open |

_Showing the 18 most recent. Open `index.html` for the full visual dashboard._

---
_Statuses are refreshed straight from the GitHub API, so this page reflects the live state of every pull request._
