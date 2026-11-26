# Open-source contributions

_Vineeth Sai · [@vineethsaivs](https://github.com/vineethsaivs) · auto-updated after every contribution · last updated November 26, 2026 at 1:42 PM PT_

| PRs | Merged | Open | Merge rate | Projects | Streak |
|:--:|:--:|:--:|:--:|:--:|:--:|
| **580** | **279** | **222** | **78%** | **42** | **168 days** |

_2278 GitHub contributions in the last year · 196 in the last 7 days · 593 in the last 30._

## Bug reports

- [peft #4115](https://github.com/huggingface/peft/issues/4115): C3ALinear.forward rebinds x to each adapter's output, so with more than one active adapter the second one convolves the first one's result instead of the layer input.
- [peft #4094](https://github.com/huggingface/peft/issues/4094): reduce_intruder_dimension does not transpose the delta weight for fan_in_fan_out (GPT-2 Conv1D) or nn.Embedding LoRA layers, so the rebuilt adapter is wrong.
- [flax #5594](https://github.com/google/flax/issues/5594): nnx.GRUCell is missing the b_hn bias that its docstring and linen.GRUCell both specify.
- [trl #7221](https://github.com/huggingface/trl/issues/7221): Reproduced NaN entropy for valid zero-probability tokens, including finite float16 inputs; PyTorch categorical entropy remains finite.

## Recent activity

| Date | Project | What | Status |
|---|---|---|---|
| 2026-11-26 | [pytorch-lightning #22240](https://github.com/Lightning-AI/pytorch-lightning/pull/22240) | LearningRateFinder and BatchSizeFinder used as callbacks now reach the LR schedulers: fit calls configure_optimizers again after the search, instead of keeping the pre-search schedule. | Open |
| 2026-11-26 | [unsloth-zoo #2853](https://github.com/unslothai/unsloth-zoo/pull/2853) | train_on_responses_only no longer trains Gemma 4 and FunctionGemma models to write the tool results their templates render inside the model turn. | Open |
| 2026-11-26 | [unsloth #19806](https://github.com/unslothai/unsloth/pull/19806) | save_pretrained_gguf(save_method='lora') now writes adapters that llama.cpp applies as trained for rsLoRA, PiSSA and OLoRA, instead of a silently wrong adapter. | Open |
| 2026-11-25 | [unsloth #19545](https://github.com/unslothai/unsloth/pull/19545) | save_pretrained_merged now writes the trained model after from_pretrained reloads a PiSSA or OLoRA adapter, instead of adding the adapter to the wrong base weight. | Open |
| 2026-11-25 | [unsloth-zoo #2787](https://github.com/unslothai/unsloth-zoo/pull/2787) | UnslothMTPTrainer with gradient accumulation under Unsloth now weights the accumulation window by tokens, like one big batch, instead of silently averaging per-microbatch means. | Open |
| 2026-11-25 | [pytorch-lightning #22233](https://github.com/Lightning-AI/pytorch-lightning/pull/22233) | EarlyStopping no longer crashes at setup with AttributeError when val_check_interval is time-based (timedelta, 'DD:HH:MM:SS' or dict); it checks after validation, as ModelCheckpoint does. | Merged |
| 2026-11-24 | [optax #1902](https://github.com/google-deepmind/optax/pull/1902) | contrib.scale_by_ademamix(mu_dtype=...) now keeps its state dtypes stable across updates: mu_dtype covers the fast EMA only and is cast back after each update, so the optimizer runs inside jax.lax.scan. | Open |
| 2026-11-24 | [unsloth #19314](https://github.com/unslothai/unsloth/pull/19314) | The Studio Data Recipe seed preview now reads a JSON or JSONL file that starts with a UTF-8 BOM instead of failing with 422 seed inspect failed, as its CSV branch already did. | Merged |
| 2026-11-24 | [optax #1901](https://github.com/google-deepmind/optax/pull/1901) | contrib.scale_by_muon() with its default weight_dimension_numbers=None now orthogonalizes every leaf of a params tree as a matrix instead of raising a pytree structure error. | Open |
| 2026-11-23 | [optax #1900](https://github.com/google-deepmind/optax/pull/1900) | contrib.muon(weight_decay_mask=...) now also masks weight decay on the leaves routed to its AdamW branch, so the usual no-decay mask for biases and norms works when adam_weight_decay > 0. | Open |
| 2026-11-23 | [flax #5661](https://github.com/google/flax/pull/5661) | nn.scan, nn.RNN and nn.remat_scan no longer raise a false 'broadcasted variable has a data dependency on the scan body' error when the body has jax.debug.print, jax.debug.callback or checkify.check. | Open |
| 2026-11-23 | [pytorch-lightning #22216](https://github.com/Lightning-AI/pytorch-lightning/pull/22216) | Fabric.clip_gradients(max_norm=...) with precision 16-mixed no longer raises on the overflow steps that the GradScaler skips. | Open |
| 2026-11-22 | [tunix #3451](https://github.com/google/tunix/pull/3451) | Carry the learner's precomputed sampler IS/RS weights and the sampler_agreement_applied flag through sequence packing, so TIS, rejection sampling and seq_logprob_error_threshold keep working on packed GRPO batches. | Open |
| 2026-11-22 | [pytorch-lightning #22212](https://github.com/Lightning-AI/pytorch-lightning/pull/22212) | Stop LearningRateFinder and BatchSizeFinder callbacks from wiping the checkpoint that fit(ckpt_path=...) is about to resume, so training continues from the saved epoch, step, optimizer, scheduler and scaler. | Merged |
| 2026-11-22 | [unsloth #18974](https://github.com/unslothai/unsloth/pull/18974) | Route the generated UnslothSFTTrainer's prediction_step back to Unsloth's eval step on TRL 1.15 and later, so evaluate() with compute_metrics and trainer.predict() stop crashing on EmptyLogits. | Merged |
| 2026-11-22 | [unsloth #18973](https://github.com/unslothai/unsloth/pull/18973) | Decide ensure_weight_tying after the add_new_tokens block appends embed_tokens and lm_head, so a tied model trains one shared embedding and the merged and GGUF exports keep the trained head. | Merged |

_Showing the 16 most recent. Open `index.html` for the full visual dashboard._

---
_Statuses are refreshed straight from the GitHub API, so this page reflects the live state of every pull request._
