# Open-source contributions

_Vineeth Sai · [@vineethsaivs](https://github.com/vineethsaivs) · auto-updated after every contribution · last updated October 29, 2026 at 6:54 PM PT_

| PRs | Merged | Open | Merge rate | Projects | Streak |
|:--:|:--:|:--:|:--:|:--:|:--:|
| **483** | **217** | **198** | **76%** | **42** | **140 days** |

_1620 GitHub contributions in the last year · 92 in the last 7 days · 328 in the last 30._

## Bug reports

- [flax #5594](https://github.com/google/flax/issues/5594): nnx.GRUCell is missing the b_hn bias that its docstring and linen.GRUCell both specify.
- [trl #7221](https://github.com/huggingface/trl/issues/7221): Reproduced NaN entropy for valid zero-probability tokens, including finite float16 inputs; PyTorch categorical entropy remains finite.

## Recent activity

| Date | Project | What | Status |
|---|---|---|---|
| 2026-10-29 | [Ray #67558](https://github.com/ray-project/ray/pull/67558) | tune.qrandint(0, 100, 10) in ZOOptSearch suggested values like 8, 16 and 65 and could never reach the inclusive upper bound 100, because convert_search_space dropped q for the Integer branch | Open |
| 2026-10-29 | [DeepSpeed #8947](https://github.com/deepspeedai/DeepSpeed/pull/8947) | generalized_jsd_loss reported a wrong valid_token_count and loss for bf16 and fp16 logits (bf16 rounded 97992 valid tokens to 97792; fp16 with more than 65504 returned int64 max and the loss collapsed to about 0), because it cast response_mask to the logits dtype before summing | Open |
| 2026-10-29 | [unsloth-zoo #2254](https://github.com/unslothai/unsloth-zoo/pull/2254) | The compiled LED encoder returned different hidden states from stock LED (max diff 0.025), because convert_attention_masks_to_bool rewrote LED's additive encoder mask into a boolean one that LED's non-SDPA Longformer encoder still reads additively | Open |
| 2026-10-28 | [vllm #64337](https://github.com/vllm-project/vllm/pull/64337) | A chat request (input_audio or audio_url) carrying a WAV cut to 30 bytes returned HTTP 500 instead of 400, because load_audio re-raised libsndfile's RuntimeError for any error code outside the format-detection ones | Open |
| 2026-10-28 | [unsloth-zoo #2214](https://github.com/unslothai/unsloth-zoo/pull/2214) | On transformers 4.52 to 4.57 the compiler silently dropped the causal mask for models that do not use SDPA (T5, mT5, UMT5, GPT-J, CodeGen, GPT-NeoX-Japanese, Bloom), so every position saw future tokens and training loss and generations were wrong with no error | Open |
| 2026-10-28 | [Ray #67509](https://github.com/ray-project/ray/pull/67509) | NevergradSearch returned nan for every tune.randn and tune.qrandn parameter, because the unbounded domain became ng.p.Scalar(lower=-inf, upper=inf), which starts at NaN on nevergrad 1.0.12 | Open |
| 2026-10-28 | [unsloth #15775](https://github.com/unslothai/unsloth/pull/15775) | The legacy unsloth-cli.py documents --dtype None (its own usage line; the help says None for auto detection), but on every non-MLX backend it crashed with an AssertionError, because the CLI passed the string "None" to FastLanguageModel.from_pretrained, which asserts dtype is None or a torch dtype | Open |
| 2026-10-27 | [unsloth-zoo #2154](https://github.com/unslothai/unsloth-zoo/pull/2154) | On TRL 0.18.2 (the declared floor), prompt/completion SFT through Unsloth trained on the prompt tokens too, because completion_mask became a labels column that TRL 0.18's collator never reads | Merged |
| 2026-10-27 | [vllm #64102](https://github.com/vllm-project/vllm/pull/64102) | A vllm run-batch input line with a missing, null or non-string url crashed validate_batch with a raw KeyError: 'url' instead of reporting the bad field | Open |
| 2026-10-27 | [unsloth-zoo #2152](https://github.com/unslothai/unsloth-zoo/pull/2152) | On transformers 4.52 to 4.57, an old-layout bnb skip entry never matched model.language_model.layers.N for Qwen2-VL and Qwen2.5-VL, so a layer meant to stay in bf16 became Linear4bit | Merged |
| 2026-10-27 | [Ray #67482](https://github.com/ray-project/ray/pull/67482) | tune.sample_from values never reached trial.evaluated_params, so TensorBoard hparams, the CLI table and Aim left them out; with every varied param on sample_from, TensorBoard logged no hparams at all | Open |
| 2026-10-26 | [litellm #48440](https://github.com/BerriAI/litellm/pull/48440) | create_eval dropped the caller's metadata and create_run had the assignment commented out, so metadata was accepted and silently dropped; re-filed against main from #34735 | Open |
| 2026-10-26 | [litellm #48439](https://github.com/BerriAI/litellm/pull/48439) | CloudflareChatConfig sent OpenAI content-part arrays unflattened, so Cloudflare Workers AI rejected them with a type mismatch (array not in string); still true on main, re-filed against main from #33991 | Open |
| 2026-10-26 | [vllm #63814](https://github.com/vllm-project/vllm/pull/63814) | --fingerprint-mode custom without --fingerprint-value started the server and silently dropped system_fingerprint from every response, the same as mode none | Open |
| 2026-10-26 | [DeepSpeed #8916](https://github.com/deepspeedai/DeepSpeed/pull/8916) | With checkpoint.writer set and data_parallel unset (the default), plain data parallel on ZeRO 0, 1 and 2 with no mpu or MoE crashed at engine init with AttributeError: 'UniversalParallelInfo' object has no attribute 'dp_rank' | Open |
| 2026-10-26 | [unsloth #15389](https://github.com/unslothai/unsloth/pull/15389) | Studio answered 500 instead of 422 for a request integer past signed 64-bit (createdAt/updatedAt on the chat history routes and /api/prompts, offset on /api/chat/attachments, since on /api/scheduled-tasks/runs) | Merged |
| 2026-10-26 | [unsloth-zoo #2117](https://github.com/unslothai/unsloth-zoo/pull/2117) | The patched PEFT LoRA forward applied only the first adapter under set_adapter(["a", "b"]), so the second adapter had no effect and received no gradient | Merged |
| 2026-10-26 | [Ray #67425](https://github.com/ray-project/ray/pull/67425) | Tuner.fit() crashed in resolve_placeholders with a TypeError when a search space mixed a non-primitive option with a primitive one, e.g. tune.grid_search([Act("relu"), 5]) | Open |

_Showing the 18 most recent. Open `index.html` for the full visual dashboard._

---
_Statuses are refreshed straight from the GitHub API, so this page reflects the live state of every pull request._
