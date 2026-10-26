# Open-source contributions

_Vineeth Sai · [@vineethsaivs](https://github.com/vineethsaivs) · auto-updated after every contribution · last updated October 26, 2026 at 4:06 PM PT_

| PRs | Merged | Open | Merge rate | Projects | Streak |
|:--:|:--:|:--:|:--:|:--:|:--:|
| **472** | **210** | **196** | **76%** | **42** | **137 days** |

_1573 GitHub contributions in the last year · 76 in the last 7 days · 330 in the last 30._

## Bug reports

- [flax #5594](https://github.com/google/flax/issues/5594): nnx.GRUCell is missing the b_hn bias that its docstring and linen.GRUCell both specify.
- [trl #7221](https://github.com/huggingface/trl/issues/7221): Reproduced NaN entropy for valid zero-probability tokens, including finite float16 inputs; PyTorch categorical entropy remains finite.

## Recent activity

| Date | Project | What | Status |
|---|---|---|---|
| 2026-10-26 | [litellm #48440](https://github.com/BerriAI/litellm/pull/48440) | create_eval dropped the caller's metadata and create_run had the assignment commented out, so metadata was accepted and silently dropped; re-filed against main from #34735 | Open |
| 2026-10-26 | [litellm #48439](https://github.com/BerriAI/litellm/pull/48439) | CloudflareChatConfig sent OpenAI content-part arrays unflattened, so Cloudflare Workers AI rejected them with a type mismatch (array not in string); still true on main, re-filed against main from #33991 | Open |
| 2026-10-26 | [vllm #63814](https://github.com/vllm-project/vllm/pull/63814) | --fingerprint-mode custom without --fingerprint-value started the server and silently dropped system_fingerprint from every response, the same as mode none | Open |
| 2026-10-26 | [DeepSpeed #8916](https://github.com/deepspeedai/DeepSpeed/pull/8916) | With checkpoint.writer set and data_parallel unset (the default), plain data parallel on ZeRO 0, 1 and 2 with no mpu or MoE crashed at engine init with AttributeError: 'UniversalParallelInfo' object has no attribute 'dp_rank' | Open |
| 2026-10-26 | [unsloth #15389](https://github.com/unslothai/unsloth/pull/15389) | Studio answered 500 instead of 422 for a request integer past signed 64-bit (createdAt/updatedAt on the chat history routes and /api/prompts, offset on /api/chat/attachments, since on /api/scheduled-tasks/runs) | Open |
| 2026-10-26 | [unsloth-zoo #2117](https://github.com/unslothai/unsloth-zoo/pull/2117) | The patched PEFT LoRA forward applied only the first adapter under set_adapter(["a", "b"]), so the second adapter had no effect and received no gradient | Open |
| 2026-10-26 | [Ray #67425](https://github.com/ray-project/ray/pull/67425) | Tuner.fit() crashed in resolve_placeholders with a TypeError when a search space mixed a non-primitive option with a primitive one, e.g. tune.grid_search([Act("relu"), 5]) | Open |
| 2026-10-25 | [unsloth #15282](https://github.com/unslothai/unsloth/pull/15282) | Studio /v1/messages with a Connection model answered 500 instead of 400 for an out-of-range sampling value | Merged |
| 2026-10-25 | [Ray #67408](https://github.com/ray-project/ray/pull/67408) | HyperOptSearch returned values off the grid for tune.qrandint and tune.qlograndint (0 for qrandint(1, 10, 3), 10 for qrandint(0, 9, 5)) | Open |
| 2026-10-25 | [unsloth-zoo #2086](https://github.com/unslothai/unsloth-zoo/pull/2086) | higher_precision_softmax rewrote a softmax with a compound first argument into a TypeError (Falcon) or a SyntaxError (SLANet, SLANeXt) in the generated module | Merged |
| 2026-10-24 | [Ray #67378](https://github.com/ray-project/ray/pull/67378) | CLIReporter and JupyterNotebookReporter with sort_by_metric=True crashed with a TypeError when a terminated trial never reported the metric | Open |
| 2026-10-24 | [unsloth #15176](https://github.com/unslothai/unsloth/pull/15176) | Studio training requests accepted a random_seed outside the numpy range, which only failed in set_seed after the model had loaded | Merged |
| 2026-10-24 | [vllm #63521](https://github.com/vllm-project/vllm/pull/63521) | An unsupported endpoint-load-metrics-format header logged the Python builtin "format" instead of the format name | Open |
| 2026-10-23 | [DeepSpeed #8896](https://github.com/deepspeedai/DeepSpeed/pull/8896) | Draft: With comms profiling on, the first all_gather_object or monitored_barrier printed "wrong comm_op specified" and exited the process with status 0 | Open |
| 2026-10-23 | [unsloth #14999](https://github.com/unslothai/unsloth/pull/14999) | Studio dropped a column mapped to the system role when the advisor mapping also carried metadata | Merged |
| 2026-10-23 | [Ray #67335](https://github.com/ray-project/ray/pull/67335) | Reusing a RunConfig with callbacks for a second Tuner.fit() errored the trials, because the default callbacks were appended to the caller's list | Open |

_Showing the 16 most recent. Open `index.html` for the full visual dashboard._

---
_Statuses are refreshed straight from the GitHub API, so this page reflects the live state of every pull request._
