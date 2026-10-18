# Open-source contributions

_Vineeth Sai · [@vineethsaivs](https://github.com/vineethsaivs) · auto-updated after every contribution · last updated October 18, 2026 at 11:31 AM PT_

| PRs | Merged | Open | Merge rate | Projects | Streak |
|:--:|:--:|:--:|:--:|:--:|:--:|
| **446** | **192** | **190** | **75%** | **42** | **129 days** |

_1483 GitHub contributions in the last year · 55 in the last 7 days · 364 in the last 30._

## Bug reports

- [flax #5594](https://github.com/google/flax/issues/5594): nnx.GRUCell is missing the b_hn bias that its docstring and linen.GRUCell both specify.
- [trl #7221](https://github.com/huggingface/trl/issues/7221): Reproduced NaN entropy for valid zero-probability tokens, including finite float16 inputs; PyTorch categorical entropy remains finite.

## Recent activity

| Date | Project | What | Status |
|---|---|---|---|
| 2026-10-18 | [sentence-transformers #4225](https://github.com/huggingface/sentence-transformers/pull/4225) | fit() with several train objectives trained everything after the first 1/k of the run at learning rate 0 | Open |
| 2026-10-18 | [unsloth #14150](https://github.com/unslothai/unsloth/pull/14150) | FastSentenceTransformer.get_peft_model silently ignored layers_to_transform, layers_pattern, use_rslora and modules_to_save on the fast encoder path | Open |
| 2026-10-17 | [Ray #67137](https://github.com/ray-project/ray/pull/67137) | HyperBand could keep a trial reporting NaN and stop the best trial of its bracket | Open |
| 2026-10-17 | [unsloth #14112](https://github.com/unslothai/unsloth/pull/14112) | GRPO compute_loss filed kl, completion_length and clip_ratio metrics under the wrong train/eval bucket for eval_on_start and standalone evaluate() | Open |
| 2026-10-17 | [tunix #2961](https://github.com/google/tunix/pull/2961) | PPO evaluation sampled with the TRAIN rollout config, ignoring the eval temperature, top_p and top_k | Open |
| 2026-10-16 | [sentence-transformers #4203](https://github.com/huggingface/sentence-transformers/pull/4203) | Pooling("cls") crashed on top of WordEmbeddings because a None cls_token_embeddings counted as present | Open |
| 2026-10-16 | [vllm #62038](https://github.com/vllm-project/vllm/pull/62038) | A NaN logit_bias value was clamped to -100, silently banning that token | Open |
| 2026-10-16 | [unsloth #14021](https://github.com/unslothai/unsloth/pull/14021) | FastModel.get_peft_model raised a ValueError for finetune_last_n_layers and layers_to_transform with the default targets | Open |
| 2026-10-16 | [Ray #67115](https://github.com/ray-project/ray/pull/67115) | MedianStoppingRule averaged a finished trial's last result into its running mean up to three times | Open |
| 2026-10-16 | [tunix #2949](https://github.com/google/tunix/pull/2949) | LogitStrategy averaged KL, task and teacher losses over padded positions, skewing the loss and metrics | Open |
| 2026-10-15 | [unsloth #13906](https://github.com/unslothai/unsloth/pull/13906) | A padded prefill on a sliding-window model (Mistral) attended one key more than the configured window | Open |
| 2026-10-15 | [tunix #2915](https://github.com/google/tunix/pull/2915) | PeftTrainer passed the eval hook a sum of batch losses for scalar losses but a mean for weighted losses | Open |
| 2026-10-14 | [sentence-transformers #4181](https://github.com/huggingface/sentence-transformers/pull/4181) | The nan/inf filter replaced a loss component with a value divided by optimizer steps instead of logged calls, shifting the logged mean | Merged |
| 2026-10-14 | [tunix #2880](https://github.com/google/tunix/pull/2880) | DAPOLearner appended reward_shaping to the caller's reward_fns list, so reusing the list doubled the overlong penalty | Open |
| 2026-10-14 | [unsloth #13751](https://github.com/unslothai/unsloth/pull/13751) | FastLanguageModel.get_peft_model accepted layers_pattern but never passed it to PEFT, so the argument had no effect | Merged |
| 2026-10-14 | [Ray #67013](https://github.com/ray-project/ray/pull/67013) | Repeater passed the last repeat's error flag with the group's mean score, so searchers that skip errored trials dropped a valid mean | Open |
| 2026-10-14 | [vllm #61661](https://github.com/vllm-project/vllm/pull/61661) | Generation token metrics counted tokens that were trimmed off after a stop string matched mid-step | Open |
| 2026-10-14 | [vllm #61660](https://github.com/vllm-project/vllm/pull/61660) | Completions with echo=True and max_tokens=0 reported one completion token and returned a token id that is not in the response | Open |

_Showing the 18 most recent. Open `index.html` for the full visual dashboard._

---
_Statuses are refreshed straight from the GitHub API, so this page reflects the live state of every pull request._
