# Open-source contributions

_Vineeth Sai · [@vineethsaivs](https://github.com/vineethsaivs) · auto-updated after every contribution · last updated October 15, 2026 at 11:14 AM PT_

| PRs | Merged | Open | Merge rate | Projects | Streak |
|:--:|:--:|:--:|:--:|:--:|:--:|
| **436** | **187** | **185** | **75%** | **42** | **126 days** |

_1459 GitHub contributions in the last year · 55 in the last 7 days · 390 in the last 30._

## Bug reports

- [flax #5594](https://github.com/google/flax/issues/5594): nnx.GRUCell is missing the b_hn bias that its docstring and linen.GRUCell both specify.
- [trl #7221](https://github.com/huggingface/trl/issues/7221): Reproduced NaN entropy for valid zero-probability tokens, including finite float16 inputs; PyTorch categorical entropy remains finite.

## Recent activity

| Date | Project | What | Status |
|---|---|---|---|
| 2026-10-15 | [unsloth #13906](https://github.com/unslothai/unsloth/pull/13906) | A padded prefill on a sliding-window model (Mistral) attended one key more than the configured window | Open |
| 2026-10-15 | [tunix #2915](https://github.com/google/tunix/pull/2915) | PeftTrainer passed the eval hook a sum of batch losses for scalar losses but a mean for weighted losses | Open |
| 2026-10-14 | [sentence-transformers #4181](https://github.com/huggingface/sentence-transformers/pull/4181) | The nan/inf filter replaced a loss component with a value divided by optimizer steps instead of logged calls, shifting the logged mean | Open |
| 2026-10-14 | [tunix #2880](https://github.com/google/tunix/pull/2880) | DAPOLearner appended reward_shaping to the caller's reward_fns list, so reusing the list doubled the overlong penalty | Open |
| 2026-10-14 | [unsloth #13751](https://github.com/unslothai/unsloth/pull/13751) | FastLanguageModel.get_peft_model accepted layers_pattern but never passed it to PEFT, so the argument had no effect | Open |
| 2026-10-14 | [Ray #67013](https://github.com/ray-project/ray/pull/67013) | Repeater passed the last repeat's error flag with the group's mean score, so searchers that skip errored trials dropped a valid mean | Open |
| 2026-10-14 | [vllm #61661](https://github.com/vllm-project/vllm/pull/61661) | Generation token metrics counted tokens that were trimmed off after a stop string matched mid-step | Open |
| 2026-10-14 | [vllm #61660](https://github.com/vllm-project/vllm/pull/61660) | Completions with echo=True and max_tokens=0 reported one completion token and returned a token id that is not in the response | Open |
| 2026-10-13 | [unsloth #13643](https://github.com/unslothai/unsloth/pull/13643) | Gemma and Gemma2 fast decode returned wrong hidden states on every step for float32 models | Merged |
| 2026-10-12 | [tunix #2827](https://github.com/google/tunix/pull/2827) | Agentic GRPO reward and metric fns scored only the first assistant message of each multi-turn trajectory | Open |
| 2026-10-12 | [unsloth #13454](https://github.com/unslothai/unsloth/pull/13454) | Granite fast decode summed the normed hidden states into the residual because the residual aliased an in-place norm | Open |
| 2026-10-12 | [Ray #66939](https://github.com/ray-project/ray/pull/66939) | With mode="max", a trial that had not reported the metric yet was ranked as the top job and given the free resources | Open |
| 2026-10-11 | [unsloth #13335](https://github.com/unslothai/unsloth/pull/13335) | DiffusionTrainer always raised for an SFTConfig because to_dict() masked eos_token and pad_token | Merged |
| 2026-10-11 | [Ray #66923](https://github.com/ray-project/ray/pull/66923) | CombinedStopper stopped calling later stoppers once one returned True, starving stateful stoppers of results | Open |
| 2026-10-11 | [tunix #2819](https://github.com/google/tunix/pull/2819) | PPO built its reward tensor with the completion ids int dtype, truncating every score toward zero | Open |
| 2026-10-10 | [tunix #2809](https://github.com/google/tunix/pull/2809) | ORPO SFT term scored the first prompt token of every left-padded row from a pad position | Open |
| 2026-10-10 | [unsloth #13254](https://github.com/unslothai/unsloth/pull/13254) | Fused LoRA kernels ran on a DoRA adapter activated after get_peft_model, dropping its magnitude | Merged |
| 2026-10-10 | [DeepSpeed #8804](https://github.com/deepspeedai/DeepSpeed/pull/8804) | WarmupLR, WarmupDecayLR and WarmupCosineLR rejected warmup_num_steps=0, crashing HF Trainer runs with no warmup | Open |
| 2026-10-10 | [Ray #66919](https://github.com/ray-project/ray/pull/66919) | PB2 truncated GP suggestions for integer hyperparameters instead of rounding | Open |

_Showing the 19 most recent. Open `index.html` for the full visual dashboard._

---
_Statuses are refreshed straight from the GitHub API, so this page reflects the live state of every pull request._
