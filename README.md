# Open-source contributions

_Vineeth Sai · [@vineethsaivs](https://github.com/vineethsaivs) · auto-updated after every contribution · last updated August 29, 2026 at 3:51 PM PT_

| PRs | Merged | Open | Merge rate | Projects | Streak |
|:--:|:--:|:--:|:--:|:--:|:--:|
| **221** | **82** | **116** | **78%** | **39** | **26 days** |

_25 in the last 7 days · 96 in the last 30._

## Recent activity

| Date | Project | What | Status |
|---|---|---|---|
| 2026-08-29 | [unsloth-zoo #1133](https://github.com/unslothai/unsloth-zoo/pull/1133) | the test suite's own sys.modules leak guard reported unsloth-zoo's own bitsandbytes stub as a test leak, so the first test in any session to import the package failed in teardown on every host without a real bitsandbytes | Open |
| 2026-08-29 | [ray #65790](https://github.com/ray-project/ray/pull/65790) | PBT's _quantiles sliced the top of the population as trials[-num_trials_in_quantile:], so quantile_fraction=0, documented as no exploitation at all, put every trial in the upper quantile and made all of them checkpoint every interval | Open |
| 2026-08-29 | [DeepSpeed #8360](https://github.com/deepspeedai/DeepSpeed/pull/8360) | ZenFlow's gradient copy branched on grad_accum is None and then called .view() on the None in both arms, raising an AttributeError where the base ZeRO-1/2 copy raises its own assertion | Open |
| 2026-08-29 | [pytorch-lightning #21923](https://github.com/Lightning-AI/pytorch-lightning/pull/21923) | lr_find's suggestion() sliced the loss curve with [skip_begin:-skip_end], so skip_end=0, the documented way to keep the whole curve, selected nothing and returned no suggestion at all | Open |
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

_Showing the 16 most recent. Open `index.html` for the full visual dashboard._

---
_Statuses are refreshed straight from the GitHub API, so this page reflects the live state of every pull request._
