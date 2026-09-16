# Open-source contributions

_Vineeth Sai · [@vineethsaivs](https://github.com/vineethsaivs) · auto-updated after every contribution · last updated September 16, 2026 at 1:17 PM PT_

| PRs | Merged | Open | Merge rate | Projects | Streak |
|:--:|:--:|:--:|:--:|:--:|:--:|
| **326** | **129** | **156** | **76%** | **39** | **10 days** |

_66 in the last 7 days · 150 in the last 30._

## Bug reports

- [trl #7221](https://github.com/huggingface/trl/issues/7221): Reproduced NaN entropy for valid zero-probability tokens, including finite float16 inputs; PyTorch categorical entropy remains finite.

## Recent activity

| Date | Project | What | Status |
|---|---|---|---|
| 2026-09-16 | [unsloth-zoo #1262](https://github.com/unslothai/unsloth-zoo/pull/1262) | Keep GRPO KL metrics finite for fully masked completions | Open |
| 2026-09-16 | [unsloth-zoo #1261](https://github.com/unslothai/unsloth-zoo/pull/1261) | Apply MLX clipping scales before narrowing to fp16 | Open |
| 2026-09-16 | [accelerate #4274](https://github.com/huggingface/accelerate/pull/4274) | Return the wrapped optimizer step result | Open |
| 2026-09-16 | [DeepSpeed #8553](https://github.com/deepspeedai/DeepSpeed/pull/8553) | Accept NumPy integer indices in indexed datasets | Open |
| 2026-09-16 | [DeepSpeed #8552](https://github.com/deepspeedai/DeepSpeed/pull/8552) | Preserve convolution shapes and scaling in Muon updates | Open |
| 2026-09-15 | [unsloth-zoo #1241](https://github.com/unslothai/unsloth-zoo/pull/1241) | Keep DiscoPOP loss finite for large negative margins | Open |
| 2026-09-15 | [unsloth-zoo #1240](https://github.com/unslothai/unsloth-zoo/pull/1240) | Preserve small reverse-KL penalties in GRPO | Open |
| 2026-09-15 | [DeepSpeed #8533](https://github.com/deepspeedai/DeepSpeed/pull/8533) | Normalize Gram Newton-Schulz inputs before casting to fp16 | Open |
| 2026-09-15 | [sentence-transformers #4033](https://github.com/huggingface/sentence-transformers/pull/4033) | Keep Euclidean similarity gradients finite at zero distance | Open |
| 2026-09-15 | [sentence-transformers #4032](https://github.com/huggingface/sentence-transformers/pull/4032) | Return zero ranking loss when no label pairs are ordered | Open |
| 2026-09-15 | [vllm #57090](https://github.com/vllm-project/vllm/pull/57090) | Draft: [Bugfix][Benchmark] Keep all requests in prefix-repetition samples | Open |
| 2026-09-15 | [accelerate #4268](https://github.com/huggingface/accelerate/pull/4268) | Keep cached buffers registered as buffers | Open |
| 2026-09-15 | [unsloth-zoo #1237](https://github.com/unslothai/unsloth-zoo/pull/1237) | Keep negative embedding rows classified as trained | Merged |
| 2026-09-15 | [DeepSpeed #8530](https://github.com/deepspeedai/DeepSpeed/pull/8530) | Fix ZeRO-3 checkpoint conversion with --debug | Open |
| 2026-09-15 | [litellm #41286](https://github.com/BerriAI/litellm/pull/41286) | Draft: fix(proxy): count Gemini contents in local token estimates | Open |
| 2026-09-15 | [sentence-transformers #4028](https://github.com/huggingface/sentence-transformers/pull/4028) | Group tied scores when evaluating paraphrase mining | Merged |
| 2026-09-15 | [accelerate #4267](https://github.com/huggingface/accelerate/pull/4267) | Filter nonpersistent buffers by their qualified names | Open |
| 2026-09-15 | [unsloth #11040](https://github.com/unslothai/unsloth/pull/11040) | Count the final EOS token within the raw-text chunk budget | Open |
| 2026-09-15 | [unsloth #11039](https://github.com/unslothai/unsloth/pull/11039) | Match stopping criteria separately for each generated sequence | Merged |
| 2026-09-15 | [DeepSpeed #8529](https://github.com/deepspeedai/DeepSpeed/pull/8529) | Keep Random-LTD sequence lengths above the configured minimum | Open |
| 2026-09-15 | [DeepSpeed #8528](https://github.com/deepspeedai/DeepSpeed/pull/8528) | Keep tensor scheduler bounds fixed across LR updates | Open |
| 2026-09-15 | [crewai #7471](https://github.com/crewAIInc/crewAI/pull/7471) | Draft: fix(rag): enforce chunk size and overlap when merging splits | Open |

_Showing the 22 most recent. Open `index.html` for the full visual dashboard._

---
_Statuses are refreshed straight from the GitHub API, so this page reflects the live state of every pull request._
