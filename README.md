# Open-source contributions

_Vineeth Sai · [@vineethsaivs](https://github.com/vineethsaivs) · auto-updated after every contribution · last updated August 28, 2026 at 10:50 PM PT_

| PRs | Merged | Open | Merge rate | Projects | Streak |
|:--:|:--:|:--:|:--:|:--:|:--:|
| **215** | **82** | **110** | **78%** | **37** | **25 days** |

_22 in the last 7 days · 92 in the last 30._

## Recent activity

| Date | Project | What | Status |
|---|---|---|---|
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
| 2026-08-23 | [DeepSpeed #8305](https://github.com/deepspeedai/DeepSpeed/pull/8305) | ZeRO-3's partition() hardcoded free_data=True at two hops, so free_data=False never reached the guard and the leaf-module fast-sharding path was a no-op | Open |
| 2026-08-23 | [DeepSpeed #8304](https://github.com/deepspeedai/DeepSpeed/pull/8304) | the SLURM launcher forwarded DeepSpeed's own --include to srun, which has no such flag, and sized the job from the unfiltered hostfile, so both resource filters were broken | Open |
| 2026-08-23 | [unsloth #9590](https://github.com/unslothai/unsloth/pull/9590) | main's Repo tests (CPU) went red because a contract test matched raw source for a set literal that a new entry wrapped across lines, while the rule it guards stayed intact | Closed, fix validated |
| 2026-08-23 | [pytorch #194537](https://github.com/pytorch/pytorch/pull/194537) | the conv and avg_pool nn.functional docs carried no parameter types at all, so their pages showed bare names where every other page shows name (type) | Open |
| 2026-08-23 | [pytorch #194535](https://github.com/pytorch/pytorch/pull/194535) | gather and scatter accept a 0-D tensor opposite a 1-D one, but the docs and the shape-check messages claim the dimensions must match | Open |

_Showing the 19 most recent. Open `index.html` for the full visual dashboard._

---
_Statuses are refreshed straight from the GitHub API, so this page reflects the live state of every pull request._
