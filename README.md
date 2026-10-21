# Open-source contributions

_Vineeth Sai · [@vineethsaivs](https://github.com/vineethsaivs) · auto-updated after every contribution · last updated October 21, 2026 at 9:34 AM PT_

| PRs | Merged | Open | Merge rate | Projects | Streak |
|:--:|:--:|:--:|:--:|:--:|:--:|
| **450** | **202** | **183** | **76%** | **42** | **132 days** |

_1515 GitHub contributions in the last year · 61 in the last 7 days · 350 in the last 30._

## Bug reports

- [flax #5594](https://github.com/google/flax/issues/5594): nnx.GRUCell is missing the b_hn bias that its docstring and linen.GRUCell both specify.
- [trl #7221](https://github.com/huggingface/trl/issues/7221): Reproduced NaN entropy for valid zero-probability tokens, including finite float16 inputs; PyTorch categorical entropy remains finite.

## Recent activity

| Date | Project | What | Status |
|---|---|---|---|
| 2026-10-20 | [Ray #67199](https://github.com/ray-project/ray/pull/67199) | OptunaSearch rejected tune.qlograndint because it passed a quantization step together with log=True | Open |
| 2026-10-20 | [unsloth #14380](https://github.com/unslothai/unsloth/pull/14380) | RawTextDataLoader raised on CSV text cells larger than 128 KB | Open |
| 2026-10-20 | [unsloth #14378](https://github.com/unslothai/unsloth/pull/14378) | has_internet set the process-wide socket timeout to 3 seconds and never restored it | Merged |
| 2026-10-19 | [Ray #67171](https://github.com/ray-project/ray/pull/67171) | BayesOptSearch.register_analysis paired results with the wrong configs once any trial had no results | Open |
| 2026-10-18 | [sentence-transformers #4225](https://github.com/huggingface/sentence-transformers/pull/4225) | fit() with several train objectives trained everything after the first 1/k of the run at learning rate 0 | Merged |
| 2026-10-18 | [unsloth #14150](https://github.com/unslothai/unsloth/pull/14150) | FastSentenceTransformer.get_peft_model silently ignored layers_to_transform, layers_pattern, use_rslora and modules_to_save on the fast encoder path | Merged |
| 2026-10-17 | [Ray #67137](https://github.com/ray-project/ray/pull/67137) | HyperBand could keep a trial reporting NaN and stop the best trial of its bracket | Open |
| 2026-10-17 | [unsloth #14112](https://github.com/unslothai/unsloth/pull/14112) | GRPO compute_loss filed kl, completion_length and clip_ratio metrics under the wrong train/eval bucket for eval_on_start and standalone evaluate() | Merged |
| 2026-10-17 | [tunix #2961](https://github.com/google/tunix/pull/2961) | PPO evaluation sampled with the TRAIN rollout config, ignoring the eval temperature, top_p and top_k | Open |
| 2026-10-16 | [sentence-transformers #4203](https://github.com/huggingface/sentence-transformers/pull/4203) | Pooling("cls") crashed on top of WordEmbeddings because a None cls_token_embeddings counted as present | Closed, maintainer declined the fix |
| 2026-10-16 | [vllm #62038](https://github.com/vllm-project/vllm/pull/62038) | A NaN logit_bias value was clamped to -100, silently banning that token | Open |
| 2026-10-16 | [unsloth #14021](https://github.com/unslothai/unsloth/pull/14021) | FastModel.get_peft_model raised a ValueError for finetune_last_n_layers and layers_to_transform with the default targets | Merged |
| 2026-10-16 | [Ray #67115](https://github.com/ray-project/ray/pull/67115) | MedianStoppingRule averaged a finished trial's last result into its running mean up to three times | Open |
| 2026-10-16 | [tunix #2949](https://github.com/google/tunix/pull/2949) | LogitStrategy averaged KL, task and teacher losses over padded positions, skewing the loss and metrics | Open |
| 2026-10-15 | [unsloth #13906](https://github.com/unslothai/unsloth/pull/13906) | A padded prefill on a sliding-window model (Mistral) attended one key more than the configured window | Merged |
| 2026-10-15 | [tunix #2915](https://github.com/google/tunix/pull/2915) | PeftTrainer passed the eval hook a sum of batch losses for scalar losses but a mean for weighted losses | Open |

_Showing the 16 most recent. Open `index.html` for the full visual dashboard._

---
_Statuses are refreshed straight from the GitHub API, so this page reflects the live state of every pull request._
