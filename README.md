# Open-source contributions

_Vineeth Sai · [@vineethsaivs](https://github.com/vineethsaivs) · auto-updated after every contribution · last updated November 6, 2026 at 12:21 AM PT_

| PRs | Merged | Open | Merge rate | Projects | Streak |
|:--:|:--:|:--:|:--:|:--:|:--:|
| **509** | **229** | **212** | **77%** | **42** | **148 days** |

_1708 GitHub contributions in the last year · 72 in the last 7 days · 319 in the last 30._

## Bug reports

- [peft #4115](https://github.com/huggingface/peft/issues/4115): C3ALinear.forward rebinds x to each adapter's output, so with more than one active adapter the second one convolves the first one's result instead of the layer input.
- [peft #4094](https://github.com/huggingface/peft/issues/4094): reduce_intruder_dimension does not transpose the delta weight for fan_in_fan_out (GPT-2 Conv1D) or nn.Embedding LoRA layers, so the rebuilt adapter is wrong.
- [flax #5594](https://github.com/google/flax/issues/5594): nnx.GRUCell is missing the b_hn bias that its docstring and linen.GRUCell both specify.
- [trl #7221](https://github.com/huggingface/trl/issues/7221): Reproduced NaN entropy for valid zero-probability tokens, including finite float16 inputs; PyTorch categorical entropy remains finite.

## Recent activity

| Date | Project | What | Status |
|---|---|---|---|
| 2026-11-05 | [unsloth #16827](https://github.com/unslothai/unsloth/pull/16827) | `_configure_mlx_training_schedule` turned the warmup ratio into steps with `int(round(...))` and the eval ratio with `int(...)`, so a small ratio gave no warmup or an early eval, unlike transformers (`math.ceil`) | Open |
| 2026-11-05 | [unsloth-zoo #2419](https://github.com/unslothai/unsloth-zoo/pull/2419) | `grpo_entropy_bonus_weights` kept the pre-1.9.1 normalizer for the dapo, cispo and vespo entropy bonus, so on TRL 1.9.1 and 1.9.2 the bonus was off by `grad_accum / steps_per_generation` (x0.5 at 2 vs 4, x2 at 4 vs 2) | Open |
| 2026-11-05 | [Ray #67872](https://github.com/ray-project/ray/pull/67872) | `DistributeResources._get_multiplier` counted `increase_by` steps with float floor division, so `0.9 // 0.1` is 8.0 and one step was lost: a trial at 0.1 GPU with `increase_by={"GPU": 0.1}` stopped at 0.9 GPU of 1.0 | Open |
| 2026-11-04 | [Ray #67830](https://github.com/ray-project/ray/pull/67830) | `wrap_function.handle_output` skipped every falsy output, so a function trainable that returned or yielded `0` never reported that metric and the trial could never win `get_best_result` | Open |
| 2026-11-04 | [Ray #67829](https://github.com/ray-project/ray/pull/67829) | `tune.run` and `TuneConfig(max_concurrent_trials=N)` ignored the limit when `search_alg` was a user-built `BasicVariantGenerator`, so every trial ran at once (4 trials peaked together with a limit of 1) | Open |
| 2026-11-04 | [unsloth #16697](https://github.com/unslothai/unsloth/pull/16697) | `TextPreprocessor.add_structure_tokens` ran the heading regexes before wrapping fenced code, so a `# comment` inside a fenced python block became a `<|chapter|>` token and `##` became `<|section|>`, corrupting the code | Open |
| 2026-11-03 | [vllm #65477](https://github.com/vllm-project/vllm/pull/65477) | VLLM_FLOAT32_MATMUL_PRECISION is declared case_sensitive=False but returned the raw string, so HIGH passed validation and torch.set_float32_matmul_precision silently stayed on highest | Open |
| 2026-11-03 | [Ray #67751](https://github.com/ray-project/ray/pull/67751) | ExperimentPlateauStopper.__call__ kept a NaN in its top values, so the standard deviation was NaN, has_plateaued() was always False and the experiment never plateau-stopped | Open |
| 2026-11-03 | [Ray #67750](https://github.com/ray-project/ray/pull/67750) | _TrainingRunMetadata.update_metric took max(value, old) and min(value, old) with a NaN value, which returns NaN, so the next finite result overwrote the earlier best value with itself | Open |
| 2026-11-03 | [unsloth-zoo #2379](https://github.com/unslothai/unsloth-zoo/pull/2379) | unsloth_train compared the config dtype straight to torch.float16, but the config can hold the string "float16", so an fp16 model trained under bf16 autocast with no GradScaler | Merged |
| 2026-11-02 | [Ray #67712](https://github.com/ray-project/ray/pull/67712) | MedianStoppingRule.set_search_properties set its comparison operator unconditionally, so a rule with a metric but no mode silently became min and the check in on_trial_add never fired | Open |
| 2026-11-02 | [Ray #67711](https://github.com/ray-project/ray/pull/67711) | AsyncHyperBandScheduler computed its rung count with a float log ratio that lands just below the integer when max_t / min_t is an exact power of reduction_factor, so int() dropped the rung at max_t | Open |
| 2026-11-02 | [unsloth-zoo #2366](https://github.com/unslothai/unsloth-zoo/pull/2366) | UnslothForCausalLMLoss passed half-precision logits straight to F.cross_entropy when ignore_index != -100, where stock ForCausalLMLoss upcasts to float32 first, so an fp16 loss could overflow to inf | Merged |
| 2026-11-02 | [peft #4100](https://github.com/huggingface/peft/pull/4100) | reduce_intruder_dimension rebuilt lora_A and lora_B from the SVD of the delta weight without transposing it for fan_in_fan_out (GPT-2 Conv1D) and nn.Embedding layers, so a square Conv1D gave wrong output silently and other shapes failed in forward | Merged |
| 2026-11-01 | [Ray #67670](https://github.com/ray-project/ray/pull/67670) | Tuner.restore ignored max_concurrent_trials: errored and unfinished trials were re-queued straight into the controller, so all of them started at once | Open |
| 2026-11-01 | [DeepSpeed #8978](https://github.com/deepspeedai/DeepSpeed/pull/8978) | launcher_helper always exited 0, so under --launcher mpich a rank that crashed or was killed was reported as a success | Open |
| 2026-11-01 | [DeepSpeed #8977](https://github.com/deepspeedai/DeepSpeed/pull/8977) | With --venv_script, the pdsh runner's remote pkill pattern no longer named deepspeed.launcher.launch and the unquoted ; split the remote command, so ranks survived Ctrl-C | Open |
| 2026-11-01 | [unsloth-zoo #2351](https://github.com/unslothai/unsloth-zoo/pull/2351) | requires_grad_for_gradient_checkpointing re-registered a module's other forward hooks with always_call=False, so a hook that must run when forward raises (the float32 bias exit hook) went silent | Merged |
| 2026-11-01 | [unsloth #16425](https://github.com/unslothai/unsloth/pull/16425) | get_chat_template(mapping=...) silently ignored the mapping whenever it kept the role key, so Llama 3.1 wrote human/gpt as headers and ChatML turned every turn into a system turn | Open |
| 2026-11-01 | [unsloth #16424](https://github.com/unslothai/unsloth/pull/16424) | unsloth-cli.py applied --chunk_size and --stride only to --raw_text_file, so --dataset notes.txt (or .md, .json, .jsonl) silently used 2048/512 | Merged |

_Showing the 20 most recent. Open `index.html` for the full visual dashboard._

---
_Statuses are refreshed straight from the GitHub API, so this page reflects the live state of every pull request._
