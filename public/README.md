# Open-source contributions

_Vineeth Sai · [@vineethsaivs](https://github.com/vineethsaivs) · auto-updated after every contribution · last updated November 18, 2026 at 9:30 PM PT_

| PRs | Merged | Open | Merge rate | Projects | Streak |
|:--:|:--:|:--:|:--:|:--:|:--:|
| **555** | **262** | **220** | **78%** | **42** | **160 days** |

_2033 GitHub contributions in the last year · 139 in the last 7 days · 439 in the last 30._

## Bug reports

- [peft #4115](https://github.com/huggingface/peft/issues/4115): C3ALinear.forward rebinds x to each adapter's output, so with more than one active adapter the second one convolves the first one's result instead of the layer input.
- [peft #4094](https://github.com/huggingface/peft/issues/4094): reduce_intruder_dimension does not transpose the delta weight for fan_in_fan_out (GPT-2 Conv1D) or nn.Embedding LoRA layers, so the rebuilt adapter is wrong.
- [flax #5594](https://github.com/google/flax/issues/5594): nnx.GRUCell is missing the b_hn bias that its docstring and linen.GRUCell both specify.
- [trl #7221](https://github.com/huggingface/trl/issues/7221): Reproduced NaN entropy for valid zero-probability tokens, including finite float16 inputs; PyTorch categorical entropy remains finite.

## Recent activity

| Date | Project | What | Status |
|---|---|---|---|
| 2026-11-18 | [litellm #52736](https://github.com/BerriAI/litellm/pull/52736) | Latency-based routing kept sending streaming and sync requests to a deployment that times out on every call, because the timeout penalty only reached the non-streaming latency list and only fired from the async failure hook. | Open |
| 2026-11-18 | [vllm #68547](https://github.com/vllm-project/vllm/pull/68547) | With gpt-oss on the Responses API, a built-in tool call cut off by max_output_tokens or a stop string was still executed on its truncated input, another turn started, and the response reported completed. | Open |
| 2026-11-18 | [flax #5654](https://github.com/google/flax/pull/5654) | nnx.BatchNorm with bf16 or fp16 compute cast its float32 running statistics to the half dtype in eval, so eval drifted from training and an fp16 variance above 65504 collapsed its channel to the bias. | Open |
| 2026-11-18 | [Ray #68314](https://github.com/ray-project/ray/pull/68314) | Result.get_best_checkpoint returned a NaN-scored checkpoint as the best one, in Ray Tune and in Ray Train V2, whenever a run diverged and num_to_keep was left at its default. | Open |
| 2026-11-18 | [pytorch-lightning #22197](https://github.com/Lightning-AI/pytorch-lightning/pull/22197) | Resuming from a mid-epoch checkpoint silently skipped one batch whenever the stateful train dataloader had no length (torchdata StatefulDataLoader over an IterableDataset, HF streaming datasets). | Open |
| 2026-11-17 | [Ray #68261](https://github.com/ray-project/ray/pull/68261) | A PBT trial retried under max_failures lost its PBT state, so synchronous PBT exploited at mismatched steps and could overwrite the best trial with a worse one. | Open |
| 2026-11-17 | [unsloth #18213](https://github.com/unslothai/unsloth/pull/18213) | On transformers >= 4.48 the LongRoPE rotary was never installed, so llama-type Phi-3.5 used short factors at every length; cos/sin were up to 2.38 off past 4096 tokens in training and decode. | Merged |
| 2026-11-17 | [unsloth-zoo #2579](https://github.com/unslothai/unsloth-zoo/pull/2579) | prepare_model_for_training froze PEFT trainable_token_indices deltas, so the chosen token rows never trained on either loader path. | Merged |
| 2026-11-16 | [tunix #3372](https://github.com/google/tunix/pull/3372) | Agentic GRPO advantages now ignore overlong-filtered, timed out and non-finite-reward rollouts, per group, matching the distributed path. | Open |
| 2026-11-16 | [flax #5653](https://github.com/google/flax/pull/5653) | nn.Fp8DotGeneral (Fp8DirectDotGeneralOp) and nn.Fp8Einsum now quantize with their configured e4m3_dtype and e5m2_dtype instead of hardcoded OCP formats. | Open |
| 2026-11-16 | [optax #1892](https://github.com/google-deepmind/optax/pull/1892) | contrib.scale_by_muon(adaptive=True) now scales each matrix in a stacked leaf by its own dual norm <G_l, O_l> instead of the sum over all matrices. | Open |
| 2026-11-16 | [pytorch-lightning #22193](https://github.com/Lightning-AI/pytorch-lightning/pull/22193) | An epoch-interval ReduceLROnPlateau now steps at the end of an epoch resumed from a mid-epoch checkpoint when its monitor was logged again in that run. | Open |
| 2026-11-16 | [Ray #68198](https://github.com/ray-project/ray/pull/68198) | TuneController no longer rewraps a TuneError raised by a result or error handler into a new TuneError holding a traceback string. | Open |
| 2026-11-16 | [unsloth-zoo #2553](https://github.com/unslothai/unsloth-zoo/pull/2553) | unsloth_train now steps the LR scheduler only when the fp16 GradScaler actually ran the optimizer. | Merged |
| 2026-11-16 | [unsloth #17940](https://github.com/unslothai/unsloth/pull/17940) | Cohere fast attention forward and decode now apply q_norm/k_norm on (batch, seq, heads, head_dim) before the head transpose. | Merged |
| 2026-11-15 | [flax #5651](https://github.com/google/flax/pull/5651) | nnx.SimpleCell no longer forces dtype=float32; it infers from inputs and params like the other cells and linen. | Open |
| 2026-11-15 | [unsloth-zoo #2518](https://github.com/unslothai/unsloth-zoo/pull/2518) | sft_prepare_dataset now cuts prompt/completion rows by truncation_mode and treats max_length=None as no limit, like messages rows. | Merged |
| 2026-11-15 | [unsloth #17810](https://github.com/unslothai/unsloth/pull/17810) | FastSentenceTransformer.get_peft_model (fast encoder path) now forwards exclude_modules, lora_bias, rank_pattern and every other LoraConfig kwarg, and refuses aLoRA. | Merged |

_Showing the 18 most recent. Open `index.html` for the full visual dashboard._

---
_Statuses are refreshed straight from the GitHub API, so this page reflects the live state of every pull request._
