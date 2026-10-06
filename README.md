# Open-source contributions

_Vineeth Sai · [@vineethsaivs](https://github.com/vineethsaivs) · auto-updated after every contribution · last updated October 6, 2026 at 12:27 AM PT_

| PRs | Merged | Open | Merge rate | Projects | Streak |
|:--:|:--:|:--:|:--:|:--:|:--:|
| **403** | **169** | **171** | **73%** | **42** | **117 days** |

_1356 GitHub contributions in the last year · 63 in the last 7 days · 497 in the last 30._

## Bug reports

- [flax #5594](https://github.com/google/flax/issues/5594): nnx.GRUCell is missing the b_hn bias that its docstring and linen.GRUCell both specify.
- [trl #7221](https://github.com/huggingface/trl/issues/7221): Reproduced NaN entropy for valid zero-probability tokens, including finite float16 inputs; PyTorch categorical entropy remains finite.

## Recent activity

| Date | Project | What | Status |
|---|---|---|---|
| 2026-10-04 | [flax #5611](https://github.com/google/flax/pull/5611) | norm layers with axis_name and mask averaged per-device masked means, and a fully padded device made every device's stats nan | Open |
| 2026-10-04 | [Ray #66711](https://github.com/ray-project/ray/pull/66711) | metric_analysis avg used training_iteration as the count, so sparse metrics' averages were wrong | Open |
| 2026-10-04 | [flax #5610](https://github.com/google/flax/pull/5610) | CIRCULAR ConvTranspose(transpose_kernel=True) was a circularly shifted transpose of CIRCULAR Conv for most strides | Open |
| 2026-10-04 | [Ray #66710](https://github.com/ray-project/ray/pull/66710) | HyperBand stopped each bracket's best trials short of max_t unless eta**s divides max_t | Open |
| 2026-10-04 | [unsloth #12697](https://github.com/unslothai/unsloth/pull/12697) | the #12458 regression test raised TypeError on Transformers 4.x before checking anything | Open |
| 2026-10-03 | [unsloth #12642](https://github.com/unslothai/unsloth/pull/12642) | DoRA models generated without the DoRA magnitude: fast decode ran the plain LoRA delta | Merged |
| 2026-10-03 | [DeepSpeed #8735](https://github.com/deepspeedai/DeepSpeed/pull/8735) | fp32 pipeline parallelism clipped every stage with the first stage's gradient norm | Open |
| 2026-10-03 | [flax #5609](https://github.com/google/flax/pull/5609) | nnx.view(mha, decode=True, batch_size=..., max_length=...) never created the KV cache | Open |
| 2026-10-03 | [sentence-transformers #4120](https://github.com/huggingface/sentence-transformers/pull/4120) | ParaphraseMiningEvaluator(add_transitive_closure=True) followed pairs marked False in duplicates_dict as duplicates | Open |
| 2026-10-02 | [DeepSpeed #8729](https://github.com/deepspeedai/DeepSpeed/pull/8729) | ZeRO++ qgZ across nodes returned 2D weight gradients scaled by GPUs per node (8x on 8-GPU nodes) | Open |
| 2026-10-02 | [flax #5608](https://github.com/google/flax/pull/5608) | nnx OptimizedLSTMCell and GRUCell applied orthogonal init to the fused (H, kH) kernel, so no gate block was orthogonal | Open |
| 2026-10-02 | [sentence-transformers #4117](https://github.com/huggingface/sentence-transformers/pull/4117) | With SparseAutoEncoder(normalize=True), CSR compared de-normalized reconstructions with the normalized input | Open |
| 2026-10-01 | [DeepSpeed #8725](https://github.com/deepspeedai/DeepSpeed/pull/8725) | FusedLamb applied Adam's bias correction after LAMB's trust ratio, shrinking every step (0.32x at t=1, 0.15x near t=10) | Open |
| 2026-10-01 | [sentence-transformers #4111](https://github.com/huggingface/sentence-transformers/pull/4111) | CSR's SparseAutoEncoder masked pre-activations in place for the aux loss, so the 4k reconstruction term trained nothing | Open |
| 2026-10-01 | [optax #1799](https://github.com/google-deepmind/optax/pull/1799) | projection_l1_sphere returned points off the sphere for inputs inside the l1 ball that contain zeros | Open |
| 2026-10-01 | [unsloth #12458](https://github.com/unslothai/unsloth/pull/12458) | With embedding_learning_rate and adamw_8bit, trained embeddings got 8-bit Adam state instead of transformers' 32-bit | Merged |
| 2026-10-01 | [sentence-transformers #4109](https://github.com/huggingface/sentence-transformers/pull/4109) | NO_DUPLICATES and GROUP_BY_LABEL batch samplers ignored args.seed, so every seed trained on the same batch order | Open |
| 2026-10-01 | [DeepSpeed #8721](https://github.com/deepspeedai/DeepSpeed/pull/8721) | DeepSpeedCPUAdagrad crashed on every real nn.Embedding(sparse=True) step (uncoalesced sparse grad) | Open |
| 2026-10-01 | [flax #5606](https://github.com/google/flax/pull/5606) | nnx.GroupNorm gave wrong outputs when reduction_axes left more than the batch axis unreduced | Open |

_Showing the 19 most recent. Open `index.html` for the full visual dashboard._

---
_Statuses are refreshed straight from the GitHub API, so this page reflects the live state of every pull request._
