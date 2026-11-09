# Open-source contributions

_Vineeth Sai · [@vineethsaivs](https://github.com/vineethsaivs) · auto-updated after every contribution · last updated November 9, 2026 at 12:07 PM PT_

| PRs | Merged | Open | Merge rate | Projects | Streak |
|:--:|:--:|:--:|:--:|:--:|:--:|
| **523** | **236** | **218** | **77%** | **42** | **151 days** |

_1751 GitHub contributions in the last year · 86 in the last 7 days · 332 in the last 30._

## Bug reports

- [peft #4115](https://github.com/huggingface/peft/issues/4115): C3ALinear.forward rebinds x to each adapter's output, so with more than one active adapter the second one convolves the first one's result instead of the layer input.
- [peft #4094](https://github.com/huggingface/peft/issues/4094): reduce_intruder_dimension does not transpose the delta weight for fan_in_fan_out (GPT-2 Conv1D) or nn.Embedding LoRA layers, so the rebuilt adapter is wrong.
- [flax #5594](https://github.com/google/flax/issues/5594): nnx.GRUCell is missing the b_hn bias that its docstring and linen.GRUCell both specify.
- [trl #7221](https://github.com/huggingface/trl/issues/7221): Reproduced NaN entropy for valid zero-probability tokens, including finite float16 inputs; PyTorch categorical entropy remains finite.

## Recent activity

| Date | Project | What | Status |
|---|---|---|---|
| 2026-11-09 | [unsloth #17316](https://github.com/unslothai/unsloth/pull/17316) | `save_pretrained_gguf` keeps the BOS in Llama 3's chat template while its log says it removed it, because `_strip_bos_from_chat_template_text` only matched `{{ bos_token }}` and `{{ bos_token + ... }}`, not Llama 3's `{% set content = bos_token + content %}` | Open |
| 2026-11-09 | [unsloth #17307](https://github.com/unslothai/unsloth/pull/17307) | A local decision dataset in JSON Lines failed with `Invalid JSON ... Unterminated string` when a string held U+2028, U+2029 or U+0085, because `_read_local_rows` split the file with `str.splitlines()`, which also breaks rows at those characters | Open |
| 2026-11-09 | [unsloth #17303](https://github.com/unslothai/unsloth/pull/17303) | Studio clamped a Train Split Start at or past the end of a non-streaming dataset to the last row, so the run trained on a single row ("Sliced dataset to 1 rows (indices 9-9)") and, with `max_steps`, looped it for the whole run with no error | Open |
| 2026-11-08 | [unsloth #17176](https://github.com/unslothai/unsloth/pull/17176) | `get_chat_template(tok, "llama-3.1")` raised `TypeError` and `"gpt-oss"` raised `UndefinedError` on any message carrying `tool_calls: None`, which `datasets` fills into every plain row of a tool-calling dataset, because both templates tested whether the key exists | Open |
| 2026-11-08 | [unsloth #17175](https://github.com/unslothai/unsloth/pull/17175) | `get_chat_template(tok, "qwen3")` raised `TypeError` on an assistant tool-call turn whose `content` is null (and `UndefinedError` when it is missing), the usual OpenAI tool-call shape, because `qwen3_template` tested `'</think>' in message.content` on the raw value | Open |
| 2026-11-08 | [unsloth-zoo #2451](https://github.com/unslothai/unsloth-zoo/pull/2451) | After `requires_grad_for_gradient_checkpointing`, `handle.remove()` on a user's forward hook did nothing and the hook kept running, because the cleanup replaced each module's hook dict and re-registered the kept hooks under new ids | Open |
| 2026-11-08 | [flax #5645](https://github.com/google/flax/pull/5645) | nnx.GRUCell was missing the b_hn bias its own docstring specifies; replaces #5595, which GitHub closed when main was force-pushed to its branch | Open |
| 2026-11-07 | [unsloth-zoo #2449](https://github.com/unslothai/unsloth-zoo/pull/2449) | `create_locked_down_function` (and `load_single_function`, `validate_single_function_source`) refused a generated function like `def strategy(board, penalty = -1)` with "Only simple literal default argument values are allowed.", while `penalty = 1` was accepted | Open |
| 2026-11-07 | [unsloth #17116](https://github.com/unslothai/unsloth/pull/17116) | `unsloth train --num-epochs 0` (or `num_epochs: 0` in a config) with the default `max_steps: 0` was accepted, so the run trained 0 steps with the HF Trainer and exactly one step on MLX, while Studio refuses the same pair | Open |
| 2026-11-07 | [unsloth-zoo #2448](https://github.com/unslothai/unsloth-zoo/pull/2448) | The two-line `sqrt(mean(X**2))` rewrite in `higher_precision_sqrt_mean` emitted `.to(X.dtype)` one parenthesis too early, so the sqrt still ran in float16 and a float32 mean-square above 65504 became inf and the renormalised hidden state came out 0 | Open |
| 2026-11-07 | [unsloth #17115](https://github.com/unslothai/unsloth/pull/17115) | `unsloth-cli.py --use_gradient_checkpointing false` (also `true`, `0`, `none`) died with an AssertionError after the model loaded, because the flag is a plain string handed to `get_peft_model`, which only takes `True`, `False` or `"unsloth"` | Open |
| 2026-11-06 | [unsloth-zoo #2441](https://github.com/unslothai/unsloth-zoo/pull/2441) | `load_vllm` set `VLLM_USE_FLASHINFER_SAMPLER=1` on every GPU once vLLM was 0.11 or newer, and from vLLM 0.24 engine init raises when FlashInfer rejects the GPU, so `fast_inference=True` failed on a Colab T4 | Merged |
| 2026-11-06 | [unsloth #16933](https://github.com/unslothai/unsloth/pull/16933) | `save_pretrained_merged(..., save_method="Merged_16bit")` (also `"merged 16bit"`, `"merged-16bit"`) wrote the weights and tokenizer but no `config.json` or `generation_config.json`, because `unsloth_generic_save` forwarded `save_method` verbatim to a merge that compares the exact string | Open |
| 2026-11-06 | [unsloth #16932](https://github.com/unslothai/unsloth/pull/16932) | `get_chat_template(tok, "qwen-2.5", system_message=...)` only applied the chosen system message to rows without `tools`, because the tools branch of `qwen25_template` hardcoded Qwen's default persona | Open |
| 2026-11-05 | [unsloth #16827](https://github.com/unslothai/unsloth/pull/16827) | `_configure_mlx_training_schedule` turned the warmup ratio into steps with `int(round(...))` and the eval ratio with `int(...)`, so a small ratio gave no warmup or an early eval, unlike transformers (`math.ceil`) | Merged |
| 2026-11-05 | [unsloth-zoo #2419](https://github.com/unslothai/unsloth-zoo/pull/2419) | `grpo_entropy_bonus_weights` kept the pre-1.9.1 normalizer for the dapo, cispo and vespo entropy bonus, so on TRL 1.9.1 and 1.9.2 the bonus was off by `grad_accum / steps_per_generation` (x0.5 at 2 vs 4, x2 at 4 vs 2) | Merged |
| 2026-11-05 | [Ray #67872](https://github.com/ray-project/ray/pull/67872) | `DistributeResources._get_multiplier` counted `increase_by` steps with float floor division, so `0.9 // 0.1` is 8.0 and one step was lost: a trial at 0.1 GPU with `increase_by={"GPU": 0.1}` stopped at 0.9 GPU of 1.0 | Open |

_Showing the 17 most recent. Open `index.html` for the full visual dashboard._

---
_Statuses are refreshed straight from the GitHub API, so this page reflects the live state of every pull request._
