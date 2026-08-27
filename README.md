# Open-source contributions

_Vineeth Sai · [@vineethsaivs](https://github.com/vineethsaivs) · auto-updated after every contribution · last updated August 27, 2026 at 10:37 AM PT_

| PRs | Merged | Open | Merge rate | Projects | Streak |
|:--:|:--:|:--:|:--:|:--:|:--:|
| **208** | **78** | **107** | **77%** | **37** | **23 days** |

_18 in the last 7 days · 87 in the last 30._

## Recent activity

| Date | Project | What | Status |
|---|---|---|---|
| 2026-08-26 | [DeepSpeed #8324](https://github.com/deepspeedai/DeepSpeed/pull/8324) | the flops profiler broadcast elementwise mul/add shapes from index 0 instead of from the trailing dimension, so scaling a [2, 3, 4] activation by a [4] vector was counted over [4, 3, 4] | Open |
| 2026-08-26 | [Ray #65747](https://github.com/ray-project/ray/pull/65747) | PBT converted a perturbed integer hyperparameter back with int(), which truncates toward zero, so * 1.2 was a no-op below 5 while * 0.8 always landed lower and the parameter could only ratchet down to an absorbing 0 | Open |
| 2026-08-26 | [DeepSpeed #8323](https://github.com/deepspeedai/DeepSpeed/pull/8323) | the flops profiler read a transposed convolution's weight as if it were a forward convolution's and sized its output with the forward shape formula, so every grouped transposed conv under-counted its macs by a factor of groups and a depthwise one reported zero | Open |
| 2026-08-25 | [Ray #65731](https://github.com/ray-project/ray/pull/65731) | tune.qrandint and tune.qlograndint never sampled the upper bound they document as inclusive, and raised ValueError when the quantization grid held a single point | Open |
| 2026-08-25 | [litellm #38244](https://github.com/BerriAI/litellm/pull/38244) | shorten_message_to_fit_limit grew the message instead of trimming it whenever the target was small, because content[-0:] is the whole string | Open |
| 2026-08-25 | [DeepSpeed #8317](https://github.com/deepspeedai/DeepSpeed/pull/8317) | the Ulysses all2all built its output shape from the wrong branch for the seq-first (s, b, n, h) layout, silently returning a transposed tensor when the head count divides evenly and raising on the reshape when it does not | Open |
| 2026-08-24 | [DeepSpeed #8313](https://github.com/deepspeedai/DeepSpeed/pull/8313) | three norm-combining sites squared the per-tensor norms and then took the 1/norm_type root, so every p-norm except p=2 returned the wrong global norm and clipped the gradients by the wrong factor; ZeRO-3 also took an L2 norm per tensor whatever norm_type said | Open |
| 2026-08-23 | [DeepSpeed #8305](https://github.com/deepspeedai/DeepSpeed/pull/8305) | ZeRO-3's partition() hardcoded free_data=True at two hops, so free_data=False never reached the guard and the leaf-module fast-sharding path was a no-op | Open |
| 2026-08-23 | [DeepSpeed #8304](https://github.com/deepspeedai/DeepSpeed/pull/8304) | the SLURM launcher forwarded DeepSpeed's own --include to srun, which has no such flag, and sized the job from the unfiltered hostfile, so both resource filters were broken | Open |
| 2026-08-23 | [unsloth #9590](https://github.com/unslothai/unsloth/pull/9590) | main's Repo tests (CPU) went red because a contract test matched raw source for a set literal that a new entry wrapped across lines, while the rule it guards stayed intact | Closed, fix validated |
| 2026-08-23 | [pytorch #194537](https://github.com/pytorch/pytorch/pull/194537) | the conv and avg_pool nn.functional docs carried no parameter types at all, so their pages showed bare names where every other page shows name (type) | Open |
| 2026-08-23 | [pytorch #194535](https://github.com/pytorch/pytorch/pull/194535) | gather and scatter accept a 0-D tensor opposite a 1-D one, but the docs and the shape-check messages claim the dimensions must match | Open |
| 2026-08-22 | [pytorch-lightning #21916](https://github.com/Lightning-AI/pytorch-lightning/pull/21916) | scale_batch_size ran zero batches per trial when the search started after training had begun, so every trial succeeded and it returned a batch size the model cannot run | Open |
| 2026-08-22 | [litellm #37943](https://github.com/BerriAI/litellm/pull/37943) | stream_chunk_builder raised on a raw SSE frame in a collected stream, and six of the nine guardrails that reassemble one call it with no guard, turning an already-delivered completion into a 500 | Open |
| 2026-08-22 | [litellm #37942](https://github.com/BerriAI/litellm/pull/37942) | the Bedrock guardrail used request_data['api_key'] as its own AWS bearer token, so a BYOK credential override sent the caller's NVIDIA or OpenRouter key to AWS and the guardrail 403'd | Open |
| 2026-08-21 | [litellm #37861](https://github.com/BerriAI/litellm/pull/37861) | MCP OAuth discovery ran the resource GET buffered, so a Streamable HTTP server answering GET with an open SSE stream stalled proxy startup; MCP_METADATA_TIMEOUT is httpx's per-read timeout and a keepalive resets it forever | Open |
| 2026-08-21 | [vllm #53302](https://github.com/vllm-project/vllm/pull/53302) | --reasoning-parser qwen3 read only enable_thinking, so a chat template that closed the think block for any other reason left the engine in REASONING and returned the whole answer as reasoning with content null | Open |
| 2026-08-21 | [litellm #37859](https://github.com/BerriAI/litellm/pull/37859) | a Responses API tool-only stream emitted output_text.done, content_part.done and output_item.done for a message item it never opened, so clients that track output items by id (the Vercel AI SDK) aborted the run before the tool result arrived | Open |

_Showing the 18 most recent. Open `index.html` for the full visual dashboard._

---
_Statuses are refreshed straight from the GitHub API, so this page reflects the live state of every pull request._
