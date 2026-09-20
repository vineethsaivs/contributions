# Open-source contributions

_Vineeth Sai · [@vineethsaivs](https://github.com/vineethsaivs) · auto-updated after every contribution · last updated September 19, 2026 at 5:12 PM PT_

| PRs | Merged | Open | Merge rate | Projects | Streak |
|:--:|:--:|:--:|:--:|:--:|:--:|
| **338** | **129** | **166** | **75%** | **39** | **100 days** |

_1142 GitHub contributions in the last year · 195 in the last 7 days · 462 in the last 30._

## Bug reports

- [trl #7221](https://github.com/huggingface/trl/issues/7221): Reproduced NaN entropy for valid zero-probability tokens, including finite float16 inputs; PyTorch categorical entropy remains finite.

## Recent activity

| Date | Project | What | Status |
|---|---|---|---|
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
| 2026-09-16 | [unsloth-zoo #1262](https://github.com/unslothai/unsloth-zoo/pull/1262) | Keep GRPO KL metrics finite for fully masked completions | Open |
| 2026-09-16 | [unsloth-zoo #1261](https://github.com/unslothai/unsloth-zoo/pull/1261) | Apply MLX clipping scales before narrowing to fp16 | Open |
| 2026-09-16 | [accelerate #4274](https://github.com/huggingface/accelerate/pull/4274) | Return the wrapped optimizer step result | Open |
| 2026-09-16 | [DeepSpeed #8553](https://github.com/deepspeedai/DeepSpeed/pull/8553) | Accept NumPy integer indices in indexed datasets | Open |
| 2026-09-16 | [DeepSpeed #8552](https://github.com/deepspeedai/DeepSpeed/pull/8552) | Preserve convolution shapes and scaling in Muon updates | Open |

_Showing the 17 most recent. Open `index.html` for the full visual dashboard._

---
_Statuses are refreshed straight from the GitHub API, so this page reflects the live state of every pull request._
