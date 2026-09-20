# Open-source contributions

_Vineeth Sai · [@vineethsaivs](https://github.com/vineethsaivs) · auto-updated after every contribution · last updated September 20, 2026 at 12:48 PM PT_

| PRs | Merged | Open | Merge rate | Projects | Streak |
|:--:|:--:|:--:|:--:|:--:|:--:|
| **344** | **129** | **172** | **75%** | **39** | **101 days** |

_1152 GitHub contributions in the last year · 168 in the last 7 days · 463 in the last 30._

## Bug reports

- [trl #7221](https://github.com/huggingface/trl/issues/7221): Reproduced NaN entropy for valid zero-probability tokens, including finite float16 inputs; PyTorch categorical entropy remains finite.

## Recent activity

| Date | Project | What | Status |
|---|---|---|---|
| 2026-09-20 | [DeepSpeed #8614](https://github.com/deepspeedai/DeepSpeed/pull/8614) | Say why a bf16 gradient norm cannot be clipped from | Open |
| 2026-09-20 | [DeepSpeed #8613](https://github.com/deepspeedai/DeepSpeed/pull/8613) | Include the expert gradients in the unfused fp16 clip norm | Open |
| 2026-09-20 | [sentence-transformers #4054](https://github.com/huggingface/sentence-transformers/pull/4054) | Cap reranked scores by the positives the first stage missed | Open |
| 2026-09-20 | [accelerate #4294](https://github.com/huggingface/accelerate/pull/4294) | Unscale gradients once when FSDP clipping gets a partial list | Open |
| 2026-09-20 | [unsloth-zoo #1301](https://github.com/unslothai/unsloth-zoo/pull/1301) | Warn that the GRPO entropy bonus is ignored on this path | Open |
| 2026-09-20 | [DeepSpeed #8612](https://github.com/deepspeedai/DeepSpeed/pull/8612) | Forward the per-head Muon tag at every muon_update call site | Open |
| 2026-09-19 | [unsloth-zoo #1291](https://github.com/unslothai/unsloth-zoo/pull/1291) | Give TiledMLP autocast a device type torch understands | Open |
| 2026-09-19 | [unsloth-zoo #1290](https://github.com/unslothai/unsloth-zoo/pull/1290) | Size TiledMLP tiles over the whole batch, not one sequence | Open |
| 2026-09-19 | [DeepSpeed #8601](https://github.com/deepspeedai/DeepSpeed/pull/8601) | Clear the gradient ZenFlow just offloaded, not param.grad | Open |
| 2026-09-19 | [unsloth-zoo #1286](https://github.com/unslothai/unsloth-zoo/pull/1286) | Floor the DAPO normalizer so an empty batch is not a nan | Open |
| 2026-09-19 | [unsloth #11337](https://github.com/unslothai/unsloth/pull/11337) | Stop dividing the GRPO eval loss by the accumulation steps | Open |
| 2026-09-19 | [accelerate #4282](https://github.com/huggingface/accelerate/pull/4282) | Make reduce(reduction="none") perform no reduction | Open |
| 2026-09-19 | [sentence-transformers #4051](https://github.com/huggingface/sentence-transformers/pull/4051) | Count PListMLE rank positions from one, not zero | Open |
| 2026-09-18 | [unsloth-zoo #1282](https://github.com/unslothai/unsloth-zoo/pull/1282) | Mask the luspo loss elementwise before aggregating | Open |
| 2026-09-18 | [unsloth #11277](https://github.com/unslothai/unsloth/pull/11277) | Apply the logit scale on the fused cross entropy path | Open |
| 2026-09-18 | [DeepSpeed #8589](https://github.com/deepspeedai/DeepSpeed/pull/8589) | Decay OneCycle momentum instead of growing it past 1.0 | Open |
| 2026-09-18 | [DeepSpeed #8588](https://github.com/deepspeedai/DeepSpeed/pull/8588) | Report the unscaled gradient norm from FP16_UnfusedOptimizer | Open |
| 2026-09-18 | [DeepSpeed #8587](https://github.com/deepspeedai/DeepSpeed/pull/8587) | Weight the TiledLoss backward pass the way the forward does | Open |

_Showing the 18 most recent. Open `index.html` for the full visual dashboard._

---
_Statuses are refreshed straight from the GitHub API, so this page reflects the live state of every pull request._
