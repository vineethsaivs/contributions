# Open-source contributions

_Vineeth Sai · [@vineethsaivs](https://github.com/vineethsaivs) · auto-updated after every contribution · last updated November 21, 2026 at 4:17 PM PT_

| PRs | Merged | Open | Merge rate | Projects | Streak |
|:--:|:--:|:--:|:--:|:--:|:--:|
| **564** | **264** | **227** | **78%** | **42** | **163 days** |

_2128 GitHub contributions in the last year · 187 in the last 7 days · 505 in the last 30._

## Bug reports

- [peft #4115](https://github.com/huggingface/peft/issues/4115): C3ALinear.forward rebinds x to each adapter's output, so with more than one active adapter the second one convolves the first one's result instead of the layer input.
- [peft #4094](https://github.com/huggingface/peft/issues/4094): reduce_intruder_dimension does not transpose the delta weight for fan_in_fan_out (GPT-2 Conv1D) or nn.Embedding LoRA layers, so the rebuilt adapter is wrong.
- [flax #5594](https://github.com/google/flax/issues/5594): nnx.GRUCell is missing the b_hn bias that its docstring and linen.GRUCell both specify.
- [trl #7221](https://github.com/huggingface/trl/issues/7221): Reproduced NaN entropy for valid zero-probability tokens, including finite float16 inputs; PyTorch categorical entropy remains finite.

## Recent activity

| Date | Project | What | Status |
|---|---|---|---|
| 2026-11-21 | [unsloth #18818](https://github.com/unslothai/unsloth/pull/18818) | GemmaFixedRotaryEmbedding now applies the linear RoPE scaling the loader writes when max_seq_length passes Gemma's native window, in the eager table and the compiled path. | Open |
| 2026-11-21 | [tunix #3449](https://github.com/google/tunix/pull/3449) | Re-snapshot the old-policy anchor at sampling time for SHARED weight placement, so trainer-side old logps use the weights that sampled. | Open |
| 2026-11-21 | [pytorch-lightning #22208](https://github.com/Lightning-AI/pytorch-lightning/pull/22208) | Wrap the model in DDP again when BaseFinetuning changes requires_grad, so parameters unfrozen mid-training get all-reduced and the replicas stay in sync. | Open |
| 2026-11-20 | [unsloth-zoo #2636](https://github.com/unslothai/unsloth-zoo/pull/2636) | merged_16bit, push_to_hub_merged and GGUF exports wrote the base checkpoint's RoPE config next to weights trained with rope_scaling, so the reloaded model differed from the trained one. | Open |
| 2026-11-20 | [unsloth #18650](https://github.com/unslothai/unsloth/pull/18650) | Unsloth Studio vision training gave a separate eval split a different user prompt than train, and the seeded max_steps shuffle picked the training prompt. | Open |
| 2026-11-20 | [pytorch-lightning #22203](https://github.com/Lightning-AI/pytorch-lightning/pull/22203) | With every_n_train_steps and a validation monitor, a step checkpoint saved right before validation was scored with the previous validation's metric, so the wrong checkpoint was kept as best. | Open |
| 2026-11-19 | [Ray #68354](https://github.com/ray-project/ray/pull/68354) | With HyperBandScheduler, search algorithms never saw the final metrics of trials stopped while PAUSED, so HyperOpt treated the 2nd and 3rd best trials as the worst points and Optuna marked full-length trials as pruned. | Open |
| 2026-11-19 | [flax #5655](https://github.com/google/flax/pull/5655) | nnx.MultiHeadAttention autoregressive decode with the RoPE attention function produced wrong outputs from the second token on, with no workaround. | Open |
| 2026-11-19 | [pytorch-lightning #22202](https://github.com/Lightning-AI/pytorch-lightning/pull/22202) | Since Lightning 2.5.0, a run resumed from a mid-epoch checkpoint silently lost its GradientAccumulationScheduler factor for the rest of the epoch and ran StochasticWeightAveraging one epoch late, and a second resume restarted the SWA average. | Open |
| 2026-11-18 | [litellm #52736](https://github.com/BerriAI/litellm/pull/52736) | Latency-based routing kept sending streaming and sync requests to a deployment that times out on every call, because the timeout penalty only reached the non-streaming latency list and only fired from the async failure hook. | Open |
| 2026-11-18 | [vllm #68547](https://github.com/vllm-project/vllm/pull/68547) | With gpt-oss on the Responses API, a built-in tool call cut off by max_output_tokens or a stop string was still executed on its truncated input, another turn started, and the response reported completed. | Open |
| 2026-11-18 | [flax #5654](https://github.com/google/flax/pull/5654) | nnx.BatchNorm with bf16 or fp16 compute cast its float32 running statistics to the half dtype in eval, so eval drifted from training and an fp16 variance above 65504 collapsed its channel to the bias. | Open |
| 2026-11-18 | [Ray #68314](https://github.com/ray-project/ray/pull/68314) | Result.get_best_checkpoint returned a NaN-scored checkpoint as the best one, in Ray Tune and in Ray Train V2, whenever a run diverged and num_to_keep was left at its default. | Open |
| 2026-11-18 | [pytorch-lightning #22197](https://github.com/Lightning-AI/pytorch-lightning/pull/22197) | Resuming from a mid-epoch checkpoint silently skipped one batch whenever the stateful train dataloader had no length (torchdata StatefulDataLoader over an IterableDataset, HF streaming datasets). | Open |
| 2026-11-17 | [Ray #68261](https://github.com/ray-project/ray/pull/68261) | A PBT trial retried under max_failures lost its PBT state, so synchronous PBT exploited at mismatched steps and could overwrite the best trial with a worse one. | Open |
| 2026-11-17 | [unsloth #18213](https://github.com/unslothai/unsloth/pull/18213) | On transformers >= 4.48 the LongRoPE rotary was never installed, so llama-type Phi-3.5 used short factors at every length; cos/sin were up to 2.38 off past 4096 tokens in training and decode. | Merged |
| 2026-11-17 | [unsloth-zoo #2579](https://github.com/unslothai/unsloth-zoo/pull/2579) | prepare_model_for_training froze PEFT trainable_token_indices deltas, so the chosen token rows never trained on either loader path. | Merged |

_Showing the 17 most recent. Open `index.html` for the full visual dashboard._

---
_Statuses are refreshed straight from the GitHub API, so this page reflects the live state of every pull request._
