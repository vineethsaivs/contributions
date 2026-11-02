# Open-source contributions

_Vineeth Sai · [@vineethsaivs](https://github.com/vineethsaivs) · auto-updated after every contribution · last updated November 2, 2026 at 1:53 PM PT_

| PRs | Merged | Open | Merge rate | Projects | Streak |
|:--:|:--:|:--:|:--:|:--:|:--:|
| **499** | **219** | **212** | **76%** | **42** | **144 days** |

_1663 GitHub contributions in the last year · 86 in the last 7 days · 322 in the last 30._

## Bug reports

- [peft #4094](https://github.com/huggingface/peft/issues/4094): reduce_intruder_dimension does not transpose the delta weight for fan_in_fan_out (GPT-2 Conv1D) or nn.Embedding LoRA layers, so the rebuilt adapter is wrong.
- [flax #5594](https://github.com/google/flax/issues/5594): nnx.GRUCell is missing the b_hn bias that its docstring and linen.GRUCell both specify.
- [trl #7221](https://github.com/huggingface/trl/issues/7221): Reproduced NaN entropy for valid zero-probability tokens, including finite float16 inputs; PyTorch categorical entropy remains finite.

## Recent activity

| Date | Project | What | Status |
|---|---|---|---|
| 2026-11-02 | [Ray #67712](https://github.com/ray-project/ray/pull/67712) | MedianStoppingRule.set_search_properties set its comparison operator unconditionally, so a rule with a metric but no mode silently became min and the check in on_trial_add never fired | Open |
| 2026-11-02 | [Ray #67711](https://github.com/ray-project/ray/pull/67711) | AsyncHyperBandScheduler computed its rung count with a float log ratio that lands just below the integer when max_t / min_t is an exact power of reduction_factor, so int() dropped the rung at max_t | Open |
| 2026-11-02 | [unsloth-zoo #2366](https://github.com/unslothai/unsloth-zoo/pull/2366) | UnslothForCausalLMLoss passed half-precision logits straight to F.cross_entropy when ignore_index != -100, where stock ForCausalLMLoss upcasts to float32 first, so an fp16 loss could overflow to inf | Open |
| 2026-11-02 | [peft #4100](https://github.com/huggingface/peft/pull/4100) | reduce_intruder_dimension rebuilt lora_A and lora_B from the SVD of the delta weight without transposing it for fan_in_fan_out (GPT-2 Conv1D) and nn.Embedding layers, so a square Conv1D gave wrong output silently and other shapes failed in forward | Open |
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

_Showing the 16 most recent. Open `index.html` for the full visual dashboard._

---
_Statuses are refreshed straight from the GitHub API, so this page reflects the live state of every pull request._
