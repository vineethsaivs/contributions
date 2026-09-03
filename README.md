# Open-source contributions

_Vineeth Sai · [@vineethsaivs](https://github.com/vineethsaivs) · auto-updated after every contribution · last updated September 3, 2026 at 2:36 PM PT_

| PRs | Merged | Open | Merge rate | Projects | Streak |
|:--:|:--:|:--:|:--:|:--:|:--:|
| **240** | **96** | **118** | **79%** | **38** | **31 days** |

_29 in the last 7 days · 107 in the last 30._

## Recent activity

| Date | Project | What | Status |
|---|---|---|---|
| 2026-09-03 | [accelerate #4210](https://github.com/huggingface/accelerate/pull/4210) | `dtype_byte_size` ends in `bit_size // 8`, so all twenty sub-byte torch dtypes (uint1-uint7, int1-int7, float4_e2m1fn_x2, bits2x4, bits4x2, quint2x4, quint4x2) floor to 0 bytes and `compute_module_sizes` measures a 4-bit module as free | Open |
| 2026-09-03 | [datasets #8559](https://github.com/huggingface/datasets/pull/8559) | `Dataset.repeat`'s example calls `take(2).repeat(2)`, which returns four rows, and prints six; `IterableDataset.repeat` carries the same example and omits `streaming=True`, so it builds a `Dataset` and never reaches the method being documented | Open |
| 2026-09-03 | [pytorch #195936](https://github.com/pytorch/pytorch/pull/195936) | the `kaiser` window docstring prints `gaussian`'s output, ten values for a `kaiser(5)` call that returns five, and the `nuttall` docstring prints nuttall's values but calls `general_hamming`, which returns something else | Open |
| 2026-09-02 | [pytorch #195779](https://github.com/pytorch/pytorch/pull/195779) | the torch.trapezoid and torch.cumulative_trapezoid doc examples print outputs the functions never produce: two results shown as bare Python floats and two as NumPy `array(...)`, though both are documented `-> Tensor`, plus a tensor printed after an assignment that outputs nothing | Open |
| 2026-09-02 | [DeepSpeed #8395](https://github.com/deepspeedai/DeepSpeed/pull/8395) | elasticity v0.2 picked the micro batch by dividing the global batch by every GPU instead of by the data-parallel world, so with `model_parallel_size > 1` it chose a needlessly small micro batch or returned None when only the correct one was offered | Open |
| 2026-09-02 | [DeepSpeed #8394](https://github.com/deepspeedai/DeepSpeed/pull/8394) | the flops profiler counted `F.interpolate(x, size=...)` over the output spatial shape alone, dropping the batch and channel dims, so the same upsample reported 4096 flops with `size=(64,64)` and 98304 with `scale_factor=2` | Open |
| 2026-09-01 | [pytorch #195639](https://github.com/pytorch/pytorch/pull/195639) | gradcheck compares the two Jacobians with torch.allclose but never exposed its equal_nan, so a function defined on only part of the sampled domain produces two identical all-NaN Jacobians and is reported as a mismatch between them | Open |
| 2026-09-01 | [unsloth #10153](https://github.com/unslothai/unsloth/pull/10153) | get_chat_template reads padding_side straight off whatever it is handed, so a vision checkpoint's processor, which keeps it on the tokenizer it wraps, raises AttributeError before the call can do anything | Withdrawn |
| 2026-09-01 | [DeepSpeed #8386](https://github.com/deepspeedai/DeepSpeed/pull/8386) | mask_nan_or_inf_with_val_inplace takes a val argument and then builds its fill tensor from a hardcoded -1.0, so the one knob the refactor that created the helper introduced has never done anything | Open |
| 2026-08-31 | [unsloth #10101](https://github.com/unslothai/unsloth/pull/10101) | get_ollama_eos_tokens collapses a token family into its shared prefix while rewriting the text it scans, so the answer depends on list order and the list came from a set: a Gemma-shaped vocabulary exported <unk> on some runs and a two-character <un stop token in its place on others | Merged |
| 2026-08-31 | [DeepSpeed #8378](https://github.com/deepspeedai/DeepSpeed/pull/8378) | a frozen parameter has no fp32 master copy, so get_fp32_state_dict_from_zero_checkpoint returned it in the model's own dtype while trainable parameters and buffers came back fp32, breaking its documented fp32 contract on every bf16 or fp16 run | Open |
| 2026-08-31 | [DeepSpeed #8376](https://github.com/deepspeedai/DeepSpeed/pull/8376) | to_torch_tensor maps tied parameters onto one shared tensor and safetensors refuses tensors that share storage, so zero_to_fp32 --safe_serialization aborted on any model with tied weights, which is the usual embedding / lm_head pair | Open |
| 2026-08-30 | [vllm #54499](https://github.com/vllm-project/vllm/pull/54499) | the Hunyuan A13B streaming parser reads its shorter side sequence at the main sequence's index, so a stream that matches six of the seven response-start tokens and then diverges raises IndexError instead of taking the fallback every earlier divergence takes | Open |
| 2026-08-30 | [trl #6980](https://github.com/huggingface/trl/pull/6980) | the chunked lm_head backward matmuls the lm_head weight without the dtype cast its own forward applies, so under autocast a forward that succeeds cannot be backpropagated and raises a dtype mismatch | Open |
| 2026-08-30 | [unsloth #10028](https://github.com/unslothai/unsloth/pull/10028) | the single-device block assigned a bare lambda to Accelerator.distributed_type, which is a property upstream, so it bound as a method and accelerate's != DistributedType.NO guards fired on a single device with the device_map error the block exists to prevent | Merged |
| 2026-08-30 | [pytorch #195376](https://github.com/pytorch/pytorch/pull/195376) | the non-empty guard in the nearest-upsample metas passed torch._check the product of the non-batch sizes, an int rather than a bool, so every zero-element input raised TypeError out of the check itself, including the zero-batch case eager upsamples fine | Open |
| 2026-08-30 | [accelerate #4197](https://github.com/huggingface/accelerate/pull/4197) | convert_file_size_to_int applies the bit-vs-byte suffix rule to the decimal units only, so a max_memory entry given in gibibits is parsed as gibibytes and plans a device map against 8x the memory that is there | Open |
| 2026-08-30 | [sentence-transformers #3971](https://github.com/huggingface/sentence-transformers/pull/3971) | two of the four multi-process workers never walk a list result, so the list-of-tensors and output_value=None shapes reach the results queue still on the accelerator, as handles the caller can no longer read once stop_multi_process_pool has torn the workers down | Merged |
| 2026-08-30 | [datasets #8539](https://github.com/huggingface/datasets/pull/8539) | convert_file_size_to_int reads a lowercase trailing b as bits and divides by 8 on the decimal units only, so the five binary branches read 1Gib as one gibibyte and return a max_shard_size 8x too large | Open |

_Showing the 19 most recent. Open `index.html` for the full visual dashboard._

---
_Statuses are refreshed straight from the GitHub API, so this page reflects the live state of every pull request._
