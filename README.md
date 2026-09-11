# Open-source contributions

_Vineeth Sai · [@vineethsaivs](https://github.com/vineethsaivs) · auto-updated after every contribution · last updated September 11, 2026 at 1:57 PM PT_

| PRs | Merged | Open | Merge rate | Projects | Streak |
|:--:|:--:|:--:|:--:|:--:|:--:|
| **268** | **106** | **126** | **75%** | **42** | **5 days** |

_17 in the last 7 days · 109 in the last 30._

## Recent activity

| Date | Project | What | Status |
|---|---|---|---|
| 2026-09-11 | [unsloth #10818](https://github.com/unslothai/unsloth/pull/10818) | the gradient-accumulation rewrite used octal escapes instead of group references, so the captured indents came back as control characters and the exec that follows could not parse the result | Open |
| 2026-09-11 | [unsloth #10816](https://github.com/unslothai/unsloth/pull/10816) | upload_to_huggingface took a method argument and formatted the model card with method empty, so every card it pushed read 'Uploaded  model' instead of naming the method | Open |
| 2026-09-11 | [DeepSpeed #8488](https://github.com/deepspeedai/DeepSpeed/pull/8488) | every _graph_replay copied only top-level tensors into the captured CUDA graph inputs, so SDXL's added_cond_kwargs dict was never refreshed and each image after the first replayed the first prompt's conditioning | Open |
| 2026-09-10 | [unsloth #10743](https://github.com/unslothai/unsloth/pull/10743) | test_raw_text_loader wrapped its whole body in try/except, so its 170 lines of assertions could never fail the suite | Open |
| 2026-09-10 | [unsloth #10742](https://github.com/unslothai/unsloth/pull/10742) | to_sharegpt read the inside of an escaped brace pair as a column name, so a prompt asking for JSON reported its own text as a missing dataset column | Open |
| 2026-09-10 | [unsloth #10741](https://github.com/unslothai/unsloth/pull/10741) | TextPreprocessor.clean_text deleted every non-ASCII character, so accented words lost their accents and a document in any non-Latin script came back empty | Open |
| 2026-09-10 | [unsloth #10682](https://github.com/unslothai/unsloth/pull/10682) | Stripping the template BOS from a Llama 2 style expression removed its opening braces, so the prompt rendered as literal Jinja source | Open |
| 2026-09-10 | [unsloth #10681](https://github.com/unslothai/unsloth/pull/10681) | LongRope applied the long RoPE factor a token early, and that same length read a long cos/sin cache nothing had built | Open |
| 2026-09-09 | [datasets #8594](https://github.com/huggingface/datasets/pull/8594) | IterableDatasetDict.shuffle could not pass max_buffer_input_shards, so shuffling a streamed dataset dict raised TypeError | Merged |
| 2026-09-09 | [PyTorch Lightning #21945](https://github.com/Lightning-AI/pytorch-lightning/pull/21945) | Fabric's call tracker leaked a forward hook per submodule on every failed call and carried its verdict into the next call | Open |
| 2026-09-09 | [PyTorch Lightning #21944](https://github.com/Lightning-AI/pytorch-lightning/pull/21944) | Setting an attribute on a Fabric-wrapped model ran the model's own property getter, so a getter that guards an uninitialized value raised out of the assignment | Open |
| 2026-09-08 | [sentence-transformers #3993](https://github.com/huggingface/sentence-transformers/pull/3993) | `CachedGISTEmbedLoss` still read `tokenizer.vocab` after PR #3226 moved only the uncached loss to `get_vocab()`, so it raised AttributeError on GPT-2, XLM and Flaubert tokenizers | Merged |
| 2026-09-08 | [datasets #8588](https://github.com/huggingface/datasets/pull/8588) | `TranslationVariableLanguages` declares `languages` optional but `encode_example` built `set(self.languages)` before its own None guard, so the default feature raised TypeError on every example | Open |
| 2026-09-08 | [Ray #65991](https://github.com/ray-project/ray/pull/65991) | With `constant_grid_search=True` every grid variant shared one `resolved_vars` dict, so all trials reported the last grid value as their hyperparameters while each ran its own correct config | Open |
| 2026-09-07 | [accelerate #4228](https://github.com/huggingface/accelerate/pull/4228) | `split_between_processes(apply_padding=True)` raised TypeError for a tuple, a documented input type, because the slice keeps the tuple type and the padding was always a list | Closed, maintainer declined the fix |
| 2026-09-07 | [DeepSpeed #8455](https://github.com/deepspeedai/DeepSpeed/pull/8455) | With `partition_activations` on, `merge_tensors` handed the activation-checkpoint recompute a stray `None` after every non-tensor argument, shifting every argument that followed it | Open |
| 2026-09-07 | [PyTorch Lightning #21936](https://github.com/Lightning-AI/pytorch-lightning/pull/21936) | `ckpt_path="last"` silently resumed from nothing whenever `ModelCheckpoint` saved to a remote filesystem: `os.path.normpath` stripped the protocol off the paths `fs.ls` returned, so every candidate resolved against local disk and was dropped | Open |

_Showing the 17 most recent. Open `index.html` for the full visual dashboard._

---
_Statuses are refreshed straight from the GitHub API, so this page reflects the live state of every pull request._
