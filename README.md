# Open-source contributions

_Vineeth Sai · [@vineethsaivs](https://github.com/vineethsaivs) · auto-updated after every contribution · last updated October 13, 2026 at 10:59 AM PT_

| PRs | Merged | Open | Merge rate | Projects | Streak |
|:--:|:--:|:--:|:--:|:--:|:--:|
| **428** | **186** | **178** | **74%** | **42** | **124 days** |

_1441 GitHub contributions in the last year · 61 in the last 7 days · 465 in the last 30._

## Bug reports

- [flax #5594](https://github.com/google/flax/issues/5594): nnx.GRUCell is missing the b_hn bias that its docstring and linen.GRUCell both specify.
- [trl #7221](https://github.com/huggingface/trl/issues/7221): Reproduced NaN entropy for valid zero-probability tokens, including finite float16 inputs; PyTorch categorical entropy remains finite.

## Recent activity

| Date | Project | What | Status |
|---|---|---|---|
| 2026-10-13 | [unsloth #13643](https://github.com/unslothai/unsloth/pull/13643) | Gemma and Gemma2 fast decode returned wrong hidden states on every step for float32 models | Open |
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
| 2026-10-09 | [flax #5619](https://github.com/google/flax/pull/5619) | nnx.metrics.Average let a masked nan or inf turn the whole average into nan | Open |
| 2026-10-09 | [DeepSpeed #8793](https://github.com/deepspeedai/DeepSpeed/pull/8793) | Pipeline eval_batch crashed or hung when loss_fn returns several losses | Open |
| 2026-10-08 | [vllm #60669](https://github.com/vllm-project/vllm/pull/60669) | Olmo3 reasoning parser treats any </think> in the prompt as reasoning already ended | Open |
| 2026-10-08 | [vllm #60668](https://github.com/vllm-project/vllm/pull/60668) | Streamed /v1/completions logprobs text_offset fell short of its tokens whenever stop strings held back text | Merged |
| 2026-10-07 | [DeepSpeed #8772](https://github.com/deepspeedai/DeepSpeed/pull/8772) | Sparse gradients come out gradient_predivide_factor times the data-parallel average | Open |
| 2026-10-07 | [DeepSpeed #8771](https://github.com/deepspeedai/DeepSpeed/pull/8771) | One fp16 overflow step reset SuperOffload weights to 0 and left nan Adam moments | Open |
| 2026-10-07 | [unsloth-zoo #1618](https://github.com/unslothai/unsloth-zoo/pull/1618) | Merged export dropped the trained lora_B bias of lora_bias=True adapters | Merged |
| 2026-10-07 | [unsloth #12981](https://github.com/unslothai/unsloth/pull/12981) | Fused LoRA kernels and decode dropped lora_B's bias when lora_bias=True | Merged |

_Showing the 19 most recent. Open `index.html` for the full visual dashboard._

---
_Statuses are refreshed straight from the GitHub API, so this page reflects the live state of every pull request._
