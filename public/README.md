# Open-source contributions

_Vineeth Sai · [@vineethsaivs](https://github.com/vineethsaivs) · auto-updated after every contribution · last updated November 23, 2026 at 6:50 PM PT_

| PRs | Merged | Open | Merge rate | Projects | Streak |
|:--:|:--:|:--:|:--:|:--:|:--:|
| **571** | **271** | **227** | **79%** | **42** | **165 days** |

_2186 GitHub contributions in the last year · 205 in the last 7 days · 540 in the last 30._

## Bug reports

- [peft #4115](https://github.com/huggingface/peft/issues/4115): C3ALinear.forward rebinds x to each adapter's output, so with more than one active adapter the second one convolves the first one's result instead of the layer input.
- [peft #4094](https://github.com/huggingface/peft/issues/4094): reduce_intruder_dimension does not transpose the delta weight for fan_in_fan_out (GPT-2 Conv1D) or nn.Embedding LoRA layers, so the rebuilt adapter is wrong.
- [flax #5594](https://github.com/google/flax/issues/5594): nnx.GRUCell is missing the b_hn bias that its docstring and linen.GRUCell both specify.
- [trl #7221](https://github.com/huggingface/trl/issues/7221): Reproduced NaN entropy for valid zero-probability tokens, including finite float16 inputs; PyTorch categorical entropy remains finite.

## Recent activity

| Date | Project | What | Status |
|---|---|---|---|
| 2026-11-23 | [optax #1900](https://github.com/google-deepmind/optax/pull/1900) | contrib.muon(weight_decay_mask=...) now also masks weight decay on the leaves routed to its AdamW branch, so the usual no-decay mask for biases and norms works when adam_weight_decay > 0. | Open |
| 2026-11-23 | [flax #5661](https://github.com/google/flax/pull/5661) | nn.scan, nn.RNN and nn.remat_scan no longer raise a false 'broadcasted variable has a data dependency on the scan body' error when the body has jax.debug.print, jax.debug.callback or checkify.check. | Open |
| 2026-11-23 | [pytorch-lightning #22216](https://github.com/Lightning-AI/pytorch-lightning/pull/22216) | Fabric.clip_gradients(max_norm=...) with precision 16-mixed no longer raises on the overflow steps that the GradScaler skips. | Open |
| 2026-11-22 | [tunix #3451](https://github.com/google/tunix/pull/3451) | Carry the learner's precomputed sampler IS/RS weights and the sampler_agreement_applied flag through sequence packing, so TIS, rejection sampling and seq_logprob_error_threshold keep working on packed GRPO batches. | Open |
| 2026-11-22 | [pytorch-lightning #22212](https://github.com/Lightning-AI/pytorch-lightning/pull/22212) | Stop LearningRateFinder and BatchSizeFinder callbacks from wiping the checkpoint that fit(ckpt_path=...) is about to resume, so training continues from the saved epoch, step, optimizer, scheduler and scaler. | Merged |
| 2026-11-22 | [unsloth #18974](https://github.com/unslothai/unsloth/pull/18974) | Route the generated UnslothSFTTrainer's prediction_step back to Unsloth's eval step on TRL 1.15 and later, so evaluate() with compute_metrics and trainer.predict() stop crashing on EmptyLogits. | Merged |
| 2026-11-22 | [unsloth #18973](https://github.com/unslothai/unsloth/pull/18973) | Decide ensure_weight_tying after the add_new_tokens block appends embed_tokens and lm_head, so a tied model trains one shared embedding and the merged and GGUF exports keep the trained head. | Merged |
| 2026-11-21 | [unsloth #18818](https://github.com/unslothai/unsloth/pull/18818) | GemmaFixedRotaryEmbedding now applies the linear RoPE scaling the loader writes when max_seq_length passes Gemma's native window, in the eager table and the compiled path. | Merged |
| 2026-11-21 | [tunix #3449](https://github.com/google/tunix/pull/3449) | Re-snapshot the old-policy anchor at sampling time for SHARED weight placement, so trainer-side old logps use the weights that sampled. | Open |
| 2026-11-21 | [pytorch-lightning #22208](https://github.com/Lightning-AI/pytorch-lightning/pull/22208) | Wrap the model in DDP again when BaseFinetuning changes requires_grad, so parameters unfrozen mid-training get all-reduced and the replicas stay in sync. | Open |
| 2026-11-20 | [unsloth-zoo #2636](https://github.com/unslothai/unsloth-zoo/pull/2636) | merged_16bit, push_to_hub_merged and GGUF exports wrote the base checkpoint's RoPE config next to weights trained with rope_scaling, so the reloaded model differed from the trained one. | Merged |
| 2026-11-20 | [unsloth #18650](https://github.com/unslothai/unsloth/pull/18650) | Unsloth Studio vision training gave a separate eval split a different user prompt than train, and the seeded max_steps shuffle picked the training prompt. | Merged |
| 2026-11-20 | [pytorch-lightning #22203](https://github.com/Lightning-AI/pytorch-lightning/pull/22203) | With every_n_train_steps and a validation monitor, a step checkpoint saved right before validation was scored with the previous validation's metric, so the wrong checkpoint was kept as best. | Open |
| 2026-11-19 | [Ray #68354](https://github.com/ray-project/ray/pull/68354) | With HyperBandScheduler, search algorithms never saw the final metrics of trials stopped while PAUSED, so HyperOpt treated the 2nd and 3rd best trials as the worst points and Optuna marked full-length trials as pruned. | Open |
| 2026-11-19 | [flax #5655](https://github.com/google/flax/pull/5655) | nnx.MultiHeadAttention autoregressive decode with the RoPE attention function produced wrong outputs from the second token on, with no workaround. | Open |
| 2026-11-19 | [pytorch-lightning #22202](https://github.com/Lightning-AI/pytorch-lightning/pull/22202) | Since Lightning 2.5.0, a run resumed from a mid-epoch checkpoint silently lost its GradientAccumulationScheduler factor for the rest of the epoch and ran StochasticWeightAveraging one epoch late, and a second resume restarted the SWA average. | Open |

_Showing the 16 most recent. Open `index.html` for the full visual dashboard._

---
_Statuses are refreshed straight from the GitHub API, so this page reflects the live state of every pull request._
