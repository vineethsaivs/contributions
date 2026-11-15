# Open-source contributions

_Vineeth Sai · [@vineethsaivs](https://github.com/vineethsaivs) · auto-updated after every contribution · last updated November 15, 2026 at 2:14 AM PT_

| PRs | Merged | Open | Merge rate | Projects | Streak |
|:--:|:--:|:--:|:--:|:--:|:--:|
| **540** | **256** | **213** | **78%** | **42** | **157 days** |

_1831 GitHub contributions in the last year · 91 in the last 7 days · 354 in the last 30._

## Bug reports

- [peft #4115](https://github.com/huggingface/peft/issues/4115): C3ALinear.forward rebinds x to each adapter's output, so with more than one active adapter the second one convolves the first one's result instead of the layer input.
- [peft #4094](https://github.com/huggingface/peft/issues/4094): reduce_intruder_dimension does not transpose the delta weight for fan_in_fan_out (GPT-2 Conv1D) or nn.Embedding LoRA layers, so the rebuilt adapter is wrong.
- [flax #5594](https://github.com/google/flax/issues/5594): nnx.GRUCell is missing the b_hn bias that its docstring and linen.GRUCell both specify.
- [trl #7221](https://github.com/huggingface/trl/issues/7221): Reproduced NaN entropy for valid zero-probability tokens, including finite float16 inputs; PyTorch categorical entropy remains finite.

## Recent activity

| Date | Project | What | Status |
|---|---|---|---|
| 2026-11-15 | [flax #5651](https://github.com/google/flax/pull/5651) | nnx.SimpleCell no longer forces dtype=float32; it infers from inputs and params like the other cells and linen. | Open |
| 2026-11-15 | [unsloth-zoo #2518](https://github.com/unslothai/unsloth-zoo/pull/2518) | sft_prepare_dataset now cuts prompt/completion rows by truncation_mode and treats max_length=None as no limit, like messages rows. | Open |
| 2026-11-15 | [unsloth #17810](https://github.com/unslothai/unsloth/pull/17810) | FastSentenceTransformer.get_peft_model (fast encoder path) now forwards exclude_modules, lora_bias, rank_pattern and every other LoraConfig kwarg, and refuses aLoRA. | Open |
| 2026-11-14 | [trl #8376](https://github.com/huggingface/trl/pull/8376) | compute_flops_per_token used the wrong MoE sparse-layer rule for qwen3_moe (off by one, ignored mlp_only_layers); replaces closed #7069. | Closed on process, fix correct |
| 2026-11-13 | [Ray #68119](https://github.com/ray-project/ray/pull/68119) | MaximumIterationStopper uses the reported training_iteration, so replayed iterations after a checkpoint restore are not counted twice. | Open |
| 2026-11-13 | [unsloth-zoo #2487](https://github.com/unslothai/unsloth-zoo/pull/2487) | sft_prepare_dataset now json-loads a string `tools` value in the prompt/completion path, as the messages path and TRL do. | Merged |
| 2026-11-13 | [unsloth #17657](https://github.com/unslothai/unsloth/pull/17657) | Scale the Falcon H1 attention input by attention_in_multiplier in the decoder layer forward, as transformers and Unsloth's decode loop do | Merged |
| 2026-11-12 | [optax #1883](https://github.com/google-deepmind/optax/pull/1883) | optax.sm3 now accepts a learning rate schedule instead of raising TypeError. | Open |
| 2026-11-12 | [Ray #68108](https://github.com/ray-project/ray/pull/68108) | Fix the inverted None check in TuneReporterBase.set_start_time so the passed start_time is kept. | Open |
| 2026-11-12 | [unsloth #17604](https://github.com/unslothai/unsloth/pull/17604) | Raise a ValueError when loraplus_lr_ratio and q_galore_config are both set, since the ratio was silently ignored. | Merged |
| 2026-11-11 | [vllm #67101](https://github.com/vllm-project/vllm/pull/67101) | pythonic and llama4_pythonic streaming no longer drop assistant text that starts with [ but is not a tool call. | Open |
| 2026-11-11 | [tunix #3293](https://github.com/google/tunix/pull/3293) | DPO/ORPO string inputs no longer put a BOS token at the start of chosen and rejected responses. | Open |
| 2026-11-11 | [Ray #68073](https://github.com/ray-project/ray/pull/68073) | tune.with_parameters now wraps a generator function trainable in a generator function, so its yielded results are reported instead of erroring. | Open |
| 2026-11-11 | [unsloth #17537](https://github.com/unslothai/unsloth/pull/17537) | Add luspo to the loss types that log clip_ratio/* metrics in the patched GRPO compute_loss. | Merged |
| 2026-11-10 | [unsloth #17438](https://github.com/unslothai/unsloth/pull/17438) | `push_to_hub_gguf(tags=...)` sent the tags through `api.add_tags`, which `HfApi` does not have, behind a bare `except: pass`, so they never reached the Hub, and it extended the caller's list in place | Merged |
| 2026-11-10 | [unsloth-zoo #2473](https://github.com/unslothai/unsloth-zoo/pull/2473) | `add_llama_cpp_system_message(inplace=False)` rebuilt a leading system message from its own content, so the llama.cpp text it exists to append was lost, and a `None` messages list hit `len()` before the `None` check | Merged |
| 2026-11-10 | [unsloth #17436](https://github.com/unslothai/unsloth/pull/17436) | Studio's diffusion dataset readers cut each `metadata.jsonl` or `captions.jsonl` row with `str.splitlines()`, which also breaks at U+2028, U+2029 and U+0085, so a caption holding one was split mid-string, failed `json.loads` and was skipped with no error | Merged |

_Showing the 17 most recent. Open `index.html` for the full visual dashboard._

---
_Statuses are refreshed straight from the GitHub API, so this page reflects the live state of every pull request._
