# Open-source contributions

_Vineeth Sai · [@vineethsaivs](https://github.com/vineethsaivs) · auto-updated after every contribution · last updated September 9, 2026 at 10:48 AM PT_

| PRs | Merged | Open | Merge rate | Projects | Streak |
|:--:|:--:|:--:|:--:|:--:|:--:|
| **260** | **101** | **125** | **75%** | **42** | **3 days** |

_23 in the last 7 days · 106 in the last 30._

## Recent activity

| Date | Project | What | Status |
|---|---|---|---|
| 2026-09-09 | [datasets #8594](https://github.com/huggingface/datasets/pull/8594) | IterableDatasetDict.shuffle could not pass max_buffer_input_shards, so shuffling a streamed dataset dict raised TypeError | Open |
| 2026-09-09 | [PyTorch Lightning #21945](https://github.com/Lightning-AI/pytorch-lightning/pull/21945) | Fabric's call tracker leaked a forward hook per submodule on every failed call and carried its verdict into the next call | Open |
| 2026-09-09 | [PyTorch Lightning #21944](https://github.com/Lightning-AI/pytorch-lightning/pull/21944) | Setting an attribute on a Fabric-wrapped model ran the model's own property getter, so a getter that guards an uninitialized value raised out of the assignment | Open |
| 2026-09-08 | [sentence-transformers #3993](https://github.com/huggingface/sentence-transformers/pull/3993) | `CachedGISTEmbedLoss` still read `tokenizer.vocab` after PR #3226 moved only the uncached loss to `get_vocab()`, so it raised AttributeError on GPT-2, XLM and Flaubert tokenizers | Open |
| 2026-09-08 | [datasets #8588](https://github.com/huggingface/datasets/pull/8588) | `TranslationVariableLanguages` declares `languages` optional but `encode_example` built `set(self.languages)` before its own None guard, so the default feature raised TypeError on every example | Open |
| 2026-09-08 | [Ray #65991](https://github.com/ray-project/ray/pull/65991) | With `constant_grid_search=True` every grid variant shared one `resolved_vars` dict, so all trials reported the last grid value as their hyperparameters while each ran its own correct config | Open |
| 2026-09-07 | [accelerate #4228](https://github.com/huggingface/accelerate/pull/4228) | `split_between_processes(apply_padding=True)` raised TypeError for a tuple, a documented input type, because the slice keeps the tuple type and the padding was always a list | Closed, maintainer declined the fix |
| 2026-09-07 | [DeepSpeed #8455](https://github.com/deepspeedai/DeepSpeed/pull/8455) | With `partition_activations` on, `merge_tensors` handed the activation-checkpoint recompute a stray `None` after every non-tensor argument, shifting every argument that followed it | Open |
| 2026-09-07 | [PyTorch Lightning #21936](https://github.com/Lightning-AI/pytorch-lightning/pull/21936) | `ckpt_path="last"` silently resumed from nothing whenever `ModelCheckpoint` saved to a remote filesystem: `os.path.normpath` stripped the protocol off the paths `fs.ls` returned, so every candidate resolved against local disk and was dropped | Open |
| 2026-09-04 | [Ray #65957](https://github.com/ray-project/ray/pull/65957) | `MedianStoppingRule` counts a trial with no result in the averaging window as a sample; `np.mean([])` is nan, the median becomes nan, and nan compares worse than every real score, so one such trial stops all the others | Open |
| 2026-09-04 | [sentence-transformers #3984](https://github.com/huggingface/sentence-transformers/pull/3984) | Four docstrings state the same CoSENT objective and two invert the difference; each wrong one sits on a base class or subclass of a right one, running identical code | Merged |
| 2026-09-04 | [PyTorch Lightning #21931](https://github.com/Lightning-AI/pytorch-lightning/pull/21931) | The lr_finder ladder is not evenly spaced: the first step is twice as wide as the rest in linear mode and the square of the rest in exponential mode, and one rung is never visited | Open |
| 2026-09-04 | [TRL #7069](https://github.com/huggingface/trl/pull/7069) | `compute_flops_per_token` raises `AttributeError` on Mixtral and Qwen2-MoE, two of the three MoE families its docstring names, and its MoE-layer rule is off by one | Open |
| 2026-09-04 | [DeepSpeed #8419](https://github.com/deepspeedai/DeepSpeed/pull/8419) | Four flop counters in the profiler count the wrong element set: `F.linear` never charged its bias, `matmul` counted a dimension its output does not have for 1-D operands and dropped broadcast batch dims, and both `addmm` counters charged the bias over its own shape | Open |
| 2026-09-04 | [Hugging Face datasets #8564](https://github.com/huggingface/datasets/pull/8564) | `Image`, `Pdf`, `Nifti` and `Video` document `X(decode=True, id=None)` as their repr, and all four declare `id` with `repr=False`, so none of them can print it; `video.py` also carries an unterminated string literal in its last example | Open |
| 2026-09-04 | [Unsloth #10304](https://github.com/unslothai/unsloth/pull/10304) | `push_to_ollama` calls `create_ollama_modelfile` with the `gguf_location=` keyword it lost in a signature change and omits both required arguments, so every call raises TypeError before reaching Ollama | Merged |
| 2026-09-04 | [DeepSpeed #8413](https://github.com/deepspeedai/DeepSpeed/pull/8413) | `DSVAE.forward` tests `cuda_graph_created`, a flag only `DSUNet` sets, so the default `enable_cuda_graph=True` path raises AttributeError; `_forward` is copied from the UNet wrapper and binds a VAE's arguments to the wrong parameters; `_decode` accepts `generator` and drops it, which every diffusers pipeline passes | Open |
| 2026-09-04 | [Ray #65918](https://github.com/ray-project/ray/pull/65918) | resubmit of #65008, which the stale bot auto-closed while the fix was still valid: ASHA's callers apply `self._metric_op` before `_Bracket.on_result` sees the value, so a `None` metric raises TypeError before reaching the branch that exists to warn and keep the trial running | Open |

_Showing the 18 most recent. Open `index.html` for the full visual dashboard._

---
_Statuses are refreshed straight from the GitHub API, so this page reflects the live state of every pull request._
