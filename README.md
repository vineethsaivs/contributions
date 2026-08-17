# Open-source contributions

_Vineeth Sai · [@vineethsaivs](https://github.com/vineethsaivs) · auto-updated after every contribution · last updated August 16, 2026 at 9:53 PM PT_

| PRs | Merged | Open | Merge rate | Projects | Streak |
|:--:|:--:|:--:|:--:|:--:|:--:|
| **173** | **68** | **87** | **79%** | **37** | **13 days** |

_23 in the last 7 days · 77 in the last 30._

## Recent activity

| Date | Project | What | Status |
|---|---|---|---|
| 2026-08-16 | [langchain #39689](https://github.com/langchain-ai/langchain/pull/39689) | FileCallbackHandler.on_tool_end documents color as an override falling back to self.color but wrote the tool output with no color at all, so agent logs had every line coloured except the tool output; the three sibling writes in the same class and StdOutCallbackHandler both do it correctly | Open |
| 2026-08-16 | [pytorch #193728](https://github.com/pytorch/pytorch/pull/193728) | scaled_dot_product_attention never checked that key and value share a sequence length; the CPU flash kernel takes its key count from the value and walks the key pointer that far, so a longer value reads past the end of the key allocation and a large overrun dies with SIGBUS, while MATH and meta both reject the same input | Open |
| 2026-08-16 | [ollama #17809](https://github.com/ollama/ollama/pull/17809) | the Modelfile parser's buffer guard tested strconv.IsPrint, which is false for format runes and non-ASCII spaces, so ollama create silently rewrote any SYSTEM/TEMPLATE value containing them: Persian می‌خواهم lost its ZWNJ and became a different word, and 👨‍👩‍👧 became three separate emoji | Open |
| 2026-08-15 | [textgen #7642](https://github.com/oobabooga/textgen/pull/7642) | the ExLlamaV3 loader calls list() on the sampler priority, which is a newline-separated string in every default path, so it became one entry per character and both the sampler order and temperature_last were silently ignored | Open |
| 2026-08-15 | [unsloth #8938](https://github.com/unslothai/unsloth/pull/8938) | custom_prompt_template is accepted, documented and forwarded through two public functions, but nothing ever read it: the Alpaca branch always rendered the hardcoded default, silently discarding the caller's prompt format | Open |
| 2026-08-15 | [vllm #52465](https://github.com/vllm-project/vllm/pull/52465) | the Muse Glimmer reasoning parser drops every completed reasoning block when generation is truncated inside a later one, and its streaming path glues consecutive blocks together with no separator, so the two paths return different reasoning for the same generation | Open |
| 2026-08-14 | [litellm #36952](https://github.com/BerriAI/litellm/pull/36952) | infer_content_type_from_url_and_content splits on '.' before stripping the query, so any dot in a query string breaks MIME detection and presigned S3 document URLs raise ValueError | Open |
| 2026-08-14 | [vllm #52370](https://github.com/vllm-project/vllm/pull/52370) | every optional Literal flag advertises None among its choices but rejects it, because the string is registered while optional_type converts the input to the object None; 16 flags affected | Open |
| 2026-08-14 | [unsloth #8837](https://github.com/unslothai/unsloth/pull/8837) | 2098b7cd4 made parallelSlotsClamped a required field of LlamaFlagCatalog but left four hand-built test fixtures without it, so npm run typecheck fails and Frontend CI has been red on main | Merged |
| 2026-08-13 | [ollama #17734](https://github.com/ollama/ollama/pull/17734) | ParseFile counts both \r and \n, so a CRLF Modelfile counts two lines per line and every parse error reports a line number roughly double the real one | Open |
| 2026-08-13 | [textgen #7641](https://github.com/oobabooga/textgen/pull/7641) | create_ui() binds stride_length twice, so all_params picks up the Perplexity tab's Stride slider and text-dataset LoRA training aborts on stock defaults with 'stride length must be smaller than cutoff length' | Open |
| 2026-08-13 | [unsloth #8726](https://github.com/unslothai/unsloth/pull/8726) | nine model ids a model_defaults file names in its Also applies to header could not resolve to it, so they fell back to default.yaml; Qwen/Qwen3-30B-A3B-Instruct-2507 got lora_r 16 instead of its tuned 32 | Open |
| 2026-08-13 | [unsloth #8724](https://github.com/unslothai/unsloth/pull/8724) | both training-chart formatters drop to zero decimals at 1000 and then strip trailing zeroes with an optional-dot regex, so 25000 rendered as 25 and 1000000 as 1 in tooltips and on the axis | Open |
| 2026-08-13 | [unsloth #8723](https://github.com/unslothai/unsloth/pull/8723) | 10 shipped model_defaults express warmup as warmup_ratio and set no warmup_steps, but the training form read only warmup_steps and its type never declared the ratio, so every one of them silently kept the generic 5 | Open |
| 2026-08-12 | [unsloth #8595](https://github.com/unslothai/unsloth/pull/8595) | getExternalMaxOutputTokens gated every cap row on providerType, so a custom OpenAI-compatible connection fell back to the generic 32K even for a model id whose family has a documented cap | Open |
| 2026-08-12 | [unsloth #8593](https://github.com/unslothai/unsloth/pull/8593) | FAMILY_TRAIN_DEFAULTS advertised lr_warmup_steps for six diffusion families while the default constant scheduler never reads num_warmup_steps, so the documented LR ramp never happened | Open |

_Showing the 16 most recent. Open `index.html` for the full visual dashboard._

---
_Statuses are refreshed straight from the GitHub API, so this page reflects the live state of every pull request._
