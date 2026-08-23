# Open-source contributions

_Vineeth Sai · [@vineethsaivs](https://github.com/vineethsaivs) · auto-updated after every contribution · last updated August 23, 2026 at 1:03 PM PT_

| PRs | Merged | Open | Merge rate | Projects | Streak |
|:--:|:--:|:--:|:--:|:--:|:--:|
| **199** | **74** | **104** | **78%** | **37** | **20 days** |

_26 in the last 7 days · 88 in the last 30._

## Recent activity

| Date | Project | What | Status |
|---|---|---|---|
| 2026-08-23 | [unsloth #9590](https://github.com/unslothai/unsloth/pull/9590) | main's Repo tests (CPU) went red because a contract test matched raw source for a set literal that a new entry wrapped across lines, while the rule it guards stayed intact | Open |
| 2026-08-23 | [pytorch #194537](https://github.com/pytorch/pytorch/pull/194537) | the conv and avg_pool nn.functional docs carried no parameter types at all, so their pages showed bare names where every other page shows name (type) | Open |
| 2026-08-23 | [pytorch #194535](https://github.com/pytorch/pytorch/pull/194535) | gather and scatter accept a 0-D tensor opposite a 1-D one, but the docs and the shape-check messages claim the dimensions must match | Open |
| 2026-08-22 | [pytorch-lightning #21916](https://github.com/Lightning-AI/pytorch-lightning/pull/21916) | scale_batch_size ran zero batches per trial when the search started after training had begun, so every trial succeeded and it returned a batch size the model cannot run | Open |
| 2026-08-22 | [litellm #37943](https://github.com/BerriAI/litellm/pull/37943) | stream_chunk_builder raised on a raw SSE frame in a collected stream, and six of the nine guardrails that reassemble one call it with no guard, turning an already-delivered completion into a 500 | Open |
| 2026-08-22 | [litellm #37942](https://github.com/BerriAI/litellm/pull/37942) | the Bedrock guardrail used request_data['api_key'] as its own AWS bearer token, so a BYOK credential override sent the caller's NVIDIA or OpenRouter key to AWS and the guardrail 403'd | Open |
| 2026-08-21 | [litellm #37861](https://github.com/BerriAI/litellm/pull/37861) | MCP OAuth discovery ran the resource GET buffered, so a Streamable HTTP server answering GET with an open SSE stream stalled proxy startup; MCP_METADATA_TIMEOUT is httpx's per-read timeout and a keepalive resets it forever | Open |
| 2026-08-21 | [vllm #53302](https://github.com/vllm-project/vllm/pull/53302) | --reasoning-parser qwen3 read only enable_thinking, so a chat template that closed the think block for any other reason left the engine in REASONING and returned the whole answer as reasoning with content null | Open |
| 2026-08-21 | [litellm #37859](https://github.com/BerriAI/litellm/pull/37859) | a Responses API tool-only stream emitted output_text.done, content_part.done and output_item.done for a message item it never opened, so clients that track output items by id (the Vercel AI SDK) aborted the run before the tool result arrived | Open |
| 2026-08-20 | [unsloth #9447](https://github.com/unslothai/unsloth/pull/9447) | torch_amp_custom_fwd/_bwd are in _utils.__all__ but the device chain covered cuda, hip and xpu only, so on the MLX runtime the names were never bound and `from ._utils import *` raised AttributeError, taking unsloth.models, unsloth.save and unsloth.utils.attention_dispatch with it | Open |
| 2026-08-20 | [unsloth #9445](https://github.com/unslothai/unsloth/pull/9445) | chat-adapter.ts grew three server-tuning imports the auto-load harness had no stubs for, so every scenario died as a bare ReferenceError inside the retry loop and main's Repo tests (CPU) went red at 70 failed / 1 passed; fixed by inlining the real dependency-free module rather than hand-mirroring it | Open |
| 2026-08-20 | [litellm #37657](https://github.com/BerriAI/litellm/pull/37657) | with code_interpreter_interception a stream:true request came back as a bare ModelResponseStream, which has no __aiter__, so the caller's `async for` raised TypeError and the chunk-shaped object reached the response cache for a later request to trip over | Open |
| 2026-08-20 | [Ray #65621](https://github.com/ray-project/ray/pull/65621) | flatten_dict(prevent_delimiter=True, flatten_list=True) raised UnboundLocalError, because the list branch re-checked `subkey`, a name only the dict branch binds | Open |
| 2026-08-20 | [litellm #37655](https://github.com/BerriAI/litellm/pull/37655) | stream_chunk_builder dropped delta.reasoning_items on both of its paths, so a streamed reasoning turn lost the provider's encrypted reasoning state and could not be round-tripped through the Responses API bridge or replayed from the response cache | Open |
| 2026-08-19 | [unsloth #9311](https://github.com/unslothai/unsloth/pull/9311) | slot 1 of an __INT_TO_FLOAT_MAPPER entry becomes FLOAT_TO_INT_MAPPER[upstream] and MAP_TO_UNSLOTH_16bit[upstream], and both Apertus rows put swiss-ai/Apertus-{8B,70B}-2509 (the pretrained base) there instead of the -Instruct repo; withdrawn the same day as a duplicate of our own earlier PR #7339, which additionally handles the unpublished 70B 16bit repo this one would have pointed at | Withdrawn |
| 2026-08-19 | [litellm #37489](https://github.com/BerriAI/litellm/pull/37489) | _reset_expired_window parsed reset_at then called .replace(tzinfo=None) and compared it against datetime.utcnow(), so an offset compute_budget_reset_at had itself written was read as a wall clock: an Asia/Shanghai window due at 16:00 UTC stayed enforced until 00:00 UTC and an America/New_York window due at 05:00 UTC was reset at 00:00 UTC | Open |
| 2026-08-19 | [litellm #37487](https://github.com/BerriAI/litellm/pull/37487) | langfuse_proxy_route ran base64.b64decode(...).split(':')[1] on the Authorization header before calling user_api_key_auth, so a missing header, non-base64, non-utf8 bytes or a value with no colon raised out of an unauthenticated request and became HTTP 500 with a traceback, on a route registered for GET, POST, PUT, PATCH and DELETE | Open |
| 2026-08-19 | [litellm #37484](https://github.com/BerriAI/litellm/pull/37484) | transform_responses_api_request and transform_compact_response_api_request call remove_cache_control_flag_from_input_and_tools unconditionally, while the chat path has _should_preserve_cache_control_for_endpoint carving out the generic openai provider on a non-openai.com api_base, so a cache_control-aware gateway kept its breakpoints on /chat/completions and lost them on /responses | Open |

_Showing the 18 most recent. Open `index.html` for the full visual dashboard._

---
_Statuses are refreshed straight from the GitHub API, so this page reflects the live state of every pull request._
