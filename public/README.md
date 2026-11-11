# Open-source contributions

_Vineeth Sai · [@vineethsaivs](https://github.com/vineethsaivs) · auto-updated after every contribution · last updated November 11, 2026 at 9:46 AM PT_

| PRs | Merged | Open | Merge rate | Projects | Streak |
|:--:|:--:|:--:|:--:|:--:|:--:|
| **529** | **237** | **223** | **77%** | **42** | **153 days** |

_1768 GitHub contributions in the last year · 71 in the last 7 days · 332 in the last 30._

## Bug reports

- [peft #4115](https://github.com/huggingface/peft/issues/4115): C3ALinear.forward rebinds x to each adapter's output, so with more than one active adapter the second one convolves the first one's result instead of the layer input.
- [peft #4094](https://github.com/huggingface/peft/issues/4094): reduce_intruder_dimension does not transpose the delta weight for fan_in_fan_out (GPT-2 Conv1D) or nn.Embedding LoRA layers, so the rebuilt adapter is wrong.
- [flax #5594](https://github.com/google/flax/issues/5594): nnx.GRUCell is missing the b_hn bias that its docstring and linen.GRUCell both specify.
- [trl #7221](https://github.com/huggingface/trl/issues/7221): Reproduced NaN entropy for valid zero-probability tokens, including finite float16 inputs; PyTorch categorical entropy remains finite.

## Recent activity

| Date | Project | What | Status |
|---|---|---|---|
| 2026-11-11 | [tunix #3293](https://github.com/google/tunix/pull/3293) | DPO/ORPO string inputs no longer put a BOS token at the start of chosen and rejected responses. | Open |
| 2026-11-11 | [Ray #68073](https://github.com/ray-project/ray/pull/68073) | tune.with_parameters now wraps a generator function trainable in a generator function, so its yielded results are reported instead of erroring. | Open |
| 2026-11-11 | [unsloth #17537](https://github.com/unslothai/unsloth/pull/17537) | Add luspo to the loss types that log clip_ratio/* metrics in the patched GRPO compute_loss. | Open |
| 2026-11-10 | [unsloth #17438](https://github.com/unslothai/unsloth/pull/17438) | `push_to_hub_gguf(tags=...)` sent the tags through `api.add_tags`, which `HfApi` does not have, behind a bare `except: pass`, so they never reached the Hub, and it extended the caller's list in place | Open |
| 2026-11-10 | [unsloth-zoo #2473](https://github.com/unslothai/unsloth-zoo/pull/2473) | `add_llama_cpp_system_message(inplace=False)` rebuilt a leading system message from its own content, so the llama.cpp text it exists to append was lost, and a `None` messages list hit `len()` before the `None` check | Open |
| 2026-11-10 | [unsloth #17436](https://github.com/unslothai/unsloth/pull/17436) | Studio's diffusion dataset readers cut each `metadata.jsonl` or `captions.jsonl` row with `str.splitlines()`, which also breaks at U+2028, U+2029 and U+0085, so a caption holding one was split mid-string, failed `json.loads` and was skipped with no error | Open |
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

_Showing the 17 most recent. Open `index.html` for the full visual dashboard._

---
_Statuses are refreshed straight from the GitHub API, so this page reflects the live state of every pull request._
