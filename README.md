# Open-source contributions

_Vineeth Sai · [@vineethsaivs](https://github.com/vineethsaivs) · auto-updated after every contribution · last updated November 1, 2026 at 12:02 PM PT_

| PRs | Merged | Open | Merge rate | Projects | Streak |
|:--:|:--:|:--:|:--:|:--:|:--:|
| **495** | **218** | **209** | **76%** | **42** | **143 days** |

_1648 GitHub contributions in the last year · 93 in the last 7 days · 313 in the last 30._

## Bug reports

- [peft #4094](https://github.com/huggingface/peft/issues/4094): reduce_intruder_dimension does not transpose the delta weight for fan_in_fan_out (GPT-2 Conv1D) or nn.Embedding LoRA layers, so the rebuilt adapter is wrong.
- [flax #5594](https://github.com/google/flax/issues/5594): nnx.GRUCell is missing the b_hn bias that its docstring and linen.GRUCell both specify.
- [trl #7221](https://github.com/huggingface/trl/issues/7221): Reproduced NaN entropy for valid zero-probability tokens, including finite float16 inputs; PyTorch categorical entropy remains finite.

## Recent activity

| Date | Project | What | Status |
|---|---|---|---|
| 2026-11-01 | [Ray #67670](https://github.com/ray-project/ray/pull/67670) | Tuner.restore ignored max_concurrent_trials: errored and unfinished trials were re-queued straight into the controller, so all of them started at once | Open |
| 2026-11-01 | [DeepSpeed #8978](https://github.com/deepspeedai/DeepSpeed/pull/8978) | launcher_helper always exited 0, so under --launcher mpich a rank that crashed or was killed was reported as a success | Open |
| 2026-11-01 | [DeepSpeed #8977](https://github.com/deepspeedai/DeepSpeed/pull/8977) | With --venv_script, the pdsh runner's remote pkill pattern no longer named deepspeed.launcher.launch and the unquoted ; split the remote command, so ranks survived Ctrl-C | Open |
| 2026-11-01 | [unsloth-zoo #2351](https://github.com/unslothai/unsloth-zoo/pull/2351) | requires_grad_for_gradient_checkpointing re-registered a module's other forward hooks with always_call=False, so a hook that must run when forward raises (the float32 bias exit hook) went silent | Open |
| 2026-11-01 | [unsloth #16425](https://github.com/unslothai/unsloth/pull/16425) | get_chat_template(mapping=...) silently ignored the mapping whenever it kept the role key, so Llama 3.1 wrote human/gpt as headers and ChatML turned every turn into a system turn | Open |
| 2026-11-01 | [unsloth #16424](https://github.com/unslothai/unsloth/pull/16424) | unsloth-cli.py applied --chunk_size and --stride only to --raw_text_file, so --dataset notes.txt (or .md, .json, .jsonl) silently used 2048/512 | Open |
| 2026-10-31 | [unsloth-zoo #2327](https://github.com/unslothai/unsloth-zoo/pull/2327) | finetune_vision_layers = False still put LoRA on GIT's vision tower (12 extra Linears on a tiny GIT), because the get_peft_regex fallback drops the model-part requirement and GIT's decoder has no language tag | Open |
| 2026-10-31 | [DeepSpeed #8969](https://github.com/deepspeedai/DeepSpeed/pull/8969) | A blank or # line in .deepspeed_env aborted the launch with ValueError, and a commented-out # VAR=val line was exported as a variable named # VAR, because runner.py split every line on = and unpacked two values | Open |
| 2026-10-30 | [DeepSpeed #8960](https://github.com/deepspeedai/DeepSpeed/pull/8960) | sequence_tiled_compute(..., output_reduction="mean") rescaled the gradient of other terms summed into the same loss (x.grad error 0.75), because backward did incoming_grad /= shards in place on the tensor autograd shares across summed branches | Open |
| 2026-10-30 | [unsloth-zoo #2283](https://github.com/unslothai/unsloth-zoo/pull/2283) | merge_and_overwrite_lora on a GPT-2 Conv1D LoRA adapter crashed with Bad in-place call on rectangular layers or silently merged a transposed delta on square ones, because _merge_lora added B@A to the base weight as (out, in) while Conv1D adapters (fan_in_fan_out=True) store (in, out) | Open |
| 2026-10-30 | [Ray #67618](https://github.com/ray-project/ray/pull/67618) | A nested points_to_evaluate entry crashed on_trial_complete in BayesOptSearch with ValueError (Parameters' keys do not match the expected set of keys), because suggest stored the popped nested point while the optimizer registers flattened a/x keys | Open |
| 2026-10-30 | [Ray #67616](https://github.com/ray-project/ray/pull/67616) | A nested points_to_evaluate entry in OptunaSearch was silently ignored (Optuna sampled the parameter at random) or rejected with a misleading validate_warmstart error (Dim of point ... do not match), because the space is flattened to a/b keys but the points were stored as given | Open |
| 2026-10-29 | [Ray #67558](https://github.com/ray-project/ray/pull/67558) | tune.qrandint(0, 100, 10) in ZOOptSearch suggested values like 8, 16 and 65 and could never reach the inclusive upper bound 100, because convert_search_space dropped q for the Integer branch | Open |
| 2026-10-29 | [DeepSpeed #8947](https://github.com/deepspeedai/DeepSpeed/pull/8947) | generalized_jsd_loss reported a wrong valid_token_count and loss for bf16 and fp16 logits (bf16 rounded 97992 valid tokens to 97792; fp16 with more than 65504 returned int64 max and the loss collapsed to about 0), because it cast response_mask to the logits dtype before summing | Open |
| 2026-10-29 | [unsloth-zoo #2254](https://github.com/unslothai/unsloth-zoo/pull/2254) | The compiled LED encoder returned different hidden states from stock LED (max diff 0.025), because convert_attention_masks_to_bool rewrote LED's additive encoder mask into a boolean one that LED's non-SDPA Longformer encoder still reads additively | Open |
| 2026-10-28 | [vllm #64337](https://github.com/vllm-project/vllm/pull/64337) | A chat request (input_audio or audio_url) carrying a WAV cut to 30 bytes returned HTTP 500 instead of 400, because load_audio re-raised libsndfile's RuntimeError for any error code outside the format-detection ones | Open |
| 2026-10-28 | [unsloth-zoo #2214](https://github.com/unslothai/unsloth-zoo/pull/2214) | On transformers 4.52 to 4.57 the compiler silently dropped the causal mask for models that do not use SDPA (T5, mT5, UMT5, GPT-J, CodeGen, GPT-NeoX-Japanese, Bloom), so every position saw future tokens and training loss and generations were wrong with no error | Open |
| 2026-10-28 | [Ray #67509](https://github.com/ray-project/ray/pull/67509) | NevergradSearch returned nan for every tune.randn and tune.qrandn parameter, because the unbounded domain became ng.p.Scalar(lower=-inf, upper=inf), which starts at NaN on nevergrad 1.0.12 | Open |
| 2026-10-28 | [unsloth #15775](https://github.com/unslothai/unsloth/pull/15775) | The legacy unsloth-cli.py documents --dtype None (its own usage line; the help says None for auto detection), but on every non-MLX backend it crashed with an AssertionError, because the CLI passed the string "None" to FastLanguageModel.from_pretrained, which asserts dtype is None or a torch dtype | Open |

_Showing the 19 most recent. Open `index.html` for the full visual dashboard._

---
_Statuses are refreshed straight from the GitHub API, so this page reflects the live state of every pull request._
