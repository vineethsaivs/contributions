# Open-source contributions

_Vineeth Sai · [@vineethsaivs](https://github.com/vineethsaivs) · auto-updated after every contribution · last updated September 12, 2026 at 8:44 PM PT_

| PRs | Merged | Open | Merge rate | Projects | Streak |
|:--:|:--:|:--:|:--:|:--:|:--:|
| **277** | **108** | **133** | **75%** | **38** | **6 days** |

_26 in the last 7 days · 113 in the last 30._

## Recent activity

| Date | Project | What | Status |
|---|---|---|---|
| 2026-09-12 | [vllm #56647](https://github.com/vllm-project/vllm/pull/56647) | Serve benchmarks counted sequential requests in one second as concurrent | Open |
| 2026-09-12 | [DeepSpeed #8496](https://github.com/deepspeedai/DeepSpeed/pull/8496) | ZenFlow's low-precision Adam step counters stopped at 256 or 2048 | Open |
| 2026-09-12 | [DeepSpeed #8495](https://github.com/deepspeedai/DeepSpeed/pull/8495) | OneCycle silently replaced each Adam parameter group's beta2 with 0.99 | Open |
| 2026-09-12 | [unsloth #10842](https://github.com/unslothai/unsloth/pull/10842) | Q-GaLore advanced Adam bias correction twice per optimizer step | Open |
| 2026-09-12 | [unsloth #10841](https://github.com/unslothai/unsloth/pull/10841) | Q-GaLore quantization clipped single-sign groups and erased constant projection vectors | Open |
| 2026-09-12 | [unsloth-zoo #1194](https://github.com/unslothai/unsloth-zoo/pull/1194) | higher_precision_layernorms matched its float32 markers against the norm class plus a whole unrelated class, so Llama 4's neighbouring experts block upcast layernorm weights that should stay in float16 | Open |
| 2026-09-12 | [accelerate #4252](https://github.com/huggingface/accelerate/pull/4252) | DataLoaderShard took the same torch_device_mesh argument its sibling DataLoaderDispatcher honours, documented none of it, and never read it | Open |
| 2026-09-12 | [unsloth-zoo #1193](https://github.com/unslothai/unsloth-zoo/pull/1193) | an eight-branch chunked-prefill ladder was overwritten on the next line and only ever printed, so the startup line reported a number that never reached vLLM | Open |
| 2026-09-12 | [accelerate #4251](https://github.com/huggingface/accelerate/pull/4251) | Accelerator.__init__ accepted a split_batches argument it never read, so Accelerator(split_batches=True) configured nothing and warned about nothing while its three sibling kwargs already raised | Open |
| 2026-09-11 | [unsloth #10818](https://github.com/unslothai/unsloth/pull/10818) | the gradient-accumulation rewrite used octal escapes instead of group references, so the captured indents came back as control characters and the exec that follows could not parse the result | Open |
| 2026-09-11 | [unsloth #10816](https://github.com/unslothai/unsloth/pull/10816) | upload_to_huggingface took a method argument and formatted the model card with method empty, so every card it pushed read 'Uploaded  model' instead of naming the method | Open |
| 2026-09-11 | [DeepSpeed #8488](https://github.com/deepspeedai/DeepSpeed/pull/8488) | every _graph_replay copied only top-level tensors into the captured CUDA graph inputs, so SDXL's added_cond_kwargs dict was never refreshed and each image after the first replayed the first prompt's conditioning | Open |
| 2026-09-10 | [unsloth #10743](https://github.com/unslothai/unsloth/pull/10743) | test_raw_text_loader wrapped its whole body in try/except, so its 170 lines of assertions could never fail the suite | Open |
| 2026-09-10 | [unsloth #10742](https://github.com/unslothai/unsloth/pull/10742) | to_sharegpt read the inside of an escaped brace pair as a column name, so a prompt asking for JSON reported its own text as a missing dataset column | Open |
| 2026-09-10 | [unsloth #10741](https://github.com/unslothai/unsloth/pull/10741) | TextPreprocessor.clean_text deleted every non-ASCII character, so accented words lost their accents and a document in any non-Latin script came back empty | Open |
| 2026-09-10 | [unsloth #10682](https://github.com/unslothai/unsloth/pull/10682) | Stripping the template BOS from a Llama 2 style expression removed its opening braces, so the prompt rendered as literal Jinja source | Merged |
| 2026-09-10 | [unsloth #10681](https://github.com/unslothai/unsloth/pull/10681) | LongRope applied the long RoPE factor a token early, and that same length read a long cos/sin cache nothing had built | Open |

_Showing the 17 most recent. Open `index.html` for the full visual dashboard._

---
_Statuses are refreshed straight from the GitHub API, so this page reflects the live state of every pull request._
