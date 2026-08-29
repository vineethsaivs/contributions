# Open-source contributions

_Vineeth Sai · [@vineethsaivs](https://github.com/vineethsaivs) · auto-updated after every contribution · last updated August 29, 2026 at 12:15 AM PT_

| PRs | Merged | Open | Merge rate | Projects | Streak |
|:--:|:--:|:--:|:--:|:--:|:--:|
| **217** | **82** | **112** | **78%** | **37** | **26 days** |

_21 in the last 7 days · 92 in the last 30._

## Recent activity

| Date | Project | What | Status |
|---|---|---|---|
| 2026-08-29 | [litellm #38737](https://github.com/BerriAI/litellm/pull/38737) | the spend-log truncation wrote its tail as value[-end_chars:], and both shares floor to zero at a limit of 1 or less, so the tightest MAX_STRING_LENGTH_PROMPT_IN_DB stored the whole prompt plus a marker saying it had been skipped | Open |
| 2026-08-29 | [vllm #54321](https://github.com/vllm-project/vllm/pull/54321) | an explicit tool_choice null was not treated as an absent one, so tools were never parsed out of the reply and a structured-outputs request carrying a null tool_choice and no tools was refused as asking for both | Open |
| 2026-08-28 | [unsloth #9950](https://github.com/unslothai/unsloth/pull/9950) | unsloth's copy of unsloth-zoo's optimizer collapse list carried adamw_8bit, which the zoo deliberately leaves out because MLX implements it, so the notebook default was downgraded to plain adamw and the repo's own MLX test failed on every Apple Silicon machine | Open |
| 2026-08-28 | [DeepSpeed #8347](https://github.com/deepspeedai/DeepSpeed/pull/8347) | batch_by_seqlens walked candidate slice ends with a range stopping at len(metrics), and batch_end is the exclusive end of the slice, so the last sample of the dataset was never placed in a microbatch | Open |
| 2026-08-28 | [vllm #54297](https://github.com/vllm-project/vllm/pull/54297) | the Responses API backfilled id, status and annotations only when the key was absent, so an SDK round-tripping an item with an explicit null was rejected with a 400 and a 200-entry validation dump | Open |
| 2026-08-28 | [unsloth #9944](https://github.com/unslothai/unsloth/pull/9944) | the backwards-compatible trainer wrapper sorted keywords into trainer kwargs and config kwargs, but the elif and the else wrote to the same dict, so a keyword neither side takes, max_seq_length after trl 0.20 removed it from SFTConfig, was dropped in silence and the run trained at the default length | Open |
| 2026-08-27 | [unsloth #9887](https://github.com/unslothai/unsloth/pull/9887) | quant_type defaults to None on ModelInfo, append_quant_type and register_model, but QUANT_TAG_MAP is keyed by QuantType, so using any of those defaults raised KeyError: None | Open |
| 2026-08-27 | [DeepSpeed #8334](https://github.com/deepspeedai/DeepSpeed/pull/8334) | the curriculum schedule floored the difficulty to a multiple of difficulty_step with no lower clamp, so min_difficulty 8 with difficulty_step 16, a pair the tutorial recommends together, started training at difficulty 0 | Open |
| 2026-08-27 | [pytorch #195043](https://github.com/pytorch/pytorch/pull/195043) | nn.grad.convNd_input is the reference conv_transpose is checked against but has no output_padding, so any non-default one made it reject the shape with 'grad_output[2:] shape ... must be equal to output size ...' | Open |
| 2026-08-26 | [DeepSpeed #8324](https://github.com/deepspeedai/DeepSpeed/pull/8324) | the flops profiler broadcast elementwise mul/add shapes from index 0 instead of from the trailing dimension, so scaling a [2, 3, 4] activation by a [4] vector was counted over [4, 3, 4] | Open |
| 2026-08-26 | [Ray #65747](https://github.com/ray-project/ray/pull/65747) | PBT converted a perturbed integer hyperparameter back with int(), which truncates toward zero, so * 1.2 was a no-op below 5 while * 0.8 always landed lower and the parameter could only ratchet down to an absorbing 0 | Open |
| 2026-08-26 | [DeepSpeed #8323](https://github.com/deepspeedai/DeepSpeed/pull/8323) | the flops profiler read a transposed convolution's weight as if it were a forward convolution's and sized its output with the forward shape formula, so every grouped transposed conv under-counted its macs by a factor of groups and a depthwise one reported zero | Open |
| 2026-08-25 | [Ray #65731](https://github.com/ray-project/ray/pull/65731) | tune.qrandint and tune.qlograndint never sampled the upper bound they document as inclusive, and raised ValueError when the quantization grid held a single point | Open |
| 2026-08-25 | [litellm #38244](https://github.com/BerriAI/litellm/pull/38244) | shorten_message_to_fit_limit grew the message instead of trimming it whenever the target was small, because content[-0:] is the whole string | Open |
| 2026-08-25 | [DeepSpeed #8317](https://github.com/deepspeedai/DeepSpeed/pull/8317) | the Ulysses all2all built its output shape from the wrong branch for the seq-first (s, b, n, h) layout, silently returning a transposed tensor when the head count divides evenly and raising on the reshape when it does not | Merged |
| 2026-08-24 | [DeepSpeed #8313](https://github.com/deepspeedai/DeepSpeed/pull/8313) | three norm-combining sites squared the per-tensor norms and then took the 1/norm_type root, so every p-norm except p=2 returned the wrong global norm and clipped the gradients by the wrong factor; ZeRO-3 also took an L2 norm per tensor whatever norm_type said | Merged |

_Showing the 16 most recent. Open `index.html` for the full visual dashboard._

---
_Statuses are refreshed straight from the GitHub API, so this page reflects the live state of every pull request._
