# Open-source contributions

_Vineeth Sai · [@vineethsaivs](https://github.com/vineethsaivs) · auto-updated after every contribution · last updated September 2, 2026 at 11:05 AM PT_

| PRs | Merged | Open | Merge rate | Projects | Streak |
|:--:|:--:|:--:|:--:|:--:|:--:|
| **234** | **93** | **115** | **78%** | **38** | **29 days** |

_26 in the last 7 days · 103 in the last 30._

## Recent activity

| Date | Project | What | Status |
|---|---|---|---|
| 2026-09-01 | [pytorch #195639](https://github.com/pytorch/pytorch/pull/195639) | gradcheck compares the two Jacobians with torch.allclose but never exposed its equal_nan, so a function defined on only part of the sampled domain produces two identical all-NaN Jacobians and is reported as a mismatch between them | Open |
| 2026-09-01 | [unsloth #10153](https://github.com/unslothai/unsloth/pull/10153) | get_chat_template reads padding_side straight off whatever it is handed, so a vision checkpoint's processor, which keeps it on the tokenizer it wraps, raises AttributeError before the call can do anything | Withdrawn |
| 2026-09-01 | [DeepSpeed #8386](https://github.com/deepspeedai/DeepSpeed/pull/8386) | mask_nan_or_inf_with_val_inplace takes a val argument and then builds its fill tensor from a hardcoded -1.0, so the one knob the refactor that created the helper introduced has never done anything | Open |
| 2026-08-31 | [unsloth #10101](https://github.com/unslothai/unsloth/pull/10101) | get_ollama_eos_tokens collapses a token family into its shared prefix while rewriting the text it scans, so the answer depends on list order and the list came from a set: a Gemma-shaped vocabulary exported <unk> on some runs and a two-character <un stop token in its place on others | Open |
| 2026-08-31 | [DeepSpeed #8378](https://github.com/deepspeedai/DeepSpeed/pull/8378) | a frozen parameter has no fp32 master copy, so get_fp32_state_dict_from_zero_checkpoint returned it in the model's own dtype while trainable parameters and buffers came back fp32, breaking its documented fp32 contract on every bf16 or fp16 run | Open |
| 2026-08-31 | [DeepSpeed #8376](https://github.com/deepspeedai/DeepSpeed/pull/8376) | to_torch_tensor maps tied parameters onto one shared tensor and safetensors refuses tensors that share storage, so zero_to_fp32 --safe_serialization aborted on any model with tied weights, which is the usual embedding / lm_head pair | Open |
| 2026-08-30 | [vllm #54499](https://github.com/vllm-project/vllm/pull/54499) | the Hunyuan A13B streaming parser reads its shorter side sequence at the main sequence's index, so a stream that matches six of the seven response-start tokens and then diverges raises IndexError instead of taking the fallback every earlier divergence takes | Open |
| 2026-08-30 | [trl #6980](https://github.com/huggingface/trl/pull/6980) | the chunked lm_head backward matmuls the lm_head weight without the dtype cast its own forward applies, so under autocast a forward that succeeds cannot be backpropagated and raises a dtype mismatch | Open |
| 2026-08-30 | [unsloth #10028](https://github.com/unslothai/unsloth/pull/10028) | the single-device block assigned a bare lambda to Accelerator.distributed_type, which is a property upstream, so it bound as a method and accelerate's != DistributedType.NO guards fired on a single device with the device_map error the block exists to prevent | Merged |
| 2026-08-30 | [pytorch #195376](https://github.com/pytorch/pytorch/pull/195376) | the non-empty guard in the nearest-upsample metas passed torch._check the product of the non-batch sizes, an int rather than a bool, so every zero-element input raised TypeError out of the check itself, including the zero-batch case eager upsamples fine | Open |
| 2026-08-30 | [accelerate #4197](https://github.com/huggingface/accelerate/pull/4197) | convert_file_size_to_int applies the bit-vs-byte suffix rule to the decimal units only, so a max_memory entry given in gibibits is parsed as gibibytes and plans a device map against 8x the memory that is there | Open |
| 2026-08-30 | [sentence-transformers #3971](https://github.com/huggingface/sentence-transformers/pull/3971) | two of the four multi-process workers never walk a list result, so the list-of-tensors and output_value=None shapes reach the results queue still on the accelerator, as handles the caller can no longer read once stop_multi_process_pool has torn the workers down | Merged |
| 2026-08-30 | [datasets #8539](https://github.com/huggingface/datasets/pull/8539) | convert_file_size_to_int reads a lowercase trailing b as bits and divides by 8 on the decimal units only, so the five binary branches read 1Gib as one gibibyte and return a max_shard_size 8x too large | Open |
| 2026-08-29 | [unsloth-zoo #1133](https://github.com/unslothai/unsloth-zoo/pull/1133) | the test suite's own sys.modules leak guard reported unsloth-zoo's own bitsandbytes stub as a test leak, so the first test in any session to import the package failed in teardown on every host without a real bitsandbytes | Open |
| 2026-08-29 | [Ray #65790](https://github.com/ray-project/ray/pull/65790) | PBT's _quantiles sliced the top of the population as trials[-num_trials_in_quantile:], so quantile_fraction=0, documented as no exploitation at all, put every trial in the upper quantile and made all of them checkpoint every interval | Open |
| 2026-08-29 | [DeepSpeed #8360](https://github.com/deepspeedai/DeepSpeed/pull/8360) | ZenFlow's gradient copy branched on grad_accum is None and then called .view() on the None in both arms, raising an AttributeError where the base ZeRO-1/2 copy raises its own assertion | Open |
| 2026-08-29 | [pytorch-lightning #21923](https://github.com/Lightning-AI/pytorch-lightning/pull/21923) | lr_find's suggestion() sliced the loss curve with [skip_begin:-skip_end], so skip_end=0, the documented way to keep the whole curve, selected nothing and returned no suggestion at all | Open |
| 2026-08-29 | [litellm #38737](https://github.com/BerriAI/litellm/pull/38737) | the spend-log truncation wrote its tail as value[-end_chars:], and both shares floor to zero at a limit of 1 or less, so the tightest MAX_STRING_LENGTH_PROMPT_IN_DB stored the whole prompt plus a marker saying it had been skipped | Open |
| 2026-08-29 | [vllm #54321](https://github.com/vllm-project/vllm/pull/54321) | an explicit tool_choice null was not treated as an absent one, so tools were never parsed out of the reply and a structured-outputs request carrying a null tool_choice and no tools was refused as asking for both | Open |

_Showing the 19 most recent. Open `index.html` for the full visual dashboard._

---
_Statuses are refreshed straight from the GitHub API, so this page reflects the live state of every pull request._
