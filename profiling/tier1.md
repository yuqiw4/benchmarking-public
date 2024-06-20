
## 2to3

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 27.91% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 3.51% | `python` | `gc_collect_region.isra.0` | gc |
| 2.98% | `python` | `_PyObject_Malloc` | memory |
| 2.91% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 2.16% | `python` | `_PyObject_Free` | memory |
| 1.85% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.79% | `python` | `_Py_dict_lookup` | lookup |
| 1.46% | `python` | `visit_decref` | gc |
| 1.44% | `python` | `sre_ucs1_match` | library |
| 1.31% | `python` | `tupledealloc` | memory |
| 1.29% | `python` | `_PyType_Lookup` | lookup |
| 1.29% | `python` | `_PyFrame_ClearExceptCode` | interpreter |
| 0.90% | `python` | `PyObject_GenericGetAttr` | dynamic |
| 0.88% | `python` | `visit_reachable` | gc |
| 0.80% | `python` | `_PyPegen_is_memoized` | interpreter |
| 0.73% | `python` | `r_object` | import |
| 0.72% | `python` | `initialize_locals` | interpreter |
| 0.68% | `libc-2.31.so` | `pthread_attr_setschedparam` | libc |
| 0.63% | `python` | `PyObject_GC_UnTrack` | gc |
| 0.59% | `python` | `tuple_alloc` | memory |
| 0.57% | `python` | `_PyTuple_FromArraySteal` | tuple |
| 0.56% | `python` | `PyObject_RichCompareBool` | dynamic |
| 0.53% | `python` | `siphash13` | str |
| 0.53% | `python` | `update_one_slot` | lookup |
| 0.53% | `python` | `dict_dealloc` | memory |

## aiohttp

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 26.28% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 2.99% | `python` | `_PyObject_Malloc` | memory |
| 2.58% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 2.32% | `python` | `_PyObject_Free` | memory |
| 2.25% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 2.07% | `python` | `_PyFrame_ClearExceptCode` | interpreter |
| 1.91% | `python` | `gc_collect_region.isra.0` | gc |
| 1.44% | `python` | `_Py_dict_lookup` | lookup |
| 1.30% | `python` | `initialize_locals` | interpreter |
| 1.29% | `python` | `tupledealloc` | memory |
| 0.99% | `python` | `visit_decref` | gc |
| 0.98% | `python` | `_PyType_Lookup` | lookup |
| 0.67% | `python` | `visit_reachable` | gc |
| 0.64% | `libc-2.31.so` | `pthread_attr_setschedparam` | libc |
| 0.60% | `python` | `dict_dealloc` | memory |
| 0.59% | `python` | `sre_ucs1_match` | library |
| 0.59% | `python` | `PyDict_GetItemRef` | dict |
| 0.51% | `python` | `insertdict` | dict |
| 0.51% | `python` | `PyObject_GenericGetAttr` | dynamic |

## async_generators

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 23.33% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 8.11% | `python` | `_PyErr_SetObject.part.0` | exceptions |
| 4.17% | `python` | `_PyObject_Malloc` | memory |
| 3.79% | `python` | `_PyObject_Free` | memory |
| 2.62% | `python` | `async_gen_asend_iternext` | unknown |
| 2.60% | `python` | `PyType_GenericAlloc` | memory |
| 2.00% | `python` | `StopIteration_init` | dynamic |
| 1.82% | `python` | `tupledealloc` | memory |
| 1.81% | `python` | `_Py_NewReference` | memory |
| 1.80% | `python` | `async_gen_wrapped_val_dealloc` | memory |
| 1.62% | `python` | `PyErr_ExceptionMatches` | exceptions |
| 1.59% | `python` | `StopIteration_dealloc` | memory |
| 1.48% | `python` | `async_gen_asend_dealloc` | memory |
| 1.46% | `python` | `_PyErr_ExceptionMatches` | exceptions |
| 1.46% | `python` | `_PyAsyncGenValueWrapperNew` | memory |
| 1.44% | `python` | `async_gen_anext` | unknown |
| 1.40% | `python` | `tuple_alloc` | memory |
| 1.38% | `python` | `_PyObject_MakeTpCall` | dynamic |
| 1.31% | `python` | `_PyTuple_FromArray.part.0` | tuple |
| 1.28% | `python` | `PyObject_GC_UnTrack` | gc |
| 1.22% | `python` | `_PyGen_FetchStopIterationValue` | unknown |
| 1.14% | `python` | `type_call` | dynamic |
| 1.11% | `python` | `_PyErr_Restore` | exceptions |
| 1.07% | `python` | `PyObject_CallOneArg` | dynamic |
| 1.03% | `python` | `gc_collect_region.isra.0` | gc |
| 1.01% | `python` | `PyObject_GC_Del` | gc |
| 0.85% | `python` | `_PyGen_SetStopIterationValue` | unknown |
| 0.83% | `python` | `PyObject_CallFinalizerFromDealloc` | memory |
| 0.75% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 0.70% | `python` | `PyType_IsSubtype` | dynamic |
| 0.68% | `python` | `_Py_Dealloc` | memory |
| 0.67% | `python` | `_PyFrame_ClearExceptCode` | interpreter |
| 0.62% | `python` | `_PyErr_CreateException` | exceptions |
| 0.62% | `python` | `initialize_locals` | interpreter |
| 0.60% | `python` | `BaseException_new` | memory |
| 0.55% | `python` | `_PyObject_GC_Link` | gc |
| 0.53% | `python` | `long_add` | int |
| 0.52% | `python` | `visit_decref` | gc |
| 0.51% | `python` | `PyObject_RichCompareBool` | dynamic |

## async_tree

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 24.43% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 8.27% | `python` | `gc_collect_region.isra.0` | gc |
| 4.11% | `python` | `visit_reachable` | gc |
| 3.97% | `python` | `visit_decref` | gc |
| 3.77% | `python` | `visit_add_to_container` | gc |
| 3.74% | `python` | `_PyObject_Malloc` | memory |
| 2.15% | `python` | `_PyObject_Free` | memory |
| 1.65% | `python` | `_Py_dict_lookup` | lookup |
| 1.55% | `python` | `initialize_locals` | interpreter |
| 1.46% | `python` | `PyObject_GC_UnTrack` | gc |
| 1.44% | `python` | `_PyFrame_ClearExceptCode` | interpreter |
| 1.27% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 1.09% | `python` | `_PyType_Lookup` | lookup |
| 0.99% | `python` | `subtype_traverse` | gc |
| 0.85% | `python` | `tupledealloc` | memory |
| 0.84% | `python` | `_PyObject_GetMethod` | dynamic |
| 0.81% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 0.78% | `python` | `_PyGC_Collect` | gc |
| 0.77% | `python` | `context_tp_dealloc` | memory |
| 0.71% | `python` | `_PyEvalFramePushAndInit` | interpreter |
| 0.61% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 0.57% | `python` | `_PyEval_Vector` | interpreter |
| 0.56% | `python` | `subtype_dealloc` | memory |
| 0.55% | `python` | `insertdict` | dict |
| 0.55% | `python` | `dict_traverse` | gc |
| 0.50% | `python` | `PyObject_GenericGetAttr` | dynamic |

## async_tree_cpu_io_mixed

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 17.90% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 17.73% | `python` | `k_mul` | int |
| 6.28% | `python` | `gc_collect_region.isra.0` | gc |
| 4.31% | `python` | `_PyObject_Malloc` | memory |
| 3.23% | `python` | `_PyObject_Free` | memory |
| 3.07% | `python` | `visit_reachable` | gc |
| 3.06% | `python` | `visit_decref` | gc |
| 2.72% | `python` | `visit_add_to_container` | gc |
| 1.49% | `python` | `PyErr_CheckSignals` | exceptions |
| 1.26% | `python` | `PyObject_GC_UnTrack` | gc |
| 1.06% | `python` | `_Py_dict_lookup` | lookup |
| 1.05% | `math.cpython-313-x86_64-linux-gnu.so` | `factorial_partial_product` | library |
| 1.01% | `python` | `_PyFrame_ClearExceptCode` | interpreter |
| 1.00% | `python` | `initialize_locals` | interpreter |
| 0.87% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 0.80% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 0.79% | `python` | `subtype_traverse` | gc |
| 0.77% | `python` | `_PyType_Lookup` | lookup |
| 0.70% | `python` | `PyThread_get_thread_ident` | unknown |
| 0.66% | `python` | `PyLong_FromUnsignedLong` | int |
| 0.64% | `python` | `_PyObject_GetMethod` | dynamic |
| 0.64% | `python` | `context_tp_dealloc` | memory |
| 0.61% | `python` | `_PyGC_Collect` | gc |
| 0.56% | `python` | `tupledealloc` | memory |
| 0.51% | `python` | `long_mul` | int |

## async_tree_cpu_io_mixed_tg

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 18.01% | `python` | `k_mul` | int |
| 16.93% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 6.89% | `python` | `gc_collect_region.isra.0` | gc |
| 4.41% | `python` | `_PyObject_Malloc` | memory |
| 3.95% | `python` | `visit_add_to_container` | gc |
| 3.74% | `python` | `visit_decref` | gc |
| 3.55% | `python` | `visit_reachable` | gc |
| 3.37% | `python` | `_PyObject_Free` | memory |
| 1.49% | `python` | `PyErr_CheckSignals` | exceptions |
| 1.06% | `math.cpython-313-x86_64-linux-gnu.so` | `factorial_partial_product` | library |
| 0.99% | `python` | `initialize_locals` | interpreter |
| 0.94% | `python` | `_PyFrame_ClearExceptCode` | interpreter |
| 0.93% | `python` | `PyObject_GC_UnTrack` | gc |
| 0.83% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 0.79% | `python` | `subtype_traverse` | gc |
| 0.73% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 0.72% | `python` | `PyThread_get_thread_ident` | unknown |
| 0.72% | `python` | `_Py_dict_lookup` | lookup |
| 0.70% | `python` | `_PyGC_Collect` | gc |
| 0.64% | `python` | `PyLong_FromUnsignedLong` | int |
| 0.61% | `python` | `_PyType_Lookup` | lookup |
| 0.54% | `python` | `set_traverse` | gc |
| 0.53% | `python` | `long_mul` | int |
| 0.51% | `python` | `_PyEval_Vector` | interpreter |
| 0.50% | `python` | `tupledealloc` | memory |
| 0.50% | `python` | `_PyObject_GetMethod` | dynamic |

## async_tree_io

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 21.47% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 13.76% | `python` | `gc_collect_region.isra.0` | gc |
| 6.90% | `python` | `visit_add_to_container` | gc |
| 6.42% | `python` | `visit_decref` | gc |
| 6.36% | `python` | `visit_reachable` | gc |
| 2.58% | `python` | `_PyObject_Malloc` | memory |
| 1.62% | `python` | `_PyObject_Free` | memory |
| 1.43% | `python` | `initialize_locals` | interpreter |
| 1.42% | `python` | `_PyGC_Collect` | gc |
| 1.26% | `python` | `subtype_traverse` | gc |
| 1.25% | `python` | `_PyFrame_ClearExceptCode` | interpreter |
| 1.12% | `python` | `PyObject_GC_UnTrack` | gc |
| 0.90% | `python` | `_Py_dict_lookup` | lookup |
| 0.87% | `python` | `_PyType_Lookup` | lookup |
| 0.79% | `python` | `_PyEvalFramePushAndInit` | interpreter |
| 0.78% | `python` | `_PyFrame_Traverse` | interpreter |
| 0.71% | `python` | `_PyEval_Vector` | interpreter |
| 0.65% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 0.63% | `python` | `tupledealloc` | memory |
| 0.62% | `python` | `gen_traverse` | gc |
| 0.58% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 0.55% | `python` | `PyObject_RichCompareBool` | dynamic |
| 0.54% | `python` | `dict_traverse` | gc |
| 0.54% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 0.51% | `_asyncio.cpython-313-x86_64-linux-gnu.so` | `TaskObj_traverse` | library |

## async_tree_io_tg

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 20.76% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 13.86% | `python` | `gc_collect_region.isra.0` | gc |
| 7.70% | `python` | `visit_add_to_container` | gc |
| 6.89% | `python` | `visit_decref` | gc |
| 6.83% | `python` | `visit_reachable` | gc |
| 2.47% | `python` | `_PyObject_Malloc` | memory |
| 1.58% | `python` | `_PyObject_Free` | memory |
| 1.57% | `python` | `_PyGC_Collect` | gc |
| 1.40% | `python` | `initialize_locals` | interpreter |
| 1.26% | `python` | `subtype_traverse` | gc |
| 1.18% | `python` | `_PyFrame_ClearExceptCode` | interpreter |
| 1.08% | `python` | `_PyFrame_Traverse` | interpreter |
| 1.04% | `python` | `PyObject_GC_UnTrack` | gc |
| 0.97% | `python` | `_PyEval_Vector` | interpreter |
| 0.86% | `python` | `gen_traverse` | gc |
| 0.78% | `python` | `_PyEvalFramePushAndInit` | interpreter |
| 0.74% | `python` | `_PyType_Lookup` | lookup |
| 0.69% | `python` | `set_traverse` | gc |
| 0.67% | `python` | `_Py_dict_lookup` | lookup |
| 0.65% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 0.57% | `python` | `tupledealloc` | memory |
| 0.53% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 0.53% | `_asyncio.cpython-313-x86_64-linux-gnu.so` | `TaskObj_traverse` | library |
| 0.52% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 0.52% | `python` | `gen_dealloc` | memory |
| 0.51% | `python` | `PyObject_RichCompareBool` | dynamic |

## async_tree_memoization

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 25.03% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 9.21% | `python` | `gc_collect_region.isra.0` | gc |
| 4.55% | `python` | `visit_decref` | gc |
| 4.42% | `python` | `visit_reachable` | gc |
| 3.97% | `python` | `visit_add_to_container` | gc |
| 3.42% | `python` | `_PyObject_Malloc` | memory |
| 1.97% | `python` | `_PyObject_Free` | memory |
| 1.81% | `python` | `PyObject_GC_UnTrack` | gc |
| 1.53% | `python` | `_Py_dict_lookup` | lookup |
| 1.39% | `python` | `_PyFrame_ClearExceptCode` | interpreter |
| 1.37% | `python` | `initialize_locals` | interpreter |
| 1.15% | `python` | `subtype_traverse` | gc |
| 1.11% | `python` | `_PyType_Lookup` | lookup |
| 1.11% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 0.90% | `python` | `context_tp_dealloc` | memory |
| 0.90% | `python` | `_PyGC_Collect` | gc |
| 0.87% | `python` | `_PyObject_GetMethod` | dynamic |
| 0.74% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 0.73% | `python` | `_PyEval_Vector` | interpreter |
| 0.71% | `python` | `tupledealloc` | memory |
| 0.65% | `python` | `_PyEvalFramePushAndInit` | interpreter |
| 0.63% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 0.61% | `python` | `PyObject_GenericGetAttr` | dynamic |
| 0.56% | `python` | `set_lookkey` | miscobj |
| 0.52% | `python` | `insertdict` | dict |
| 0.52% | `python` | `dict_traverse` | gc |
| 0.50% | `python` | `PyDict_GetItemRef` | dict |
| 0.50% | `python` | `subtype_dealloc` | memory |

## async_tree_memoization_tg

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 24.19% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 9.87% | `python` | `gc_collect_region.isra.0` | gc |
| 5.57% | `python` | `visit_add_to_container` | gc |
| 5.29% | `python` | `visit_decref` | gc |
| 5.04% | `python` | `visit_reachable` | gc |
| 3.22% | `python` | `_PyObject_Malloc` | memory |
| 1.97% | `python` | `_PyObject_Free` | memory |
| 1.38% | `python` | `initialize_locals` | interpreter |
| 1.34% | `python` | `PyObject_GC_UnTrack` | gc |
| 1.29% | `python` | `_PyFrame_ClearExceptCode` | interpreter |
| 1.14% | `python` | `subtype_traverse` | gc |
| 1.11% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 1.03% | `python` | `_Py_dict_lookup` | lookup |
| 1.00% | `python` | `_PyGC_Collect` | gc |
| 0.94% | `python` | `_PyType_Lookup` | lookup |
| 0.75% | `python` | `_PyEval_Vector` | interpreter |
| 0.73% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 0.73% | `python` | `_PyObject_GetMethod` | dynamic |
| 0.71% | `python` | `tupledealloc` | memory |
| 0.70% | `python` | `set_traverse` | gc |
| 0.67% | `python` | `PyObject_GenericGetAttr` | dynamic |
| 0.67% | `python` | `_PyEvalFramePushAndInit` | interpreter |
| 0.62% | `python` | `_PyFrame_Traverse` | interpreter |
| 0.60% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 0.59% | `python` | `set_lookkey` | miscobj |
| 0.51% | `python` | `gen_traverse` | gc |

## async_tree_tg

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 23.45% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 8.88% | `python` | `gc_collect_region.isra.0` | gc |
| 5.38% | `python` | `visit_add_to_container` | gc |
| 4.77% | `python` | `visit_decref` | gc |
| 4.77% | `python` | `visit_reachable` | gc |
| 3.57% | `python` | `_PyObject_Malloc` | memory |
| 2.18% | `python` | `_PyObject_Free` | memory |
| 1.59% | `python` | `initialize_locals` | interpreter |
| 1.32% | `python` | `_PyFrame_ClearExceptCode` | interpreter |
| 1.16% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 1.12% | `python` | `_Py_dict_lookup` | lookup |
| 1.06% | `python` | `PyObject_GC_UnTrack` | gc |
| 0.96% | `python` | `subtype_traverse` | gc |
| 0.90% | `python` | `_PyType_Lookup` | lookup |
| 0.87% | `python` | `_PyGC_Collect` | gc |
| 0.82% | `python` | `tupledealloc` | memory |
| 0.81% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 0.74% | `python` | `_PyEvalFramePushAndInit` | interpreter |
| 0.73% | `python` | `set_traverse` | gc |
| 0.72% | `python` | `_PyObject_GetMethod` | dynamic |
| 0.65% | `python` | `_PyEval_Vector` | interpreter |
| 0.64% | `python` | `PyObject_GenericGetAttr` | dynamic |
| 0.64% | `python` | `_PyFrame_Traverse` | interpreter |
| 0.61% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 0.56% | `python` | `subtype_dealloc` | memory |
| 0.50% | `python` | `PyObject_RichCompareBool` | dynamic |

## asyncio_tcp

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 31.79% | `[kernel.kallsyms]` | `copy_user_enhanced_fast_string` | kernel |
| 16.77% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 9.48% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 7.82% | `[kernel.kallsyms]` | `clear_page_erms` | kernel |
| 0.77% | `python` | `_PyObject_Malloc` | memory |
| 0.60% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 0.57% | `[kernel.kallsyms]` | `tcp_sendmsg_locked` | kernel |

## asyncio_tcp_ssl

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 39.27% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 25.74% | `libcrypto.so.1.1` | `CRYPTO_secure_actual_size` | libc |
| 10.63% | `[kernel.kallsyms]` | `copy_user_enhanced_fast_string` | kernel |
| 3.76% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 2.84% | `[kernel.kallsyms]` | `clear_page_erms` | kernel |
| 0.86% | `libssl.so.1.1` | `SSL_rstate_string` | library |
| 0.55% | `libc-2.31.so` | `pthread_attr_setschedparam` | libc |

## asyncio_websockets

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 63.70% | `libz.so.1.2.11` | `crc32_combine64` | library |
| 20.20% | `libz.so.1.2.11` | `inflateBackEnd` | library |
| 2.84% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.87% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 0.51% | `python` | `unicodekeys_lookup_unicode` | lookup |

## chameleon

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 38.66% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 4.37% | `python` | `_PyObject_Malloc` | memory |
| 3.12% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 2.79% | `python` | `_PyObject_Free` | memory |
| 1.88% | `python` | `_PyFrame_ClearExceptCode` | interpreter |
| 1.84% | `python` | `sre_ucs2_charset.isra.0` | library |
| 1.82% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.77% | `python` | `_Py_dict_lookup` | lookup |
| 1.57% | `python` | `gc_collect_region.isra.0` | gc |
| 1.49% | `python` | `_PyUnicode_JoinArray.part.0` | str |
| 1.37% | `python` | `long_to_decimal_string_internal` | int |
| 1.08% | `python` | `PyUnicode_Format` | str |
| 0.90% | `python` | `_sre_SRE_Pattern_search` | library |
| 0.87% | `python` | `insertdict` | dict |
| 0.81% | `python` | `dict_get` | dict |
| 0.81% | `python` | `_copy_characters.part.0.constprop.0` | str |
| 0.80% | `python` | `list_append` | list |
| 0.79% | `python` | `visit_decref` | gc |
| 0.72% | `python` | `resize_compact` | str |
| 0.64% | `python` | `PyObject_Vectorcall` | dynamic |
| 0.58% | `python` | `visit_reachable` | gc |
| 0.56% | `python` | `PyType_IsSubtype` | dynamic |
| 0.55% | `python` | `list_dealloc` | memory |
| 0.54% | `python` | `sre_search` | library |
| 0.53% | `python` | `_PyObject_Realloc` | memory |
| 0.52% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 0.51% | `python` | `r_object` | import |

## chaos

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 47.69% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 2.66% | `python` | `_PyObject_Malloc` | memory |
| 2.42% | `python` | `_PyObject_Free` | memory |
| 1.98% | `python` | `_PyLong_Subtract` | int |
| 1.91% | `python` | `_PyFrame_ClearExceptCode` | interpreter |
| 1.74% | `python` | `PyType_IsSubtype` | dynamic |
| 1.33% | `python` | `_PyLong_Add` | int |
| 1.32% | `python` | `float_dealloc` | memory |
| 1.07% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.06% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 0.99% | `python` | `compute_range_length` | unknown |
| 0.97% | `python` | `PyFloat_FromDouble` | float |
| 0.93% | `python` | `gc_collect_region.isra.0` | gc |
| 0.84% | `python` | `range_iter` | unknown |
| 0.83% | `python` | `float_div` | float |
| 0.81% | `python` | `float_richcompare` | float |
| 0.80% | `libm-2.31.so` | `f64xsubf128` | library |
| 0.80% | `python` | `_Py_NewReference` | memory |
| 0.79% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 0.77% | `python` | `float_sub` | float |
| 0.76% | `python` | `PyLong_AsDouble` | int |
| 0.74% | `python` | `_PyType_NewManagedObject` | memory |
| 0.74% | `python` | `subtype_dealloc` | memory |
| 0.59% | `python` | `PyLong_FromLong` | int |
| 0.52% | `python` | `PyObject_ClearManagedDict` | dynamic |

## comprehensions

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 40.22% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 5.29% | `python` | `_Py_dict_lookup` | lookup |
| 3.85% | `python` | `_PyObject_Malloc` | memory |
| 3.24% | `python` | `_PyObject_Free` | memory |
| 1.90% | `python` | `dict_get` | dict |
| 1.75% | `python` | `PyObject_RichCompareBool` | dynamic |
| 1.62% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 1.52% | `python` | `_PyObject_Realloc` | memory |
| 1.21% | `python` | `PyDict_GetItemRef` | dict |
| 1.21% | `python` | `insertdict` | dict |
| 1.14% | `python` | `_PyFrame_ClearExceptCode` | interpreter |
| 1.09% | `python` | `long_richcompare` | int |
| 1.05% | `python` | `gc_collect_region.isra.0` | gc |
| 1.05% | `python` | `PyFunction_NewWithQualName` | memory |
| 0.95% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 0.86% | `python` | `PyObject_GC_Del` | gc |
| 0.85% | `python` | `list_dealloc` | memory |
| 0.85% | `python` | `long_hash` | int |
| 0.81% | `python` | `unsafe_tuple_compare` | unknown |
| 0.73% | `python` | `_PyType_Lookup` | lookup |
| 0.73% | `python` | `tupledealloc` | memory |
| 0.72% | `python` | `PyObject_Hash` | dynamic |
| 0.72% | `python` | `_PyObject_GC_New` | gc |
| 0.65% | `python` | `_PyList_AppendTakeRefListResize` | list |
| 0.61% | `python` | `gen_dealloc` | memory |
| 0.58% | `python` | `list_sort_impl` | list |
| 0.52% | `python` | `visit_decref` | gc |

## concurrent_imap

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 24.97% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 3.12% | `python` | `_PyObject_Free` | memory |
| 2.19% | `python` | `_PyObject_Malloc` | memory |
| 2.08% | `[kernel.kallsyms]` | `memset_erms` | kernel |
| 1.60% | `python` | `_PyFrame_ClearExceptCode` | interpreter |
| 1.20% | `python` | `tupledealloc` | memory |
| 1.10% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.04% | `python` | `initialize_locals` | interpreter |
| 1.00% | `python` | `subtype_dealloc` | memory |
| 0.94% | `python` | `_PyType_Lookup` | lookup |
| 0.91% | `[kernel.kallsyms]` | `perf_event_alloc` | kernel |
| 0.91% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 0.90% | `python` | `PyObject_GC_UnTrack` | gc |
| 0.85% | `python` | `PyObject_GenericGetAttr` | dynamic |
| 0.79% | `python` | `PyObject_ClearManagedDict` | dynamic |
| 0.75% | `python` | `PyObject_GC_Del` | gc |
| 0.67% | `python` | `_Py_dict_lookup` | lookup |
| 0.60% | `python` | `_PyEvalFramePushAndInit` | interpreter |
| 0.58% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 0.58% | `python` | `tuple_alloc` | memory |
| 0.56% | `python` | `PyObject_GetAttr` | dynamic |
| 0.55% | `[kernel.kallsyms]` | `clear_page_erms` | kernel |
| 0.51% | `[kernel.kallsyms]` | `copy_page` | kernel |
| 0.51% | `python` | `gc_collect_region.isra.0` | gc |

## coroutines

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 44.85% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 5.67% | `python` | `gen_dealloc` | memory |
| 4.10% | `python` | `_PyObject_Malloc` | memory |
| 3.83% | `python` | `_PyObject_Free` | memory |
| 3.04% | `python` | `make_gen` | unknown |
| 2.68% | `python` | `_PyObject_GC_NewVar` | gc |
| 2.09% | `python` | `_PyLong_Subtract` | int |
| 2.03% | `python` | `_PyFrame_ClearExceptCode` | interpreter |
| 1.60% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 1.59% | `python` | `_Py_MakeCoro` | unknown |
| 1.50% | `python` | `PyObject_CallFinalizerFromDealloc` | memory |
| 1.32% | `python` | `_PyLong_Add` | int |
| 1.30% | `python` | `PyObject_GC_Del` | gc |
| 1.28% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 1.22% | `python` | `gc_collect_region.isra.0` | gc |
| 0.90% | `python` | `_PyObject_GC_Link` | gc |
| 0.76% | `python` | `_PyCoro_GetAwaitableIter` | unknown |
| 0.72% | `python` | `_PyThreadState_PopFrame` | interpreter |
| 0.61% | `python` | `visit_decref` | gc |
| 0.59% | `libc-2.31.so` | `__nss_database_lookup` | libc |

## coverage

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 15.07% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 7.32% | `python` | `call_instrumentation_vector.part.0` | unknown |
| 5.88% | `tracer.cpython-313-x86_64-linux-gnu.so` | `CTracer_trace` | library |
| 5.33% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 3.09% | `python` | `_Py_call_instrumentation_line` | unknown |
| 3.05% | `python` | `_PyObject_Free` | memory |
| 3.02% | `python` | `_PyObject_Malloc` | memory |
| 2.96% | `python` | `_Py_dict_lookup` | lookup |
| 2.47% | `python` | `siphash13` | str |
| 1.64% | `python` | `gc_collect_region.isra.0` | gc |
| 1.62% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.62% | `python` | `PyLong_FromLong` | int |
| 1.53% | `python` | `PyDict_GetItem` | dict |
| 1.20% | `python` | `set_add_entry` | miscobj |
| 1.17% | `python` | `_PyObject_GenericSetAttrWithDict` | dynamic |
| 1.14% | `python` | `_PyUnicode_InternInPlace` | str |
| 0.97% | `python` | `_Py_hashtable_get_entry_generic` | unknown |
| 0.91% | `python` | `_PyFrame_ClearExceptCode` | interpreter |
| 0.90% | `python` | `visit_decref` | gc |
| 0.81% | `python` | `_PyType_Lookup` | lookup |
| 0.73% | `python` | `dict_setdefault_ref_lock_held` | dict |
| 0.73% | `python` | `PyObject_GC_Del` | gc |
| 0.72% | `python` | `visit_reachable` | gc |
| 0.71% | `python` | `PySet_Add` | unknown |
| 0.71% | `python` | `unicode_decode_utf8` | str |
| 0.61% | `python` | `ascii_decode` | str |
| 0.60% | `python` | `_Py_call_instrumentation_jump` | unknown |
| 0.59% | `python` | `PyUnicode_New.part.0` | memory |
| 0.57% | `python` | `_PyObject_GC_NewVar` | gc |
| 0.57% | `python` | `sys_trace_return` | unknown |
| 0.55% | `python` | `frame_dealloc` | memory |
| 0.53% | `python` | `r_object` | import |
| 0.52% | `python` | `_PyCode_GetCode` | unknown |

## crypto_pyaes

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 42.04% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 7.04% | `python` | `_PyObject_Free` | memory |
| 6.85% | `python` | `long_bitwise` | int |
| 6.09% | `python` | `_PyObject_Malloc` | memory |
| 2.82% | `python` | `long_rshift1` | int |
| 1.96% | `python` | `l_mod` | int |
| 1.43% | `python` | `long_rshift` | int |
| 1.35% | `python` | `long_and` | int |
| 1.02% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 0.97% | `python` | `_PyLong_Add` | int |
| 0.97% | `python` | `PyNumber_Xor` | dynamic |
| 0.97% | `python` | `PyLong_FromLong` | int |
| 0.94% | `python` | `long_dealloc` | memory |
| 0.89% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 0.89% | `python` | `PyNumber_And` | dynamic |
| 0.85% | `python` | `gc_collect_region.isra.0` | gc |
| 0.79% | `python` | `long_xor` | int |
| 0.76% | `python` | `_Py_NewReference` | memory |
| 0.68% | `python` | `PyNumber_Rshift` | dynamic |
| 0.62% | `python` | `PyNumber_Remainder` | dynamic |
| 0.57% | `python` | `PyObject_Malloc` | dynamic |
| 0.53% | `python` | `long_mod` | int |
| 0.52% | `python` | `compute_range_length` | unknown |
| 0.51% | `python` | `_Py_dict_lookup` | lookup |

## dask

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 24.64% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 3.94% | `python` | `gc_collect_region.isra.0` | gc |
| 3.04% | `python` | `_PyObject_Malloc` | memory |
| 2.55% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 2.49% | `python` | `visit_decref` | gc |
| 2.38% | `python` | `_PyObject_Free` | memory |
| 1.93% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.82% | `python` | `visit_reachable` | gc |
| 1.44% | `python` | `visit_add_to_container` | gc |
| 1.43% | `python` | `_PyFrame_ClearExceptCode` | interpreter |
| 1.42% | `python` | `_Py_dict_lookup` | lookup |
| 1.27% | `python` | `tupledealloc` | memory |
| 1.09% | `python` | `initialize_locals` | interpreter |
| 0.94% | `python` | `dict_dealloc` | memory |
| 0.86% | `python` | `PyObject_GC_UnTrack` | gc |
| 0.86% | `python` | `PyBytes_Repr` | str |
| 0.75% | `python` | `_PyType_Lookup` | lookup |
| 0.60% | `python` | `insertdict` | dict |
| 0.53% | `libc-2.31.so` | `pthread_attr_setschedparam` | libc |

## deepcopy

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 44.65% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 4.76% | `python` | `_Py_dict_lookup` | lookup |
| 3.75% | `python` | `_PyObject_Free` | memory |
| 3.68% | `python` | `_PyObject_Malloc` | memory |
| 3.16% | `python` | `_PyFrame_ClearExceptCode` | interpreter |
| 1.84% | `python` | `dict_get` | dict |
| 1.34% | `python` | `PyLong_FromVoidPtr` | int |
| 1.23% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 1.07% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 0.98% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 0.86% | `python` | `sys_audit_tstate` | unknown |
| 0.82% | `python` | `long_hash` | int |
| 0.79% | `python` | `insertdict` | dict |
| 0.74% | `python` | `PySys_Audit` | unknown |
| 0.71% | `python` | `initialize_locals` | interpreter |
| 0.71% | `python` | `gc_collect_region.isra.0` | gc |
| 0.69% | `python` | `_PyType_Lookup` | lookup |
| 0.67% | `python` | `insert_to_emptydict` | dict |
| 0.59% | `python` | `tupledealloc` | memory |
| 0.57% | `python` | `_PyObject_Realloc` | memory |
| 0.56% | `python` | `list_append` | list |
| 0.55% | `python` | `PyObject_RichCompareBool` | dynamic |
| 0.54% | `python` | `long_richcompare` | int |
| 0.53% | `python` | `_PyObject_GenericGetAttrWithDict` | dynamic |
| 0.52% | `python` | `PyObject_Hash` | dynamic |
| 0.50% | `python` | `dict_dealloc` | memory |

## deltablue

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 55.10% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 3.46% | `python` | `_PyFrame_ClearExceptCode` | interpreter |
| 2.52% | `python` | `gc_collect_region.isra.0` | gc |
| 2.32% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 2.30% | `python` | `_PyObject_Malloc` | memory |
| 1.73% | `python` | `_PyObject_Free` | memory |
| 1.62% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 1.15% | `python` | `_PyType_Lookup` | lookup |
| 1.12% | `python` | `_PyThreadState_PopFrame` | interpreter |
| 1.02% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.01% | `python` | `visit_decref` | gc |
| 0.62% | `python` | `_Py_dict_lookup` | lookup |
| 0.56% | `python` | `_PyObject_GetMethod` | dynamic |
| 0.52% | `python` | `visit_reachable` | gc |
| 0.52% | `python` | `_Py_type_getattro` | lookup |

## django_template

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 34.08% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 3.31% | `python` | `_PyObject_Malloc` | memory |
| 3.01% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 2.92% | `python` | `_PyObject_Free` | memory |
| 2.02% | `python` | `_PyFrame_ClearExceptCode` | interpreter |
| 1.93% | `python` | `gc_collect_region.isra.0` | gc |
| 1.54% | `python` | `_Py_dict_lookup` | lookup |
| 1.51% | `python` | `_PyType_Lookup` | lookup |
| 1.48% | `python` | `_PyObject_GenericGetAttrWithDict` | dynamic |
| 1.40% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.21% | `python` | `initialize_locals` | interpreter |
| 0.97% | `python` | `visit_decref` | gc |
| 0.93% | `python` | `tupledealloc` | memory |
| 0.85% | `python` | `replace` | str |
| 0.81% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 0.76% | `python` | `visit_reachable` | gc |
| 0.75% | `python` | `insertdict` | dict |
| 0.70% | `python` | `_PyEvalFramePushAndInit` | interpreter |
| 0.65% | `python` | `PyType_IsSubtype` | dynamic |
| 0.64% | `python` | `PyObject_GC_Del` | gc |
| 0.62% | `python` | `dict_dealloc` | memory |
| 0.60% | `python` | `_PyObject_GC_New` | gc |
| 0.59% | `python` | `r_object` | import |
| 0.57% | `python` | `PyObject_GC_UnTrack` | gc |
| 0.51% | `python` | `_Py_NewReference` | memory |

## djangocms

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 18.57% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 5.31% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 3.28% | `python` | `gc_collect_region.isra.0` | gc |
| 2.73% | `python` | `_PyObject_Malloc` | memory |
| 2.27% | `python` | `_Py_dict_lookup` | lookup |
| 2.10% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.94% | `python` | `_PyObject_Free` | memory |
| 1.62% | `python` | `visit_decref` | gc |
| 1.49% | `libc-2.31.so` | `pthread_attr_setschedparam` | libc |
| 1.36% | `python` | `_PyType_Lookup` | lookup |
| 1.32% | `libsqlite3.so.0.8.6` | `sqlite3_exec` | library |
| 1.18% | `python` | `find_name_in_mro` | lookup |
| 1.15% | `python` | `_PyFrame_ClearExceptCode` | interpreter |
| 1.06% | `python` | `visit_add_to_container` | gc |
| 1.05% | `python` | `visit_reachable` | gc |
| 0.92% | `python` | `dict_traverse` | gc |
| 0.87% | `python` | `tupledealloc` | memory |
| 0.86% | `python` | `_PyDict_GetItem_KnownHash` | dict |
| 0.73% | `python` | `sre_ucs1_match` | library |
| 0.72% | `python` | `initialize_locals` | interpreter |
| 0.66% | `python` | `update_one_slot` | lookup |
| 0.63% | `python` | `dict_dealloc` | memory |
| 0.60% | `libz.so.1.2.11` | `inflateBackEnd` | library |
| 0.57% | `python` | `PyObject_GenericGetAttr` | dynamic |
| 0.52% | `python` | `PyDict_GetItemRef` | dict |
| 0.51% | `libsqlite3.so.0.8.6` | `sqlite3_str_value` | library |
| 0.51% | `python` | `insertdict` | dict |

## docutils

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 25.82% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 6.39% | `python` | `sre_ucs1_match` | library |
| 6.12% | `python` | `gc_collect_region.isra.0` | gc |
| 3.81% | `python` | `_PyObject_Malloc` | memory |
| 2.95% | `python` | `_PyObject_Free` | memory |
| 2.93% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 2.16% | `python` | `_PyType_Lookup` | lookup |
| 2.04% | `python` | `visit_add_to_container` | gc |
| 1.83% | `python` | `visit_decref` | gc |
| 1.81% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.60% | `python` | `sre_ucs2_charset.isra.0` | library |
| 1.54% | `python` | `_Py_dict_lookup` | lookup |
| 1.38% | `python` | `_PyFrame_ClearExceptCode` | interpreter |
| 1.38% | `python` | `PyObject_GenericGetAttr` | dynamic |
| 1.18% | `python` | `list_dealloc` | memory |
| 0.95% | `python` | `dict_traverse` | gc |
| 0.93% | `python` | `visit_reachable` | gc |
| 0.69% | `python` | `tupledealloc` | memory |
| 0.69% | `python` | `_PyObject_TryGetInstanceAttribute` | dynamic |
| 0.65% | `python` | `initialize_locals` | interpreter |
| 0.65% | `python` | `_PyObject_GetMethod` | dynamic |
| 0.63% | `python` | `list_traverse` | gc |
| 0.61% | `libc-2.31.so` | `pthread_attr_setschedparam` | libc |
| 0.58% | `python` | `PyObject_GC_UnTrack` | gc |
| 0.55% | `python` | `PyType_IsSubtype` | dynamic |
| 0.55% | `python` | `list_slice_lock_held.isra.0` | list |
| 0.50% | `python` | `dict_dealloc` | memory |

## dulwich_log

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 29.29% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 3.84% | `python` | `_PyObject_Malloc` | memory |
| 3.08% | `python` | `_PyObject_Free` | memory |
| 2.59% | `libz.so.1.2.11` | `inflateCodesUsed` | library |
| 2.45% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.58% | `libz.so.1.2.11` | `inflateBackEnd` | library |
| 1.44% | `libz.so.1.2.11` | `inflate` | library |
| 1.32% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 1.28% | `python` | `_PyFrame_ClearExceptCode` | interpreter |
| 1.20% | `python` | `gc_collect_region.isra.0` | gc |
| 0.74% | `python` | `tupledealloc` | memory |
| 0.71% | `python` | `visit_decref` | gc |
| 0.70% | `libc-2.31.so` | `pthread_attr_setschedparam` | libc |
| 0.69% | `python` | `_Py_dict_lookup` | lookup |
| 0.58% | `python` | `_PyType_Lookup` | lookup |
| 0.55% | `[kernel.kallsyms]` | `__d_lookup_rcu` | kernel |
| 0.52% | `python` | `initialize_locals` | interpreter |
| 0.51% | `[kernel.kallsyms]` | `copy_user_enhanced_fast_string` | kernel |

## fannkuch

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 36.62% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 8.33% | `python` | `PySlice_AdjustIndices` | miscobj |
| 5.12% | `python` | `list_ass_slice_lock_held` | list |
| 4.94% | `python` | `list_subscript` | list |
| 3.79% | `python` | `_PyObject_Free` | memory |
| 3.59% | `python` | `slice_dealloc` | memory |
| 3.02% | `python` | `_PyObject_Malloc` | memory |
| 2.53% | `python` | `list_dealloc` | memory |
| 2.36% | `python` | `_PyLong_Add` | int |
| 2.34% | `python` | `_PyEval_SliceIndex` | interpreter |
| 2.25% | `python` | `_PyBuildSlice_ConsumeRefs` | miscobj |
| 2.07% | `python` | `PySlice_New` | memory |
| 2.05% | `python` | `_Py_NewReference` | memory |
| 2.05% | `python` | `PyNumber_AsSsize_t` | dynamic |
| 1.85% | `python` | `PySlice_Unpack` | miscobj |
| 1.60% | `python` | `list_ass_subscript` | list |
| 1.43% | `python` | `PyList_New` | memory |
| 1.37% | `python` | `PyLong_AsSsize_t` | int |
| 1.05% | `python` | `list_insert` | list |
| 0.97% | `python` | `PyObject_GetItem` | dynamic |
| 0.70% | `python` | `_PyLong_Subtract` | int |
| 0.65% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 0.56% | `python` | `PyObject_GC_UnTrack` | gc |
| 0.53% | `python` | `PyObject_SetItem` | dynamic |
| 0.53% | `python` | `list_pop` | list |

## float

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 39.40% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 4.25% | `libm-2.31.so` | `f64xsubf128` | library |
| 3.42% | `python` | `_PyObject_Malloc` | memory |
| 2.59% | `python` | `_PyObject_Free` | memory |
| 2.20% | `python` | `gc_collect_region.isra.0` | gc |
| 1.79% | `python` | `PyFloat_FromDouble` | float |
| 1.75% | `python` | `subtype_traverse` | gc |
| 1.64% | `python` | `visit_decref` | gc |
| 1.58% | `python` | `float_dealloc` | memory |
| 1.54% | `python` | `_PyFrame_ClearExceptCode` | interpreter |
| 1.51% | `python` | `subtype_dealloc` | memory |
| 1.46% | `python` | `visit_reachable` | gc |
| 1.16% | `python` | `float_div` | float |
| 1.11% | `python` | `_Py_NewReference` | memory |
| 1.04% | `python` | `visit_add_to_container` | gc |
| 1.01% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 0.93% | `python` | `PyType_IsSubtype` | dynamic |
| 0.88% | `python` | `initialize_locals` | interpreter |
| 0.84% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 0.75% | `python` | `tupledealloc` | memory |
| 0.66% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 0.64% | `python` | `PyType_GenericAlloc` | memory |
| 0.61% | `python` | `PyNumber_InPlaceTrueDivide` | dynamic |
| 0.58% | `python` | `_PyEvalFramePushAndInit` | interpreter |
| 0.57% | `python` | `_PyType_Lookup` | lookup |
| 0.55% | `python` | `slot_tp_init` | unknown |
| 0.53% | `python` | `_Py_Dealloc` | memory |
| 0.51% | `python` | `long_float` | int |

## gc_collect

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 26.98% | `python` | `gc_collect_region.isra.0` | gc |
| 13.54% | `python` | `visit_reachable` | gc |
| 13.05% | `python` | `visit_decref` | gc |
| 7.62% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 4.50% | `python` | `_PyGC_Collect` | gc |
| 4.27% | `python` | `dict_traverse` | gc |
| 1.72% | `python` | `PyObject_IS_GC` | gc |
| 1.70% | `python` | `func_traverse` | gc |
| 1.43% | `python` | `_PyDict_MaybeUntrack` | gc |
| 1.42% | `python` | `subtype_traverse` | gc |
| 1.32% | `python` | `PyObject_VisitManagedDict` | dynamic |
| 1.17% | `python` | `set_traverse` | gc |
| 1.08% | `python` | `type_is_gc` | gc |
| 1.03% | `python` | `_PyObject_Malloc` | memory |
| 0.73% | `python` | `tupletraverse` | tuple |
| 0.70% | `python` | `_PyObject_Free` | memory |
| 0.68% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 0.66% | `python` | `type_traverse` | gc |
| 0.58% | `python` | `_PyFrame_ClearExceptCode` | interpreter |
| 0.53% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 0.52% | `python` | `list_traverse` | gc |

## gc_traversal

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 28.63% | `python` | `visit_reachable` | gc |
| 20.32% | `python` | `visit_decref` | gc |
| 15.72% | `python` | `list_traverse` | gc |
| 10.95% | `python` | `gc_collect_region.isra.0` | gc |
| 4.72% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 1.86% | `python` | `dict_traverse` | gc |
| 0.78% | `python` | `PyObject_IS_GC` | gc |
| 0.71% | `python` | `func_traverse` | gc |
| 0.69% | `python` | `_PyObject_Free` | memory |
| 0.67% | `python` | `_PyObject_Malloc` | memory |
| 0.65% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 0.63% | `python` | `_PyDict_MaybeUntrack` | gc |
| 0.56% | `python` | `set_traverse` | gc |

## generators

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 50.95% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 4.23% | `python` | `_PyObject_Malloc` | memory |
| 3.10% | `python` | `_PyObject_Free` | memory |
| 1.89% | `python` | `gc_collect_region.isra.0` | gc |
| 1.35% | `python` | `gen_dealloc` | memory |
| 1.26% | `python` | `_PyFrame_ClearExceptCode` | interpreter |
| 1.12% | `python` | `initialize_locals` | interpreter |
| 1.06% | `python` | `long_add` | int |
| 1.05% | `python` | `PyObject_RichCompareBool` | dynamic |
| 0.92% | `python` | `visit_decref` | gc |
| 0.86% | `python` | `_PyEvalFramePushAndInit` | interpreter |
| 0.82% | `python` | `visit_reachable` | gc |
| 0.79% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 0.73% | `python` | `range_subscript` | unknown |
| 0.73% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 0.72% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 0.71% | `python` | `make_gen` | unknown |
| 0.69% | `python` | `compute_range_length` | unknown |
| 0.67% | `python` | `_PyObject_GC_NewVar` | gc |
| 0.64% | `python` | `_PyType_Lookup` | lookup |
| 0.62% | `python` | `PyNumber_Add` | dynamic |
| 0.59% | `python` | `_PyBuildSlice_ConsumeRefs` | miscobj |
| 0.59% | `python` | `long_richcompare` | int |
| 0.56% | `python` | `slot_tp_iter` | unknown |
| 0.52% | `python` | `PyObject_GC_Del` | gc |

## genshi

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 43.10% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 3.61% | `python` | `_PyObject_Malloc` | memory |
| 2.70% | `python` | `_PyObject_Free` | memory |
| 2.65% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 2.26% | `python` | `_Py_dict_lookup` | lookup |
| 1.32% | `python` | `_PyFrame_ClearExceptCode` | interpreter |
| 1.30% | `python` | `insertdict` | dict |
| 1.21% | `python` | `tupledealloc` | memory |
| 1.16% | `python` | `gc_collect_region.isra.0` | gc |
| 1.08% | `python` | `_PyType_Lookup` | lookup |
| 1.04% | `python` | `insert_to_emptydict` | dict |
| 1.02% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 0.80% | `python` | `_PyTuple_FromArraySteal` | tuple |
| 0.80% | `python` | `dict_dealloc` | memory |
| 0.74% | `python` | `_PyObject_GC_New` | gc |
| 0.72% | `python` | `_PyDict_FromItems` | dict |
| 0.63% | `python` | `PyObject_GC_UnTrack` | gc |
| 0.61% | `libc-2.31.so` | `pthread_attr_setschedparam` | libc |
| 0.60% | `python` | `PyDict_GetItemRef` | dict |
| 0.56% | `python` | `long_to_decimal_string_internal` | int |
| 0.54% | `python` | `pattern_subx` | library |
| 0.53% | `python` | `visit_decref` | gc |
| 0.52% | `python` | `_PyObject_GetMethod` | dynamic |
| 0.51% | `python` | `initialize_locals` | interpreter |

## go

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 61.04% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 2.67% | `python` | `_PyFrame_ClearExceptCode` | interpreter |
| 2.15% | `python` | `_PyObject_Free` | memory |
| 2.13% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 1.85% | `python` | `_PyObject_GetMethod` | dynamic |
| 1.71% | `python` | `_PyObject_Malloc` | memory |
| 1.30% | `python` | `_Py_dict_lookup` | lookup |
| 1.11% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 0.99% | `python` | `gc_collect_region.isra.0` | gc |
| 0.95% | `python` | `_PyType_Lookup` | lookup |
| 0.91% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 0.83% | `python` | `long_bitwise` | int |
| 0.79% | `python` | `PyDict_GetItemRef` | dict |
| 0.59% | `python` | `_PyLong_Add` | int |
| 0.54% | `python` | `visit_decref` | gc |
| 0.54% | `python` | `_PyThreadState_PopFrame` | interpreter |
| 0.51% | `python` | `initialize_locals` | interpreter |

## gunicorn

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 27.85% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 2.90% | `python` | `_PyObject_Malloc` | memory |
| 2.59% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 2.32% | `python` | `_PyObject_Free` | memory |
| 2.17% | `python` | `_PyFrame_ClearExceptCode` | interpreter |
| 2.11% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.96% | `python` | `gc_collect_region.isra.0` | gc |
| 1.40% | `python` | `_Py_dict_lookup` | lookup |
| 1.35% | `python` | `initialize_locals` | interpreter |
| 1.22% | `python` | `tupledealloc` | memory |
| 1.00% | `python` | `_PyType_Lookup` | lookup |
| 0.99% | `python` | `visit_decref` | gc |
| 0.65% | `libc-2.31.so` | `pthread_attr_setschedparam` | libc |
| 0.63% | `python` | `visit_reachable` | gc |
| 0.59% | `python` | `PyDict_GetItemRef` | dict |
| 0.58% | `python` | `dict_dealloc` | memory |
| 0.55% | `python` | `sre_ucs1_match` | library |
| 0.55% | `python` | `subtype_dealloc` | memory |
| 0.53% | `python` | `PyObject_GC_UnTrack` | gc |
| 0.51% | `python` | `r_object` | import |

## hexiom

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 52.26% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 3.54% | `python` | `PyObject_RichCompareBool` | dynamic |
| 2.35% | `python` | `list_contains` | list |
| 2.10% | `python` | `long_richcompare` | int |
| 1.99% | `python` | `_PyFrame_ClearExceptCode` | interpreter |
| 1.88% | `python` | `_PyObject_Malloc` | memory |
| 1.81% | `python` | `_PyObject_Free` | memory |
| 1.25% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 1.21% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.19% | `python` | `gc_collect_region.isra.0` | gc |
| 0.91% | `python` | `gen_iternext` | unknown |
| 0.88% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 0.66% | `python` | `builtin_sum` | unknown |
| 0.65% | `python` | `_Py_dict_lookup` | lookup |
| 0.60% | `python` | `visit_decref` | gc |
| 0.59% | `python` | `PyLong_FromLong` | int |
| 0.55% | `python` | `PyLong_FromSsize_t` | int |
| 0.53% | `python` | `_PyThreadState_PopFrame` | interpreter |

## html5lib

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 36.24% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 4.93% | `python` | `sre_ucs2_charset.isra.0` | library |
| 3.43% | `python` | `gc_collect_region.isra.0` | gc |
| 2.94% | `python` | `_PyObject_Malloc` | memory |
| 2.32% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 2.20% | `python` | `_PyObject_Free` | memory |
| 1.59% | `python` | `_Py_dict_lookup` | lookup |
| 1.40% | `python` | `visit_decref` | gc |
| 1.37% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.35% | `python` | `_PyFrame_ClearExceptCode` | interpreter |
| 0.88% | `python` | `PyDict_GetItemRef` | dict |
| 0.72% | `python` | `PyObject_RichCompareBool` | dynamic |
| 0.71% | `libc-2.31.so` | `pthread_attr_setschedparam` | libc |
| 0.69% | `python` | `sre_ucs1_count` | library |
| 0.67% | `python` | `visit_reachable` | gc |
| 0.63% | `python` | `PyObject_GenericGetAttr` | dynamic |
| 0.60% | `python` | `initialize_locals` | interpreter |
| 0.59% | `python` | `tupledealloc` | memory |
| 0.58% | `python` | `_PyType_Lookup` | lookup |
| 0.52% | `python` | `visit_add_to_container` | gc |

## json

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 12.42% | `_json.cpython-313-x86_64-linux-gnu.so` | `scanstring_unicode` | library |
| 7.92% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 7.08% | `python` | `_PyObject_Malloc` | memory |
| 6.27% | `_json.cpython-313-x86_64-linux-gnu.so` | `scan_once_unicode` | library |
| 5.32% | `python` | `_PyObject_Free` | memory |
| 4.93% | `python` | `siphash13` | str |
| 4.37% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 3.14% | `python` | `dict_setdefault_ref_lock_held` | dict |
| 2.41% | `python` | `_Py_dict_lookup` | lookup |
| 2.39% | `python` | `insertdict` | dict |
| 2.35% | `python` | `PyLong_FromString` | int |
| 2.17% | `python` | `PyUnicode_Substring` | str |
| 1.92% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.83% | `libc-2.31.so` | `pthread_attr_setschedparam` | libc |
| 1.81% | `python` | `dict_dealloc` | memory |
| 1.62% | `python` | `PyUnicode_New.part.0` | memory |
| 1.41% | `python` | `build_indices_unicode` | dict |
| 1.35% | `python` | `find_empty_slot` | dict |
| 0.97% | `python` | `PyObject_IS_GC` | gc |
| 0.81% | `python` | `gc_collect_region.isra.0` | gc |
| 0.79% | `python` | `PyDict_SetItem` | dict |
| 0.74% | `python` | `insert_to_emptydict` | dict |
| 0.72% | `python` | `_sre_SRE_Pattern_match` | library |
| 0.60% | `python` | `initialize_locals` | interpreter |
| 0.60% | `python` | `unicode_dealloc` | memory |
| 0.56% | `python` | `sre_ucs1_match` | library |
| 0.56% | `python` | `_PyFrame_ClearExceptCode` | interpreter |
| 0.53% | `python` | `dictresize` | dict |

## json_dumps

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 13.56% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 7.84% | `python` | `_PyObject_Malloc` | memory |
| 6.17% | `_json.cpython-313-x86_64-linux-gnu.so` | `py_encode_basestring_ascii` | library |
| 5.35% | `python` | `_PyObject_Free` | memory |
| 3.36% | `python` | `_copy_characters.part.0.constprop.0` | str |
| 2.71% | `python` | `_Py_dict_lookup` | lookup |
| 2.49% | `python` | `_PyUnicodeWriter_WriteStr` | str |
| 2.45% | `_json.cpython-313-x86_64-linux-gnu.so` | `encoder_listencode_obj` | library |
| 2.30% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 2.28% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 2.15% | `python` | `resize_compact` | str |
| 1.85% | `python` | `vgetargskeywords.constprop.0` | calls |
| 1.81% | `python` | `PyUnicode_New` | memory |
| 1.53% | `_json.cpython-313-x86_64-linux-gnu.so` | `encoder_encode_key_value` | library |
| 1.30% | `python` | `gc_collect_region.isra.0` | gc |
| 1.19% | `python` | `convertitem.constprop.0` | unknown |
| 1.16% | `python` | `PyDict_GetItemRef` | dict |
| 1.08% | `python` | `_PyObject_Realloc` | memory |
| 1.08% | `python` | `PyDict_Next` | dict |
| 1.07% | `python` | `tupledealloc` | memory |
| 1.00% | `python` | `_PyFrame_ClearExceptCode` | interpreter |
| 0.99% | `python` | `initialize_locals` | interpreter |
| 0.80% | `python` | `_PyUnicodeWriter_PrepareInternal` | str |
| 0.74% | `python` | `long_to_decimal_string_internal` | int |
| 0.65% | `python` | `_PyType_Lookup` | lookup |
| 0.64% | `python` | `visit_decref` | gc |
| 0.61% | `python` | `_Py_NewReference` | memory |
| 0.61% | `python` | `unicode_dealloc` | memory |
| 0.56% | `python` | `dict_dealloc` | memory |
| 0.54% | `python` | `_Py_Dealloc` | memory |
| 0.53% | `python` | `PyType_IsSubtype` | dynamic |
| 0.53% | `python` | `_PyObject_GenericGetAttrWithDict` | dynamic |

## json_loads

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 13.62% | `_json.cpython-313-x86_64-linux-gnu.so` | `scanstring_unicode` | library |
| 7.71% | `python` | `_PyObject_Malloc` | memory |
| 7.27% | `_json.cpython-313-x86_64-linux-gnu.so` | `scan_once_unicode` | library |
| 5.95% | `python` | `siphash13` | str |
| 5.88% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 5.75% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 5.44% | `python` | `_PyObject_Free` | memory |
| 3.26% | `python` | `PyUnicode_Substring` | str |
| 2.80% | `python` | `insertdict` | dict |
| 2.68% | `python` | `_Py_dict_lookup` | lookup |
| 2.65% | `python` | `dict_setdefault_ref_lock_held` | dict |
| 2.64% | `python` | `PyLong_FromString` | int |
| 2.47% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 2.35% | `python` | `PyUnicode_New.part.0` | memory |
| 1.23% | `python` | `find_empty_slot` | dict |
| 1.10% | `python` | `dict_dealloc` | memory |
| 1.03% | `libc-2.31.so` | `pthread_attr_setschedparam` | libc |
| 0.93% | `python` | `gc_collect_region.isra.0` | gc |
| 0.83% | `python` | `build_indices_unicode` | dict |
| 0.77% | `python` | `PyDict_SetItem` | dict |
| 0.73% | `python` | `PyObject_IS_GC` | gc |
| 0.68% | `python` | `unicode_dealloc` | memory |
| 0.60% | `python` | `_Py_NewReference` | memory |

## logging

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 43.52% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 3.54% | `python` | `_PyFrame_ClearExceptCode` | interpreter |
| 2.77% | `python` | `initialize_locals` | interpreter |
| 2.52% | `python` | `_PyObject_Malloc` | memory |
| 2.19% | `python` | `_PyObject_Free` | memory |
| 2.08% | `python` | `_Py_dict_lookup` | lookup |
| 1.71% | `python` | `dict_dealloc` | memory |
| 1.67% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.65% | `python` | `PyCode_Addr2Line` | exceptions |
| 1.64% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 1.58% | `python` | `_PyEvalFramePushAndInit` | interpreter |
| 1.34% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 0.97% | `python` | `PyDict_New` | memory |
| 0.82% | `python` | `PyDict_GetItemRef` | dict |
| 0.78% | `python` | `_Py_NewReference` | memory |
| 0.77% | `python` | `_PyThreadState_PopFrame` | interpreter |
| 0.73% | `python` | `_PyType_Lookup` | lookup |
| 0.68% | `python` | `PyObject_GenericGetAttr` | dynamic |
| 0.63% | `python` | `gc_collect_region.isra.0` | gc |
| 0.60% | `python` | `PyUnicode_Contains` | str |
| 0.52% | `python` | `tupledealloc` | memory |

## mako

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 32.35% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 6.27% | `python` | `replace` | str |
| 3.94% | `python` | `_PyObject_Malloc` | memory |
| 3.39% | `python` | `long_to_decimal_string_internal` | int |
| 3.38% | `python` | `_PyObject_Free` | memory |
| 2.94% | `python` | `_PyUnicode_JoinArray.part.0` | str |
| 2.20% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 2.03% | `python` | `unicode_replace` | str |
| 1.67% | `python` | `deque_append` | miscobj |
| 1.65% | `python` | `dequeiter_next` | miscobj |
| 1.63% | `python` | `gc_collect_region.isra.0` | gc |
| 1.57% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 0.89% | `python` | `_list_extend` | unknown |
| 0.88% | `python` | `list_dealloc` | memory |
| 0.84% | `python` | `visit_decref` | gc |
| 0.82% | `python` | `_PyFrame_ClearExceptCode` | interpreter |
| 0.75% | `python` | `PyErr_CheckSignals` | exceptions |
| 0.72% | `libc-2.31.so` | `pthread_attr_setschedparam` | libc |
| 0.69% | `python` | `_Py_dict_lookup` | lookup |
| 0.66% | `python` | `PyUnicode_New` | memory |
| 0.64% | `python` | `deque_clear.part.0` | miscobj |
| 0.62% | `python` | `sre_ucs2_charset.isra.0` | library |
| 0.59% | `python` | `visit_reachable` | gc |
| 0.57% | `python` | `PyObject_Str` | dynamic |
| 0.56% | `python` | `_PyEval_FrameClearAndPop` | interpreter |

## mdp

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 27.73% | `python` | `tuplehash` | tuple |
| 16.71% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 13.05% | `python` | `PyObject_Hash` | dynamic |
| 11.16% | `python` | `long_hash` | int |
| 5.78% | `python` | `_Py_dict_lookup` | lookup |
| 2.93% | `python` | `PyObject_RichCompareBool` | dynamic |
| 1.79% | `python` | `tuplerichcompare` | tuple |
| 1.41% | `python` | `_PyObject_Malloc` | memory |
| 1.36% | `python` | `_PyObject_Free` | memory |
| 1.16% | `python` | `dict_subscript` | dict |
| 0.94% | `python` | `_PyLong_GCD` | int |
| 0.71% | `python` | `PyDict_GetItemRef` | dict |
| 0.68% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 0.67% | `python` | `_PyFrame_ClearExceptCode` | interpreter |
| 0.52% | `libc-2.31.so` | `__nss_database_lookup` | libc |

## meteor_contest

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 24.45% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 7.07% | `python` | `set_issubset_impl` | miscobj |
| 6.99% | `python` | `set_lookkey` | miscobj |
| 4.78% | `python` | `setiter_iternext` | miscobj |
| 3.38% | `python` | `set_difference` | miscobj |
| 2.94% | `python` | `_PyObject_Free` | memory |
| 2.83% | `python` | `_PyObject_Malloc` | memory |
| 2.79% | `python` | `set_dealloc` | memory |
| 2.43% | `python` | `PyObject_RichCompareBool` | dynamic |
| 1.87% | `python` | `set_add_entry` | miscobj |
| 1.65% | `python` | `list_dealloc` | memory |
| 1.45% | `python` | `long_richcompare` | int |
| 1.38% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.32% | `python` | `min_max` | unknown |
| 1.18% | `python` | `gc_collect_region.isra.0` | gc |
| 1.17% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 1.11% | `python` | `list_slice_lock_held.isra.0` | list |
| 1.05% | `python` | `PyObject_RichCompare` | dynamic |
| 0.98% | `python` | `PyIter_Next` | dynamic |
| 0.95% | `python` | `set_intersection` | miscobj |
| 0.85% | `python` | `set_table_resize` | miscobj |
| 0.70% | `python` | `PyObject_GC_Del` | gc |
| 0.67% | `python` | `_PyFrame_ClearExceptCode` | interpreter |
| 0.66% | `python` | `PyType_GenericAlloc` | memory |
| 0.59% | `python` | `set_merge_lock_held.part.0` | miscobj |
| 0.57% | `python` | `_Py_dict_lookup` | lookup |
| 0.56% | `python` | `visit_decref` | gc |
| 0.55% | `python` | `_PyObject_GC_New` | gc |
| 0.51% | `python` | `set_richcompare` | miscobj |

## mypy2

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 29.53% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 14.46% | `python` | `gc_collect_region.isra.0` | gc |
| 3.12% | `python` | `_PyObject_Malloc` | memory |
| 2.76% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 2.65% | `python` | `visit_decref` | gc |
| 2.25% | `python` | `_PyFrame_ClearExceptCode` | interpreter |
| 2.16% | `python` | `_PyObject_Free` | memory |
| 1.53% | `python` | `initialize_locals` | interpreter |
| 1.50% | `python` | `subtype_traverse` | gc |
| 1.48% | `python` | `_Py_dict_lookup` | lookup |
| 1.46% | `python` | `_PyType_Lookup` | lookup |
| 1.32% | `python` | `visit_reachable` | gc |
| 1.27% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.19% | `python` | `subtype_dealloc` | memory |
| 1.04% | `python` | `PyDict_GetItemRef` | dict |
| 0.88% | `_json.cpython-313-x86_64-linux-gnu.so` | `scanstring_unicode` | library |
| 0.85% | `python` | `siphash13` | str |
| 0.78% | `python` | `PyObject_GC_UnTrack` | gc |
| 0.78% | `_json.cpython-313-x86_64-linux-gnu.so` | `scan_once_unicode` | library |
| 0.69% | `python` | `PyType_IsSubtype` | dynamic |
| 0.66% | `python` | `dict_dealloc` | memory |
| 0.63% | `python` | `tupledealloc` | memory |
| 0.57% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 0.55% | `python` | `insertdict` | dict |
| 0.53% | `python` | `list_dealloc` | memory |
| 0.51% | `python` | `list_traverse` | gc |
| 0.50% | `python` | `PyGC_Collect` | gc |

## nbody

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 66.17% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 5.19% | `python` | `PyFloat_FromDouble` | float |
| 3.11% | `libm-2.31.so` | `f64xsubf128` | library |
| 2.76% | `python` | `float_dealloc` | memory |
| 2.60% | `python` | `_Py_NewReference` | memory |
| 1.35% | `python` | `float_pow` | float |
| 0.85% | `python` | `gc_collect_region.isra.0` | gc |
| 0.81% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 0.81% | `python` | `_PyObject_Free` | memory |
| 0.81% | `python` | `_PyObject_Malloc` | memory |

## nqueens

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 32.27% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 4.82% | `python` | `_PyObject_Malloc` | memory |
| 4.53% | `python` | `_PyObject_Free` | memory |
| 2.33% | `python` | `set_add_entry` | miscobj |
| 2.08% | `python` | `gen_iternext` | unknown |
| 1.70% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 1.69% | `python` | `PySlice_AdjustIndices` | miscobj |
| 1.46% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.32% | `python` | `gc_collect_region.isra.0` | gc |
| 1.23% | `python` | `_PyBuildSlice_ConsumeRefs` | miscobj |
| 1.11% | `python` | `list_dealloc` | memory |
| 1.02% | `python` | `_Py_dict_lookup` | lookup |
| 0.98% | `python` | `set_dealloc` | memory |
| 0.94% | `python` | `_PyLong_Add` | int |
| 0.92% | `python` | `_Py_NewReference` | memory |
| 0.90% | `python` | `tupledealloc` | memory |
| 0.80% | `python` | `PyList_New` | memory |
| 0.73% | `python` | `PyObject_GC_Del` | gc |
| 0.70% | `python` | `PyNumber_AsSsize_t` | dynamic |
| 0.70% | `python` | `PyObject_GC_UnTrack` | gc |
| 0.66% | `python` | `list_subscript` | list |
| 0.64% | `python` | `PyFunction_NewWithQualName` | memory |
| 0.63% | `python` | `_PyObject_LookupSpecial` | dynamic |
| 0.61% | `python` | `visit_decref` | gc |
| 0.59% | `python` | `slice_dealloc` | memory |
| 0.59% | `python` | `set_table_resize` | miscobj |
| 0.59% | `python` | `_PyFrame_ClearExceptCode` | interpreter |
| 0.56% | `python` | `PyLong_FromLong` | int |
| 0.54% | `python` | `gen_dealloc` | memory |
| 0.52% | `python` | `visit_reachable` | gc |
| 0.51% | `python` | `PyIter_Next` | dynamic |

## pathlib

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 14.02% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 4.94% | `python` | `_PyObject_Malloc` | memory |
| 4.66% | `python` | `_PyObject_Free` | memory |
| 1.84% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 1.55% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.43% | `[kernel.kallsyms]` | `__d_lookup_rcu` | kernel |
| 1.39% | `python` | `initialize_locals` | interpreter |
| 1.25% | `libpthread-2.31.so` | `__pthread_mutex_lock` | library |
| 1.22% | `libpthread-2.31.so` | `pthread_mutex_unlock` | library |
| 1.13% | `[kernel.kallsyms]` | `ext4_htree_store_dirent` | kernel |
| 1.12% | `python` | `_PyFrame_ClearExceptCode` | interpreter |
| 1.07% | `[kernel.kallsyms]` | `__ext4fs_dirhash` | kernel |
| 1.03% | `[kernel.kallsyms]` | `memset_erms` | kernel |
| 1.00% | `python` | `gc_collect_region.isra.0` | gc |
| 1.00% | `python` | `_Py_dict_lookup` | lookup |
| 0.96% | `python` | `_PyType_Lookup` | lookup |
| 0.89% | `python` | `_PyEvalFramePushAndInit` | interpreter |
| 0.75% | `python` | `PyDict_GetItemRef` | dict |
| 0.75% | `[kernel.kallsyms]` | `filldir64` | kernel |
| 0.74% | `python` | `tupledealloc` | memory |
| 0.73% | `python` | `k_mul` | int |
| 0.71% | `libc-2.31.so` | `pthread_attr_setschedparam` | libc |
| 0.70% | `python` | `take_gil` | gil |
| 0.68% | `python` | `_Py_NewReference` | memory |
| 0.58% | `[kernel.kallsyms]` | `link_path_walk.part.0` | kernel |
| 0.58% | `[kernel.kallsyms]` | `strncpy_from_user` | kernel |
| 0.58% | `python` | `_Py_Dealloc` | memory |
| 0.58% | `[kernel.kallsyms]` | `kmem_cache_alloc` | kernel |
| 0.56% | `python` | `subtype_dealloc` | memory |
| 0.52% | `[kernel.kallsyms]` | `copy_user_enhanced_fast_string` | kernel |
| 0.51% | `python` | `sre_ucs1_match` | library |
| 0.51% | `python` | `visit_decref` | gc |

## pickle

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 23.53% | `_pickle.cpython-313-x86_64-linux-gnu.so` | `save` | library |
| 8.83% | `_pickle.cpython-313-x86_64-linux-gnu.so` | `_Pickler_Write` | library |
| 7.59% | `_pickle.cpython-313-x86_64-linux-gnu.so` | `PyMemoTable_Set` | library |
| 4.52% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 3.95% | `_pickle.cpython-313-x86_64-linux-gnu.so` | `Pickler_clear` | library |
| 3.78% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 3.73% | `_pickle.cpython-313-x86_64-linux-gnu.so` | `memo_put.isra.0` | library |
| 3.28% | `python` | `PyDict_Next` | dict |
| 2.63% | `python` | `PyUnicode_AsUTF8AndSize` | str |
| 2.26% | `_pickle.cpython-313-x86_64-linux-gnu.so` | `_Pickler_Write.constprop.3` | library |
| 2.03% | `python` | `_PyObject_Malloc` | memory |
| 1.70% | `python` | `_PyObject_Free` | memory |
| 1.61% | `_pickle.cpython-313-x86_64-linux-gnu.so` | `memo_get.isra.0` | library |
| 1.51% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 1.50% | `libc-2.31.so` | `pthread_attr_setschedparam` | libc |
| 1.06% | `python` | `gc_collect_region.isra.0` | gc |
| 0.75% | `python` | `_PyType_Lookup` | lookup |
| 0.74% | `python` | `_Py_dict_lookup` | lookup |
| 0.52% | `python` | `PyLong_AsLongAndOverflow` | int |
| 0.50% | `python` | `visit_decref` | gc |

## pickle_dict

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 41.29% | `_pickle.cpython-313-x86_64-linux-gnu.so` | `save` | library |
| 14.16% | `python` | `PyDict_Next` | dict |
| 7.68% | `_pickle.cpython-313-x86_64-linux-gnu.so` | `_Pickler_Write` | library |
| 6.07% | `_pickle.cpython-313-x86_64-linux-gnu.so` | `_Pickler_Write.constprop.3` | library |
| 3.61% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 3.20% | `python` | `PyLong_AsLongAndOverflow` | int |
| 2.17% | `_pickle.cpython-313-x86_64-linux-gnu.so` | `PyMemoTable_Set` | library |
| 1.26% | `_pickle.cpython-313-x86_64-linux-gnu.so` | `Pickler_clear` | library |
| 0.95% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 0.91% | `_pickle.cpython-313-x86_64-linux-gnu.so` | `0x0000000000005e64` | library |
| 0.89% | `_pickle.cpython-313-x86_64-linux-gnu.so` | `memo_put.isra.0` | library |
| 0.80% | `python` | `gc_collect_region.isra.0` | gc |
| 0.78% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 0.73% | `python` | `_PyObject_Malloc` | memory |
| 0.71% | `_pickle.cpython-313-x86_64-linux-gnu.so` | `0x0000000000005ce4` | library |
| 0.55% | `python` | `_PyObject_Free` | memory |

## pickle_list

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 38.74% | `_pickle.cpython-313-x86_64-linux-gnu.so` | `save` | library |
| 9.14% | `_pickle.cpython-313-x86_64-linux-gnu.so` | `_Pickler_Write` | library |
| 5.05% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 4.45% | `python` | `PyLong_AsLongAndOverflow` | int |
| 3.70% | `_pickle.cpython-313-x86_64-linux-gnu.so` | `_Pickler_Write.constprop.3` | library |
| 3.58% | `_pickle.cpython-313-x86_64-linux-gnu.so` | `PyMemoTable_Set` | library |
| 1.96% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.87% | `_pickle.cpython-313-x86_64-linux-gnu.so` | `Pickler_clear` | library |
| 1.67% | `python` | `_PyObject_Malloc` | memory |
| 1.45% | `_pickle.cpython-313-x86_64-linux-gnu.so` | `memo_put.isra.0` | library |
| 1.45% | `libc-2.31.so` | `pthread_attr_setschedparam` | libc |
| 1.20% | `python` | `gc_collect_region.isra.0` | gc |
| 1.20% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 1.07% | `python` | `_PyObject_Free` | memory |
| 0.89% | `_pickle.cpython-313-x86_64-linux-gnu.so` | `0x0000000000005ce4` | library |
| 0.58% | `python` | `visit_decref` | gc |
| 0.53% | `python` | `_Py_dict_lookup` | lookup |
| 0.53% | `python` | `_PyThreadState_GetCurrent` | unknown |

## pickle_pure_python

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 41.52% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 4.19% | `python` | `_PyObject_Malloc` | memory |
| 3.82% | `python` | `_PyObject_Free` | memory |
| 3.55% | `python` | `_Py_dict_lookup` | lookup |
| 2.37% | `python` | `_PyFrame_ClearExceptCode` | interpreter |
| 1.84% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.79% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 1.13% | `python` | `gc_collect_region.isra.0` | gc |
| 1.12% | `python` | `initialize_locals` | interpreter |
| 1.02% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 0.80% | `python` | `tupledealloc` | memory |
| 0.70% | `python` | `PyBuffer_FillInfo` | miscobj |
| 0.68% | `python` | `PyLong_FromVoidPtr` | int |
| 0.64% | `python` | `visit_decref` | gc |
| 0.63% | `python` | `PyBuffer_Release` | miscobj |
| 0.62% | `python` | `PyDict_GetItemRef` | dict |
| 0.61% | `python` | `_PyType_Lookup` | lookup |
| 0.59% | `python` | `PyLong_FromSsize_t` | int |
| 0.58% | `python` | `bytes_concat` | str |
| 0.57% | `python` | `insertdict` | dict |
| 0.57% | `python` | `_PyEvalFramePushAndInit` | interpreter |
| 0.52% | `python` | `PyNumber_Add` | dynamic |
| 0.51% | `libc-2.31.so` | `pthread_attr_setschedparam` | libc |

## pidigits

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 32.56% | `python` | `x_divrem` | int |
| 22.01% | `python` | `k_mul` | int |
| 11.77% | `python` | `x_add` | int |
| 7.39% | `python` | `x_sub` | int |
| 4.91% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 2.33% | `libc-2.31.so` | `pthread_attr_setschedparam` | libc |
| 1.75% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.01% | `python` | `_PyObject_Malloc` | memory |
| 0.98% | `python` | `_PyObject_Free` | memory |
| 0.78% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 0.78% | `python` | `gc_collect_region.isra.0` | gc |

## pprint

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 41.58% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 5.49% | `python` | `_PyObject_Malloc` | memory |
| 3.97% | `python` | `_PyObject_Free` | memory |
| 3.48% | `python` | `_PyFrame_ClearExceptCode` | interpreter |
| 2.44% | `python` | `_PyType_Lookup` | lookup |
| 1.90% | `python` | `tupledealloc` | memory |
| 1.81% | `python` | `_Py_type_getattro_impl` | dynamic |
| 1.67% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.33% | `python` | `_Py_dict_lookup` | lookup |
| 1.31% | `python` | `_Py_type_getattro` | lookup |
| 1.30% | `python` | `long_to_decimal_string_internal` | int |
| 1.29% | `python` | `_PyUnicode_JoinArray.part.0` | str |
| 1.01% | `python` | `_PyTuple_FromArraySteal` | tuple |
| 1.00% | `python` | `PyUnicode_Format` | str |
| 0.94% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 0.90% | `python` | `tuple_alloc` | memory |
| 0.80% | `python` | `set_lookkey` | miscobj |
| 0.79% | `python` | `PyObject_GC_UnTrack` | gc |
| 0.69% | `python` | `resize_compact` | str |
| 0.62% | `python` | `_copy_characters.part.0.constprop.0` | str |
| 0.62% | `python` | `initialize_locals` | interpreter |
| 0.61% | `python` | `_Py_NewReference` | memory |
| 0.52% | `python` | `_PyObject_Realloc` | memory |
| 0.52% | `python` | `_PyUnicodeWriter_WriteSubstring.part.0` | str |
| 0.51% | `python` | `_PyEvalFramePushAndInit` | interpreter |

## pycparser

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 34.34% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 12.18% | `python` | `sre_ucs1_match` | library |
| 3.86% | `python` | `gc_collect_region.isra.0` | gc |
| 2.79% | `python` | `_PyObject_Malloc` | memory |
| 2.33% | `python` | `_Py_dict_lookup` | lookup |
| 2.28% | `python` | `_PyObject_Free` | memory |
| 2.26% | `libc-2.31.so` | `pthread_attr_setschedparam` | libc |
| 1.63% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 1.28% | `python` | `PySlice_AdjustIndices` | miscobj |
| 1.11% | `python` | `PyDict_GetItemRef` | dict |
| 1.09% | `python` | `_PyFrame_ClearExceptCode` | interpreter |
| 1.05% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 0.98% | `python` | `visit_decref` | gc |
| 0.96% | `python` | `_sre_SRE_Pattern_match` | library |
| 0.94% | `python` | `initialize_locals` | interpreter |
| 0.90% | `python` | `_PyType_Lookup` | lookup |
| 0.88% | `python` | `subtype_traverse` | gc |
| 0.86% | `python` | `list_ass_slice_lock_held` | list |
| 0.84% | `python` | `pattern_new_match.isra.0.part.0` | memory |
| 0.82% | `python` | `visit_add_to_container` | gc |
| 0.74% | `python` | `sre_ucs1_count` | library |
| 0.71% | `python` | `subtype_dealloc` | memory |
| 0.58% | `python` | `_PyObject_GenericGetAttrWithDict` | dynamic |
| 0.57% | `python` | `PyType_GenericAlloc` | memory |
| 0.55% | `python` | `visit_reachable` | gc |
| 0.54% | `python` | `_PyEvalFramePushAndInit` | interpreter |

## pyflate

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 46.02% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 4.13% | `python` | `_PyObject_Free` | memory |
| 3.79% | `python` | `list_dealloc` | memory |
| 3.65% | `python` | `list_ass_slice_lock_held` | list |
| 3.31% | `python` | `_PyObject_Malloc` | memory |
| 2.61% | `libc-2.31.so` | `pthread_attr_setschedparam` | libc |
| 2.13% | `python` | `PyNumber_AsSsize_t` | dynamic |
| 1.79% | `python` | `list_concat` | list |
| 1.64% | `python` | `list_slice_lock_held.isra.0` | list |
| 1.31% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.30% | `python` | `_PyLong_Add` | int |
| 1.16% | `python` | `_PyFrame_ClearExceptCode` | interpreter |
| 1.10% | `python` | `_PyLong_Subtract` | int |
| 1.07% | `python` | `PyLong_AsSsize_t` | int |
| 1.06% | `python` | `PySlice_AdjustIndices` | miscobj |
| 0.85% | `python` | `stringlib_bytes_join` | str |
| 0.84% | `python` | `list_sort_impl` | list |
| 0.78% | `python` | `_Py_NewReference` | memory |
| 0.72% | `python` | `bytes_subscript` | str |
| 0.69% | `python` | `_PyBuildSlice_ConsumeRefs` | miscobj |
| 0.69% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 0.68% | `python` | `PyLong_FromSsize_t` | int |
| 0.67% | `python` | `long_lshift` | int |
| 0.61% | `python` | `unsafe_long_compare` | unknown |
| 0.55% | `python` | `PyObject_GetItem` | dynamic |
| 0.55% | `python` | `long_lshift1` | int |
| 0.51% | `python` | `slice_dealloc` | memory |

## pylint

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 25.66% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 12.45% | `python` | `gc_collect_region.isra.0` | gc |
| 3.40% | `python` | `visit_decref` | gc |
| 2.76% | `python` | `_PyObject_Malloc` | memory |
| 2.71% | `python` | `visit_reachable` | gc |
| 2.63% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 2.17% | `python` | `_PyObject_Free` | memory |
| 1.69% | `python` | `_PyType_Lookup` | lookup |
| 1.56% | `python` | `_PyFrame_ClearExceptCode` | interpreter |
| 1.51% | `python` | `visit_add_to_container` | gc |
| 1.50% | `python` | `_Py_dict_lookup` | lookup |
| 1.31% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.20% | `python` | `initialize_locals` | interpreter |
| 0.86% | `python` | `dict_traverse` | gc |
| 0.81% | `python` | `PyDict_GetItemRef` | dict |
| 0.77% | `python` | `PyObject_GenericGetAttr` | dynamic |
| 0.76% | `python` | `PyObject_VisitManagedDict` | dynamic |
| 0.71% | `python` | `tupledealloc` | memory |
| 0.61% | `python` | `list_traverse` | gc |
| 0.59% | `python` | `PyObject_GC_UnTrack` | gc |
| 0.59% | `python` | `dict_dealloc` | memory |
| 0.56% | `python` | `_PyObject_GetMethod` | dynamic |
| 0.54% | `python` | `PyType_IsSubtype` | dynamic |

## python_startup

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 7.59% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 5.38% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 4.16% | `python` | `gc_collect_region.isra.0` | gc |
| 3.30% | `python` | `_PyObject_Malloc` | memory |
| 3.10% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 2.69% | `python` | `visit_decref` | gc |
| 2.15% | `python` | `_Py_dict_lookup` | lookup |
| 1.93% | `python` | `visit_reachable` | gc |
| 1.82% | `ld-2.31.so` | `_dl_rtld_di_serinfo` | library |
| 1.78% | `python` | `_PyObject_Free` | memory |
| 1.65% | `python` | `r_object` | import |
| 1.39% | `python` | `find_name_in_mro` | lookup |
| 1.39% | `python` | `siphash13` | str |
| 1.31% | `python` | `update_one_slot` | lookup |
| 1.12% | `python` | `type_ready` | dynamic |
| 1.08% | `python` | `_Py_hashtable_get_entry_generic` | unknown |
| 0.98% | `libc-2.31.so` | `pthread_attr_setschedparam` | libc |
| 0.96% | `python` | `_PyCode_Quicken` | interpreter |
| 0.88% | `python` | `tupledealloc` | memory |
| 0.82% | `python` | `dict_traverse` | gc |
| 0.82% | `python` | `ascii_decode` | str |
| 0.81% | `python` | `_PyType_Lookup` | lookup |
| 0.81% | `[kernel.kallsyms]` | `filemap_map_pages` | kernel |
| 0.78% | `python` | `_PyUnicode_FromUCS1.part.0` | str |
| 0.73% | `python` | `_PyDict_GetItem_KnownHash` | dict |
| 0.69% | `[kernel.kallsyms]` | `native_irq_return_iret` | kernel |
| 0.68% | `python` | `_PyUnicode_InternInPlace` | str |
| 0.67% | `python` | `insertdict` | dict |
| 0.62% | `python` | `build_indices_unicode` | dict |
| 0.60% | `python` | `intern_string_constants` | interpreter |
| 0.59% | `libc-2.31.so` | `wcsrtombs` | libc |
| 0.56% | `libc-2.31.so` | `__gconv_get_alias_db` | libc |
| 0.54% | `[kernel.kallsyms]` | `sync_regs` | kernel |

## python_startup_no_site

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 7.68% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 5.06% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 4.28% | `python` | `gc_collect_region.isra.0` | gc |
| 3.22% | `python` | `_PyObject_Malloc` | memory |
| 3.07% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 2.91% | `ld-2.31.so` | `_dl_rtld_di_serinfo` | library |
| 2.50% | `python` | `visit_decref` | gc |
| 1.98% | `python` | `_Py_dict_lookup` | lookup |
| 1.86% | `python` | `visit_reachable` | gc |
| 1.69% | `python` | `_PyObject_Free` | memory |
| 1.49% | `python` | `siphash13` | str |
| 1.41% | `python` | `type_ready` | dynamic |
| 1.17% | `python` | `find_name_in_mro` | lookup |
| 1.15% | `python` | `r_object` | import |
| 1.12% | `python` | `_Py_hashtable_get_entry_generic` | unknown |
| 1.11% | `python` | `update_one_slot` | lookup |
| 1.03% | `python` | `ascii_decode` | str |
| 0.93% | `libc-2.31.so` | `pthread_attr_setschedparam` | libc |
| 0.90% | `libc-2.31.so` | `wcsrtombs` | libc |
| 0.86% | `[kernel.kallsyms]` | `native_irq_return_iret` | kernel |
| 0.85% | `libc-2.31.so` | `__gconv_get_alias_db` | libc |
| 0.83% | `python` | `dict_traverse` | gc |
| 0.81% | `[kernel.kallsyms]` | `filemap_map_pages` | kernel |
| 0.78% | `python` | `_PyType_Lookup` | lookup |
| 0.76% | `python` | `tupledealloc` | memory |
| 0.75% | `python` | `_PyCode_Quicken` | interpreter |
| 0.68% | `python` | `_PyUnicode_InternInPlace` | str |
| 0.67% | `python` | `insertdict` | dict |
| 0.64% | `[kernel.kallsyms]` | `sync_regs` | kernel |
| 0.59% | `python` | `build_indices_unicode` | dict |
| 0.58% | `python` | `_PyUnicode_FromUCS1.part.0` | str |
| 0.57% | `python` | `_PyDict_GetItem_KnownHash` | dict |
| 0.54% | `python` | `dict_setdefault_ref_lock_held` | dict |
| 0.54% | `[kernel.kallsyms]` | `copy_page` | kernel |
| 0.53% | `ld-2.31.so` | `_dl_catch_error` | library |
| 0.53% | `[kernel.kallsyms]` | `clear_page_erms` | kernel |

## raytrace

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 53.68% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 4.05% | `python` | `_PyFrame_ClearExceptCode` | interpreter |
| 2.14% | `python` | `_PyObject_Free` | memory |
| 2.00% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 1.68% | `python` | `_PyObject_Malloc` | memory |
| 1.50% | `python` | `PyFloat_FromDouble` | float |
| 1.50% | `python` | `float_dealloc` | memory |
| 1.42% | `python` | `subtype_dealloc` | memory |
| 1.30% | `python` | `_PyType_NewManagedObject` | memory |
| 1.12% | `python` | `PyType_IsSubtype` | dynamic |
| 1.08% | `python` | `PyObject_ClearManagedDict` | dynamic |
| 1.04% | `python` | `_PyThreadState_PopFrame` | interpreter |
| 0.90% | `python` | `_Py_NewReference` | memory |
| 0.84% | `python` | `initialize_locals` | interpreter |
| 0.83% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 0.83% | `python` | `float_sub` | float |
| 0.78% | `python` | `PyObject_ClearWeakRefs` | dynamic |
| 0.73% | `python` | `PyNumber_Subtract` | dynamic |
| 0.63% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 0.62% | `python` | `_PyType_Lookup` | lookup |
| 0.61% | `python` | `PyObject_GC_Del` | gc |
| 0.60% | `python` | `PyLong_AsDouble` | int |
| 0.58% | `python` | `gc_collect_region.isra.0` | gc |
| 0.54% | `python` | `_PyEvalFramePushAndInit` | interpreter |
| 0.54% | `python` | `PyObject_GC_UnTrack` | gc |

## regex_compile

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 42.59% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 3.59% | `python` | `sre_ucs1_match` | library |
| 3.51% | `python` | `_PyObject_Malloc` | memory |
| 3.22% | `python` | `_PyObject_Free` | memory |
| 2.11% | `python` | `_PyFrame_ClearExceptCode` | interpreter |
| 1.32% | `python` | `PyNumber_AsSsize_t` | dynamic |
| 1.24% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.14% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 1.07% | `python` | `_PyType_Lookup` | lookup |
| 0.95% | `python` | `gc_collect_region.isra.0` | gc |
| 0.80% | `python` | `bytearray_ass_subscript` | miscobj |
| 0.80% | `python` | `tupledealloc` | memory |
| 0.72% | `python` | `sre_ucs2_charset.isra.0` | library |
| 0.70% | `python` | `PyLong_FromLong` | int |
| 0.62% | `python` | `_Py_dict_lookup` | lookup |
| 0.62% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 0.57% | `python` | `list_dealloc` | memory |
| 0.55% | `python` | `initialize_locals` | interpreter |
| 0.53% | `python` | `tuple_alloc` | memory |
| 0.53% | `python` | `_PyObject_GenericGetAttrWithDict` | dynamic |
| 0.51% | `python` | `sre_search` | library |

## regex_dna

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 33.10% | `python` | `sre_ucs1_match` | library |
| 23.77% | `python` | `sre_ucs2_charset.isra.0` | library |
| 8.52% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 7.55% | `python` | `sre_search` | library |
| 2.96% | `libm-2.31.so` | `__fmod_finite` | library |
| 1.41% | `_bisect.cpython-313-x86_64-linux-gnu.so` | `_bisect_bisect_right` | library |
| 1.21% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.00% | `python` | `pattern_subx` | library |
| 0.82% | `python` | `_PyObject_Malloc` | memory |
| 0.77% | `python` | `float_rem` | float |
| 0.70% | `python` | `gc_collect_region.isra.0` | gc |
| 0.67% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 0.65% | `python` | `float_richcompare` | float |
| 0.52% | `python` | `_PyObject_Free` | memory |
| 0.51% | `python` | `float_dealloc` | memory |

## regex_effbot

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 37.95% | `python` | `sre_ucs1_match` | library |
| 12.94% | `python` | `sre_ucs2_charset.isra.0` | library |
| 7.03% | `python` | `_PyObject_Free` | memory |
| 6.19% | `python` | `sre_search` | library |
| 5.27% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 5.05% | `python` | `_PyObject_Malloc` | memory |
| 2.16% | `python` | `sre_ucs1_count` | library |
| 1.08% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 1.07% | `python` | `gc_collect_region.isra.0` | gc |
| 0.82% | `python` | `PyMem_Malloc` | memory |
| 0.64% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 0.59% | `python` | `visit_decref` | gc |

## regex_v8

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 31.48% | `python` | `sre_ucs1_match` | library |
| 9.97% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 3.86% | `python` | `PyCode_Addr2Line` | exceptions |
| 3.60% | `python` | `sre_search` | library |
| 3.58% | `python` | `sre_ucs1_count` | library |
| 2.97% | `python` | `_PyObject_Malloc` | memory |
| 2.67% | `python` | `_PyObject_Free` | memory |
| 2.06% | `libc-2.31.so` | `pthread_attr_setschedparam` | libc |
| 1.61% | `python` | `pattern_subx` | library |
| 1.34% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 1.30% | `python` | `gc_collect_region.isra.0` | gc |
| 1.29% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.01% | `python` | `pattern_new_match.isra.0.part.0` | memory |
| 0.94% | `python` | `_Py_dict_lookup` | lookup |
| 0.92% | `python` | `_sre_SRE_Pattern_search` | library |
| 0.63% | `python` | `visit_decref` | gc |
| 0.53% | `python` | `_PyFrame_ClearExceptCode` | interpreter |

## richards

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 53.64% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 3.83% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 3.14% | `python` | `_PyType_Lookup` | lookup |
| 2.81% | `python` | `_PyFrame_ClearExceptCode` | interpreter |
| 2.29% | `python` | `PyObject_GenericGetAttr` | dynamic |
| 1.88% | `python` | `_PyObject_TryGetInstanceAttribute` | dynamic |
| 1.82% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 1.75% | `python` | `_PyObject_GetMethod` | dynamic |
| 1.43% | `python` | `_PyObject_Malloc` | memory |
| 1.34% | `python` | `_PyObject_Free` | memory |
| 1.22% | `python` | `gc_collect_region.isra.0` | gc |
| 0.99% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 0.90% | `python` | `PyObject_GetAttr` | dynamic |
| 0.65% | `python` | `_PyThreadState_PopFrame` | interpreter |
| 0.60% | `python` | `visit_decref` | gc |
| 0.53% | `python` | `initialize_locals` | interpreter |
| 0.52% | `python` | `_Py_dict_lookup` | lookup |

## richards_super

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 53.63% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 4.01% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 3.12% | `python` | `_PyType_Lookup` | lookup |
| 2.94% | `python` | `_PyFrame_ClearExceptCode` | interpreter |
| 2.04% | `python` | `PyObject_GenericGetAttr` | dynamic |
| 1.77% | `python` | `_PyObject_TryGetInstanceAttribute` | dynamic |
| 1.69% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 1.63% | `python` | `_PyObject_GetMethod` | dynamic |
| 1.43% | `python` | `_PyObject_Malloc` | memory |
| 1.22% | `python` | `_PyObject_Free` | memory |
| 1.13% | `python` | `gc_collect_region.isra.0` | gc |
| 0.86% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 0.78% | `python` | `PyObject_GetAttr` | dynamic |
| 0.77% | `python` | `_Py_dict_lookup` | lookup |
| 0.72% | `python` | `_PyThreadState_PopFrame` | interpreter |
| 0.60% | `python` | `store_instance_attr_lock_held` | unknown |
| 0.59% | `python` | `PyDict_GetItemRef` | dict |
| 0.59% | `python` | `visit_decref` | gc |
| 0.59% | `python` | `_PyObject_GenericSetAttrWithDict` | dynamic |
| 0.54% | `python` | `initialize_locals` | interpreter |
| 0.53% | `python` | `do_super_lookup` | dynamic |

## scimark

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 45.30% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 5.10% | `python` | `PyNumber_AsSsize_t` | dynamic |
| 4.12% | `python` | `_PyObject_Free` | memory |
| 3.30% | `python` | `_PyObject_Malloc` | memory |
| 3.30% | `array.cpython-313-x86_64-linux-gnu.so` | `array_subscr` | library |
| 2.53% | `python` | `PyFloat_FromDouble` | float |
| 2.09% | `python` | `vgetargs1_impl` | calls |
| 1.79% | `python` | `PyObject_GetItem` | dynamic |
| 1.73% | `python` | `_PyLong_Add` | int |
| 1.54% | `python` | `PyLong_AsSsize_t` | int |
| 1.35% | `python` | `convertitem.constprop.0` | unknown |
| 1.20% | `array.cpython-313-x86_64-linux-gnu.so` | `array_ass_subscr` | library |
| 1.19% | `python` | `_Py_NewReference` | memory |
| 1.12% | `python` | `float_dealloc` | memory |
| 1.07% | `python` | `PyLong_FromLong` | int |
| 1.00% | `python` | `_PyFrame_ClearExceptCode` | interpreter |
| 0.97% | `python` | `PyType_GetModuleByDef` | dynamic |
| 0.70% | `python` | `long_dealloc` | memory |
| 0.69% | `python` | `_PyLong_Multiply` | int |
| 0.68% | `python` | `_PyFloat_ExactDealloc` | memory |
| 0.67% | `python` | `PyIndex_Check` | unknown |
| 0.66% | `array.cpython-313-x86_64-linux-gnu.so` | `d_setitem` | library |
| 0.64% | `python` | `PyArg_Parse` | calls |
| 0.55% | `python` | `_PyObject_GenericGetAttrWithDict` | dynamic |

## spectral_norm

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 40.30% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 6.92% | `python` | `_PyLong_Add` | int |
| 6.65% | `python` | `_PyObject_Free` | memory |
| 6.12% | `python` | `_PyObject_Malloc` | memory |
| 1.97% | `python` | `_PyLong_Multiply` | int |
| 1.73% | `python` | `float_div` | float |
| 1.55% | `python` | `_PyFrame_ClearExceptCode` | interpreter |
| 1.40% | `python` | `long_div` | int |
| 1.38% | `python` | `enum_next` | miscobj |
| 1.36% | `python` | `PyType_IsSubtype` | dynamic |
| 1.22% | `python` | `PyLong_FromLong` | int |
| 1.18% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 1.17% | `python` | `_Py_NewReference` | memory |
| 1.15% | `python` | `gc_collect_region.isra.0` | gc |
| 0.86% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 0.78% | `python` | `PyNumber_TrueDivide` | dynamic |
| 0.78% | `python` | `PyNumber_FloorDivide` | dynamic |
| 0.71% | `python` | `long_dealloc` | memory |
| 0.71% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 0.68% | `python` | `listiter_next` | list |
| 0.66% | `python` | `PyLong_AsDouble` | int |
| 0.61% | `python` | `visit_decref` | gc |
| 0.56% | `python` | `PyLong_FromSsize_t` | int |
| 0.56% | `python` | `PyObject_Malloc` | dynamic |

## sqlglot

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 32.28% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 4.10% | `python` | `_PyObject_Malloc` | memory |
| 4.04% | `python` | `_PyObject_Free` | memory |
| 2.06% | `python` | `PyType_IsSubtype` | dynamic |
| 2.01% | `python` | `_PyType_Lookup` | lookup |
| 1.88% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 1.66% | `python` | `tupledealloc` | memory |
| 1.65% | `python` | `_PyFrame_ClearExceptCode` | interpreter |
| 1.62% | `python` | `_PyObject_GenericGetAttrWithDict` | dynamic |
| 1.43% | `python` | `gc_collect_region.isra.0` | gc |
| 1.16% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.12% | `python` | `_Py_dict_lookup` | lookup |
| 0.98% | `python` | `_PyObject_GC_New` | gc |
| 0.95% | `python` | `PyObject_GC_Del` | gc |
| 0.90% | `python` | `_PyObject_LookupSpecial` | dynamic |
| 0.88% | `python` | `dictiter_iternextitem` | dict |
| 0.85% | `python` | `PyObject_GC_UnTrack` | gc |
| 0.80% | `python` | `PyObject_IsInstance` | dynamic |
| 0.76% | `python` | `object_isinstance` | dynamic |
| 0.76% | `python` | `initialize_locals` | interpreter |
| 0.74% | `python` | `tuple_alloc` | memory |
| 0.74% | `python` | `_PyTuple_FromArraySteal` | tuple |
| 0.73% | `python` | `visit_decref` | gc |
| 0.70% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 0.65% | `python` | `PyObject_GetOptionalAttr` | dynamic |
| 0.65% | `python` | `insert_to_emptydict` | dict |
| 0.56% | `python` | `_Py_NewReference` | memory |
| 0.53% | `python` | `PyObject_GenericGetAttr` | dynamic |
| 0.51% | `python` | `visit_reachable` | gc |
| 0.50% | `python` | `_PyObject_GC_Link` | gc |

## sqlglot_optimize

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 31.32% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 3.92% | `python` | `_PyObject_Malloc` | memory |
| 3.89% | `python` | `_PyObject_Free` | memory |
| 2.34% | `python` | `_PyType_Lookup` | lookup |
| 2.11% | `python` | `PyType_IsSubtype` | dynamic |
| 1.91% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 1.84% | `python` | `_PyObject_GenericGetAttrWithDict` | dynamic |
| 1.59% | `python` | `gc_collect_region.isra.0` | gc |
| 1.58% | `python` | `_PyFrame_ClearExceptCode` | interpreter |
| 1.49% | `python` | `tupledealloc` | memory |
| 1.20% | `python` | `_Py_dict_lookup` | lookup |
| 1.12% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.07% | `python` | `dictiter_iternextitem` | dict |
| 1.07% | `python` | `_PyObject_LookupSpecial` | dynamic |
| 1.05% | `python` | `_PyObject_GC_New` | gc |
| 0.98% | `python` | `PyObject_GC_Del` | gc |
| 0.91% | `python` | `PyObject_GC_UnTrack` | gc |
| 0.83% | `python` | `object_isinstance` | dynamic |
| 0.83% | `python` | `PyObject_IsInstance` | dynamic |
| 0.81% | `python` | `visit_decref` | gc |
| 0.75% | `python` | `PyObject_GenericGetAttr` | dynamic |
| 0.74% | `python` | `tuple_alloc` | memory |
| 0.69% | `python` | `PyObject_GetOptionalAttr` | dynamic |
| 0.69% | `python` | `_PyTuple_FromArraySteal` | tuple |
| 0.60% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 0.60% | `python` | `initialize_locals` | interpreter |
| 0.59% | `python` | `PyCMethod_New` | memory |
| 0.59% | `python` | `_Py_NewReference` | memory |
| 0.53% | `python` | `getset_get` | dynamic |
| 0.52% | `python` | `visit_reachable` | gc |
| 0.51% | `python` | `_PyObject_RealIsInstance` | dynamic |
| 0.51% | `python` | `_PyObject_GC_Link` | gc |
| 0.50% | `python` | `insert_to_emptydict` | dict |
| 0.50% | `python` | `siphash13` | str |

## sqlglot_parse

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 46.25% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 2.89% | `python` | `_PyObject_Malloc` | memory |
| 2.68% | `python` | `_PyObject_Free` | memory |
| 2.26% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 2.23% | `python` | `gc_collect_region.isra.0` | gc |
| 2.20% | `python` | `_PyFrame_ClearExceptCode` | interpreter |
| 2.06% | `python` | `_PyType_Lookup` | lookup |
| 1.56% | `python` | `_Py_dict_lookup` | lookup |
| 1.14% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 0.92% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 0.88% | `python` | `initialize_locals` | interpreter |
| 0.86% | `python` | `visit_decref` | gc |
| 0.78% | `python` | `_Py_type_getattro` | lookup |
| 0.60% | `python` | `PyObject_RichCompare` | dynamic |
| 0.60% | `python` | `_PyLong_Add` | int |
| 0.56% | `python` | `tupledealloc` | memory |
| 0.56% | `python` | `PyType_IsSubtype` | dynamic |
| 0.50% | `python` | `visit_reachable` | gc |

## sqlglot_transpile

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 40.84% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 2.97% | `python` | `_PyObject_Malloc` | memory |
| 2.83% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 2.67% | `python` | `_PyObject_Free` | memory |
| 2.27% | `python` | `gc_collect_region.isra.0` | gc |
| 2.20% | `python` | `_PyFrame_ClearExceptCode` | interpreter |
| 1.98% | `python` | `_PyType_Lookup` | lookup |
| 1.78% | `python` | `_Py_dict_lookup` | lookup |
| 1.29% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.02% | `python` | `visit_decref` | gc |
| 0.93% | `python` | `initialize_locals` | interpreter |
| 0.79% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 0.69% | `python` | `tupledealloc` | memory |
| 0.65% | `python` | `PyType_IsSubtype` | dynamic |
| 0.62% | `python` | `visit_reachable` | gc |
| 0.59% | `python` | `_Py_type_getattro` | lookup |
| 0.58% | `python` | `PyObject_GenericGetAttr` | dynamic |

## sqlite_synth

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 10.37% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 9.21% | `libpthread-2.31.so` | `pthread_mutex_unlock` | library |
| 8.70% | `libpthread-2.31.so` | `__pthread_mutex_lock` | library |
| 3.77% | `python` | `take_gil` | gil |
| 3.70% | `libsqlite3.so.0.8.6` | `sqlite3_reset` | library |
| 3.15% | `python` | `_PyObject_Malloc` | memory |
| 2.73% | `python` | `_PyObject_Free` | memory |
| 1.86% | `libm-2.31.so` | `f64xsubf128` | library |
| 1.37% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 1.34% | `python` | `gc_collect_region.isra.0` | gc |
| 1.32% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.23% | `libsqlite3.so.0.8.6` | `sqlite3_randomness` | library |
| 0.87% | `libpthread-2.31.so` | `pthread_cond_signal@@GLIBC_2.3.2` | library |
| 0.83% | `python` | `tupledealloc` | memory |
| 0.82% | `_sqlite3.cpython-313-x86_64-linux-gnu.so` | `_pysqlite_query_execute` | library |
| 0.81% | `libc-2.31.so` | `pthread_attr_setschedparam` | libc |
| 0.77% | `libsqlite3.so.0.8.6` | `sqlite3_value_double` | library |
| 0.73% | `python` | `drop_gil` | gil |
| 0.68% | `libsqlite3.so.0.8.6` | `sqlite3_preupdate_old` | library |
| 0.68% | `python` | `visit_decref` | gc |
| 0.67% | `libsqlite3.so.0.8.6` | `sqlite3_value_int64` | library |
| 0.58% | `python` | `long_to_decimal_string_internal` | int |
| 0.58% | `python` | `_PyThreadState_MustExit` | unknown |
| 0.58% | `python` | `_Py_dict_lookup` | lookup |
| 0.58% | `libsqlite3.so.0.8.6` | `sqlite3_extended_errcode` | library |
| 0.57% | `python` | `_Py_NewReference` | memory |
| 0.57% | `python` | `PyFloat_FromDouble` | float |

## sympy

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 27.49% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 3.57% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 3.22% | `python` | `_PyObject_Malloc` | memory |
| 2.57% | `python` | `_PyObject_Free` | memory |
| 2.43% | `python` | `_PyType_Lookup` | lookup |
| 2.07% | `python` | `_Py_dict_lookup` | lookup |
| 2.04% | `python` | `gc_collect_region.isra.0` | gc |
| 1.73% | `python` | `tupledealloc` | memory |
| 1.62% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.61% | `python` | `_PyFrame_ClearExceptCode` | interpreter |
| 1.38% | `python` | `initialize_locals` | interpreter |
| 1.13% | `python` | `PyObject_RichCompareBool` | dynamic |
| 1.08% | `python` | `visit_decref` | gc |
| 0.90% | `python` | `PyType_IsSubtype` | dynamic |
| 0.88% | `python` | `_PyObject_GenericGetAttrWithDict` | dynamic |
| 0.76% | `python` | `PyObject_GC_UnTrack` | gc |
| 0.74% | `python` | `visit_reachable` | gc |
| 0.68% | `python` | `PyDict_GetItemRef` | dict |
| 0.67% | `python` | `tuple_alloc` | memory |
| 0.65% | `python` | `insertdict` | dict |
| 0.65% | `python` | `dict_dealloc` | memory |
| 0.61% | `python` | `PyObject_GenericGetAttr` | dynamic |
| 0.60% | `python` | `_Py_type_getattro` | lookup |
| 0.57% | `python` | `_PyEvalFramePushAndInit` | interpreter |
| 0.56% | `python` | `_PyObject_GC_New` | gc |
| 0.54% | `python` | `PyObject_GC_Del` | gc |
| 0.52% | `python` | `PyObject_GetAttr` | dynamic |

## telco

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 16.34% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 6.71% | `python` | `_PyObject_Malloc` | memory |
| 5.54% | `python` | `_PyObject_Free` | memory |
| 2.25% | `python` | `PyType_GetModuleByDef` | dynamic |
| 1.96% | `python` | `PyObject_GC_Del` | gc |
| 1.95% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.86% | `_decimal.cpython-313-x86_64-linux-gnu.so` | `nm_mpd_qadd` | library |
| 1.67% | `python` | `_PyObject_GC_New` | gc |
| 1.64% | `python` | `PyContextVar_Get` | unknown |
| 1.58% | `_decimal.cpython-313-x86_64-linux-gnu.so` | `mpd_setdigits` | library |
| 1.44% | `_decimal.cpython-313-x86_64-linux-gnu.so` | `_mpd_qaddsub` | library |
| 1.38% | `python` | `tupledealloc` | memory |
| 1.33% | `_decimal.cpython-313-x86_64-linux-gnu.so` | `_mpd_qmul` | library |
| 1.27% | `_decimal.cpython-313-x86_64-linux-gnu.so` | `_mpd_check_exp` | library |
| 1.25% | `python` | `vgetargskeywords.constprop.0` | calls |
| 1.21% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 1.18% | `_decimal.cpython-313-x86_64-linux-gnu.so` | `nm_mpd_qmul` | library |
| 1.17% | `python` | `_PyArg_UnpackKeywordsWithVararg` | calls |
| 1.10% | `python` | `PyObject_GenericGetAttr` | dynamic |
| 1.08% | `python` | `_PyType_Lookup` | lookup |
| 1.00% | `python` | `gc_collect_region.isra.0` | gc |
| 0.99% | `_decimal.cpython-313-x86_64-linux-gnu.so` | `_mpd_baseshiftr` | library |
| 0.95% | `python` | `PyObject_GC_UnTrack` | gc |
| 0.89% | `python` | `convertitem.constprop.0` | unknown |
| 0.84% | `_decimal.cpython-313-x86_64-linux-gnu.so` | `mpd_qquantize` | library |
| 0.78% | `_decimal.cpython-313-x86_64-linux-gnu.so` | `dec_addstatus` | library |
| 0.73% | `_decimal.cpython-313-x86_64-linux-gnu.so` | `PyDecType_New` | library |
| 0.71% | `_decimal.cpython-313-x86_64-linux-gnu.so` | `dec_mpd_qquantize` | library |
| 0.67% | `python` | `_Py_NewReference` | memory |
| 0.66% | `python` | `vgetargs1_impl` | calls |
| 0.66% | `python` | `PyUnicode_AsUCS4` | str |
| 0.65% | `python` | `PyCMethod_New` | memory |
| 0.65% | `python` | `tuple_alloc` | memory |
| 0.63% | `python` | `_PyObject_GC_Link` | gc |
| 0.63% | `_decimal.cpython-313-x86_64-linux-gnu.so` | `dec_dealloc` | library |
| 0.55% | `_decimal.cpython-313-x86_64-linux-gnu.so` | `_mpd_baseadd` | library |
| 0.55% | `python` | `_Py_dict_lookup` | lookup |
| 0.53% | `_decimal.cpython-313-x86_64-linux-gnu.so` | `mpd_qfinalize.part.0` | library |
| 0.52% | `_decimal.cpython-313-x86_64-linux-gnu.so` | `mpd_qshiftr` | library |

## thrift

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 20.42% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 4.15% | `python` | `_PyObject_Malloc` | memory |
| 3.52% | `python` | `_PyObject_Free` | memory |
| 3.20% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 2.41% | `python` | `initialize_locals` | interpreter |
| 1.84% | `fastbinary.cpython-313-x86_64-linux-gnu.so` | `apache::thrift::py::ProtocolBase<apache::thrift::py::BinaryProtocol>::encodeValue` | library |
| 1.80% | `python` | `insert_to_emptydict` | dict |
| 1.75% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.66% | `python` | `_PyType_Lookup` | lookup |
| 1.59% | `python` | `_Py_dict_lookup` | lookup |
| 1.40% | `python` | `_PyFrame_ClearExceptCode` | interpreter |
| 1.27% | `python` | `insertdict` | dict |
| 1.22% | `python` | `dict_dealloc` | memory |
| 1.18% | `python` | `gc_collect_region.isra.0` | gc |
| 1.03% | `python` | `PyType_GenericAlloc` | memory |
| 1.02% | `python` | `subtype_dealloc` | memory |
| 1.00% | `python` | `PyDict_GetItemRef` | dict |
| 0.86% | `python` | `PyObject_RichCompareBool` | dynamic |
| 0.86% | `python` | `tupledealloc` | memory |
| 0.77% | `fastbinary.cpython-313-x86_64-linux-gnu.so` | `apache::thrift::py::ProtocolBase<apache::thrift::py::BinaryProtocol>::decodeValue` | library |
| 0.77% | `python` | `PyUnicode_FromFormatV` | str |
| 0.75% | `python` | `_PyObject_GenericGetAttrWithDict` | dynamic |
| 0.71% | `python` | `_PyEvalFramePushAndInit` | interpreter |
| 0.70% | `python` | `PyObject_GC_UnTrack` | gc |
| 0.68% | `python` | `_PyObject_Call_Prepend` | dynamic |
| 0.66% | `python` | `slot_tp_init` | unknown |
| 0.62% | `python` | `PyObject_IS_GC` | gc |
| 0.59% | `python` | `PyObject_GenericGetAttr` | dynamic |
| 0.59% | `python` | `visit_decref` | gc |
| 0.59% | `python` | `_Py_NewReference` | memory |
| 0.58% | `python` | `_PyObject_MakeTpCall` | dynamic |
| 0.57% | `fastbinary.cpython-313-x86_64-linux-gnu.so` | `apache::thrift::py::ProtocolBase<apache::thrift::py::BinaryProtocol>::readStruct` | library |
| 0.57% | `python` | `_PyStack_UnpackDict` | unknown |
| 0.55% | `python` | `PyObject_GetAttr` | dynamic |
| 0.54% | `python` | `_Py_Dealloc` | memory |
| 0.53% | `python` | `PyDict_SetItem` | dict |
| 0.53% | `fastbinary.cpython-313-x86_64-linux-gnu.so` | `apache::thrift::py::ProtocolBase<apache::thrift::py::BinaryProtocol>::readBytes` | library |
| 0.52% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 0.52% | `python` | `PyLong_AsLong` | int |
| 0.50% | `python` | `PyUnicode_RichCompare` | str |
| 0.50% | `python` | `PyObject_ClearManagedDict` | dynamic |

## tomli_loads

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 47.54% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 4.62% | `python` | `set_lookkey` | miscobj |
| 4.24% | `python` | `_PyObject_Free` | memory |
| 3.63% | `python` | `_PyObject_Malloc` | memory |
| 2.97% | `python` | `_PyLong_Add` | int |
| 2.58% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 2.56% | `python` | `_PyUnicode_Equal` | str |
| 2.12% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.83% | `python` | `_PySet_Contains` | unknown |
| 1.49% | `python` | `_Py_dict_lookup` | lookup |
| 1.41% | `python` | `_PyFrame_ClearExceptCode` | interpreter |
| 1.15% | `python` | `PyDict_GetItemRef` | dict |
| 0.76% | `python` | `tupledealloc` | memory |
| 0.74% | `python` | `long_dealloc` | memory |
| 0.74% | `python` | `replace` | str |
| 0.72% | `python` | `_PyIncrementalNewlineDecoder_decode` | memory |
| 0.64% | `python` | `_PyUnicode_FromUCS4.part.0` | str |
| 0.63% | `python` | `_Py_NewReference` | memory |
| 0.63% | `python` | `PyNumber_AsSsize_t` | dynamic |
| 0.58% | `python` | `tuple_alloc` | memory |
| 0.51% | `python` | `_PyTuple_FromArraySteal` | tuple |
| 0.50% | `python` | `sre_ucs4_match` | library |

## tornado_http

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 27.43% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 3.55% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 2.86% | `python` | `_PyObject_Malloc` | memory |
| 2.41% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 1.99% | `python` | `gc_collect_region.isra.0` | gc |
| 1.98% | `python` | `_PyObject_Free` | memory |
| 1.76% | `python` | `_PyFrame_ClearExceptCode` | interpreter |
| 1.23% | `python` | `_Py_dict_lookup` | lookup |
| 1.09% | `python` | `_PyType_Lookup` | lookup |
| 1.06% | `python` | `visit_decref` | gc |
| 0.99% | `python` | `tupledealloc` | memory |
| 0.88% | `python` | `initialize_locals` | interpreter |
| 0.79% | `libc-2.31.so` | `pthread_attr_setschedparam` | libc |
| 0.78% | `python` | `visit_reachable` | gc |
| 0.67% | `[kernel.kallsyms]` | `copy_user_enhanced_fast_string` | kernel |
| 0.57% | `python` | `PyObject_GC_UnTrack` | gc |
| 0.56% | `python` | `r_object` | import |

## typing_runtime_protocols

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 27.91% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 4.30% | `python` | `_PyObject_Malloc` | memory |
| 3.47% | `python` | `_PyObject_Free` | memory |
| 2.68% | `python` | `tupledealloc` | memory |
| 2.52% | `python` | `weakref___new__` | memory |
| 2.25% | `python` | `_Py_dict_lookup` | lookup |
| 2.14% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 1.84% | `python` | `_PyObject_MakeTpCall` | dynamic |
| 1.59% | `python` | `_PyTuple_FromArray.part.0` | tuple |
| 1.54% | `python` | `_PyType_Lookup` | lookup |
| 1.53% | `python` | `gc_collect_region.isra.0` | gc |
| 1.49% | `python` | `tuple_alloc` | memory |
| 1.47% | `python` | `PyArg_UnpackTuple` | calls |
| 1.21% | `python` | `PyObject_RichCompareBool` | dynamic |
| 1.19% | `python` | `_PyFrame_ClearExceptCode` | interpreter |
| 1.14% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 0.92% | `python` | `_Py_type_getattro` | lookup |
| 0.86% | `python` | `PyObject_GC_UnTrack` | gc |
| 0.79% | `python` | `_PyObject_GC_New` | gc |
| 0.78% | `python` | `PyObject_GC_Del` | gc |
| 0.74% | `python` | `PyObject_Vectorcall` | dynamic |
| 0.71% | `python` | `visit_decref` | gc |
| 0.67% | `python` | `_Py_NewReference` | memory |
| 0.66% | `python` | `bounded_lru_cache_wrapper` | unknown |
| 0.63% | `python` | `type_call` | dynamic |
| 0.53% | `python` | `_PyDict_GetItem_KnownHash` | dict |
| 0.50% | `python` | `set_lookkey` | miscobj |

## unpack_sequence

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 75.96% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 1.13% | `python` | `gc_collect_main` | gc |
| 1.04% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 0.91% | `python` | `_PyObject_Malloc` | memory |
| 0.69% | `python` | `_PyObject_Free` | memory |
| 0.64% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 0.61% | `python` | `visit_decref` | gc |

## unpickle

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 8.17% | `python` | `_PyObject_Malloc` | memory |
| 6.77% | `_pickle.cpython-313-x86_64-linux-gnu.so` | `load` | library |
| 6.01% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 5.81% | `python` | `_PyObject_Free` | memory |
| 4.49% | `python` | `siphash13` | str |
| 4.05% | `python` | `insertdict` | dict |
| 3.94% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 3.61% | `python` | `ascii_decode` | str |
| 3.11% | `python` | `unicode_decode_utf8` | str |
| 3.04% | `_pickle.cpython-313-x86_64-linux-gnu.so` | `load_counted_binunicode` | library |
| 2.39% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 2.16% | `python` | `PyUnicode_New.part.0` | memory |
| 2.15% | `python` | `_Py_dict_lookup` | lookup |
| 1.91% | `_pickle.cpython-313-x86_64-linux-gnu.so` | `do_setitems.isra.0` | library |
| 1.47% | `python` | `dict_ass_sub` | dict |
| 1.39% | `python` | `gc_collect_region.isra.0` | gc |
| 1.35% | `_pickle.cpython-313-x86_64-linux-gnu.so` | `_Unpickler_MemoPut` | library |
| 1.29% | `python` | `find_empty_slot` | dict |
| 1.18% | `python` | `dict_dealloc` | memory |
| 1.08% | `python` | `_PyObject_Realloc` | memory |
| 1.05% | `python` | `build_indices_unicode` | dict |
| 0.99% | `_pickle.cpython-313-x86_64-linux-gnu.so` | `Unpickler_clear` | library |
| 0.94% | `python` | `unicode_dealloc` | memory |
| 0.86% | `python` | `PyObject_SetItem` | dynamic |
| 0.71% | `python` | `PyObject_IS_GC` | gc |
| 0.70% | `python` | `_Py_NewReference` | memory |
| 0.65% | `python` | `visit_decref` | gc |
| 0.59% | `libc-2.31.so` | `pthread_attr_setschedparam` | libc |
| 0.57% | `_pickle.cpython-313-x86_64-linux-gnu.so` | `Pdata_push` | library |
| 0.54% | `python` | `visit_reachable` | gc |
| 0.51% | `python` | `_PyType_Lookup` | lookup |

## unpickle_list

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 14.71% | `_pickle.cpython-313-x86_64-linux-gnu.so` | `load` | library |
| 7.32% | `python` | `_PyObject_Free` | memory |
| 6.06% | `python` | `list_dealloc` | memory |
| 5.35% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 5.23% | `python` | `_PyObject_Malloc` | memory |
| 5.18% | `python` | `list_ass_slice_lock_held` | list |
| 4.95% | `_pickle.cpython-313-x86_64-linux-gnu.so` | `Pdata_push` | library |
| 4.48% | `python` | `PyList_New` | memory |
| 3.95% | `_pickle.cpython-313-x86_64-linux-gnu.so` | `do_append.isra.0` | library |
| 3.83% | `python` | `PyLong_FromLong` | int |
| 2.68% | `python` | `_PyObject_Calloc` | memory |
| 1.86% | `python` | `PyMem_Calloc` | memory |
| 1.67% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.57% | `python` | `_Py_NewReference` | memory |
| 1.39% | `python` | `PyObject_GC_UnTrack` | gc |
| 1.25% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 1.24% | `python` | `gc_collect_region.isra.0` | gc |
| 1.21% | `python` | `_PyObject_Realloc` | memory |
| 1.17% | `_pickle.cpython-313-x86_64-linux-gnu.so` | `marker.isra.0` | library |
| 0.70% | `_pickle.cpython-313-x86_64-linux-gnu.so` | `_Unpickler_MemoPut` | library |
| 0.67% | `python` | `visit_decref` | gc |

## unpickle_pure_python

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 50.20% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 2.57% | `python` | `_PyObject_Malloc` | memory |
| 2.10% | `python` | `_PyFrame_ClearExceptCode` | interpreter |
| 2.06% | `python` | `_Py_dict_lookup` | lookup |
| 1.94% | `python` | `_PyObject_Free` | memory |
| 1.82% | `python` | `PyObject_IsTrue` | dynamic |
| 1.78% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.32% | `python` | `PyNumber_AsSsize_t` | dynamic |
| 1.21% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 1.11% | `python` | `PyDict_GetItemRef` | dict |
| 1.10% | `python` | `insertdict` | dict |
| 0.97% | `python` | `_PyEval_FrameClearAndPop` | interpreter |
| 0.95% | `python` | `initialize_locals` | interpreter |
| 0.94% | `python` | `gc_collect_region.isra.0` | gc |
| 0.92% | `python` | `_io_BytesIO_read` | unknown |
| 0.74% | `python` | `_PyEvalFramePushAndInit` | interpreter |
| 0.65% | `python` | `PyObject_GetItem` | dynamic |
| 0.65% | `python` | `bytes_subscript` | str |
| 0.64% | `python` | `PyLong_AsSsize_t` | int |
| 0.64% | `python` | `PyUnicode_Decode.part.0` | str |
| 0.58% | `python` | `PyBytes_FromStringAndSize` | str |
| 0.53% | `python` | `unicode_vectorcall` | str |
| 0.53% | `python` | `siphash13` | str |
| 0.53% | `python` | `PyLong_FromSsize_t` | int |
| 0.51% | `python` | `PyObject_IsInstance` | dynamic |

## xml_etree

| percentage | object | symbol | category |
| ---: | :--- | :--- | :--- |
| 21.01% | `python` | `_PyEval_EvalFrameDefault` | interpreter |
| 4.46% | `python` | `_PyObject_Malloc` | memory |
| 3.12% | `python` | `_PyObject_Free` | memory |
| 2.50% | `python` | `gc_collect_region.isra.0` | gc |
| 2.34% | `pyexpat.cpython-313-x86_64-linux-gnu.so` | `normal_updatePosition` | library |
| 2.07% | `pyexpat.cpython-313-x86_64-linux-gnu.so` | `normal_contentTok` | library |
| 1.93% | `python` | `_PyType_Lookup` | lookup |
| 1.78% | `libc-2.31.so` | `__nss_database_lookup` | libc |
| 1.65% | `python` | `_io_TextIOWrapper_write` | unknown |
| 1.64% | `python` | `PyObject_GenericGetAttr` | dynamic |
| 1.64% | `python` | `_Py_dict_lookup` | lookup |
| 1.42% | `python` | `visit_decref` | gc |
| 1.38% | `python` | `unicodekeys_lookup_unicode` | lookup |
| 1.34% | `python` | `visit_reachable` | gc |
| 1.31% | `pyexpat.cpython-313-x86_64-linux-gnu.so` | `sip24_update` | library |
| 1.14% | `pyexpat.cpython-313-x86_64-linux-gnu.so` | `accountingDiffTolerated.part.0` | library |
| 1.11% | `pyexpat.cpython-313-x86_64-linux-gnu.so` | `normal_nameLength` | library |
| 1.03% | `pyexpat.cpython-313-x86_64-linux-gnu.so` | `doContent` | library |
| 1.00% | `python` | `initialize_locals` | interpreter |
| 0.96% | `pyexpat.cpython-313-x86_64-linux-gnu.so` | `lookup.constprop.0` | library |
| 0.96% | `_elementtree.cpython-313-x86_64-linux-gnu.so` | `expat_end_handler` | library |
| 0.90% | `_elementtree.cpython-313-x86_64-linux-gnu.so` | `treebuilder_handle_start` | library |
| 0.81% | `python` | `_PyFrame_ClearExceptCode` | interpreter |
| 0.75% | `python` | `PyUnicode_Contains` | str |
| 0.70% | `pyexpat.cpython-313-x86_64-linux-gnu.so` | `normal_getAtts` | library |
| 0.68% | `python` | `tupledealloc` | memory |
| 0.68% | `python` | `PyObject_GC_UnTrack` | gc |
| 0.63% | `python` | `siphash13` | str |
| 0.63% | `python` | `ascii_decode` | str |
| 0.62% | `python` | `_PyEvalFramePushAndInit` | interpreter |
| 0.60% | `python` | `_copy_characters.part.0.constprop.0` | str |
| 0.59% | `_elementtree.cpython-313-x86_64-linux-gnu.so` | `element_gc_traverse` | library |
| 0.58% | `python` | `PyUnicode_New.part.0` | memory |
| 0.58% | `pyexpat.cpython-313-x86_64-linux-gnu.so` | `sip24_final` | library |
| 0.55% | `python` | `PyObject_GetAttr` | dynamic |
| 0.53% | `python` | `_PyObject_GetMethod` | dynamic |
| 0.52% | `python` | `_PyObject_GenericGetAttrWithDict` | dynamic |
| 0.51% | `python` | `getset_get` | dynamic |


## Categories

### interpreter

32.48% total

| percentage | object | symbol |
| ---: | :--- | :--- |
| 28.48% | python | _PyEval_EvalFrameDefault |
| 1.30% | python | _PyFrame_ClearExceptCode |
| 0.65% | python | initialize_locals |
| 0.52% | python | _PyEval_FrameClearAndPop |
| 0.31% | python | _PyEvalFramePushAndInit |
| 0.24% | python | _PyThreadState_PopFrame |
| 0.19% | python | _PyCode_Quicken |
| 0.16% | python | _PyEval_Vector |
| 0.12% | python | intern_string_constants |
| 0.09% | python | _Py_GetBaseOpcode |
| 0.08% | python | _PyPegen_is_memoized |
| 0.06% | python | _PyFrame_Traverse |
| 0.06% | python | _PyEval_SliceIndex |
| 0.04% | python | _PyPegen_expect_token |
| 0.03% | python | _PyPegen_update_memo |
| 0.02% | python | _PyPegen_fill_token |
| 0.02% | python | _PyCode_Validate |
| 0.01% | python | _PyEval_BuiltinsFromGlobals |
| 0.01% | python | _PyPegen_insert_memo |
| 0.01% | python | _PyPegen_name_token |
| 0.01% | python | _PyFrame_New_NoTrack |
| 0.01% | python | PyEval_SaveThread |

### memory

12.33% total

| percentage | object | symbol |
| ---: | :--- | :--- |
| 3.30% | python | _PyObject_Malloc |
| 2.83% | python | _PyObject_Free |
| 0.65% | python | tupledealloc |
| 0.48% | python | _Py_NewReference |
| 0.44% | python | list_dealloc |
| 0.33% | python | dict_dealloc |
| 0.27% | python | tuple_alloc |
| 0.25% | python | subtype_dealloc |
| 0.23% | python | PyType_GenericAlloc |
| 0.22% | python | PyList_New |
| 0.21% | python | _Py_Dealloc |
| 0.20% | python | PyUnicode_New.part.0 |
| 0.20% | python | _PyObject_Realloc |
| 0.18% | python | gen_dealloc |
| 0.13% | python | unicode_dealloc |
| 0.13% | python | float_dealloc |
| 0.12% | python | _PyObject_Calloc |
| 0.12% | python | long_dealloc |
| 0.10% | python | PyTuple_New |
| 0.10% | python | PyFunction_NewWithQualName |
| 0.09% | python | slice_dealloc |
| 0.09% | python | code_dealloc |
| 0.09% | python | PyCMethod_New |
| 0.07% | python | set_dealloc |
| 0.07% | python | meth_dealloc |
| 0.07% | python | func_dealloc |
| 0.06% | python | _PyCode_New |
| 0.06% | python | PyMem_Calloc |
| 0.06% | python | allocate_from_new_pool |
| 0.05% | python | PyObject_CallFinalizerFromDealloc |
| 0.05% | python | object_new |
| 0.05% | python | frame_dealloc |
| 0.05% | python | pattern_new_match.isra.0.part.0 |
| 0.04% | python | PyDict_New |
| 0.04% | python | _PyType_NewManagedObject |
| 0.04% | python | PyUnicode_New |
| 0.04% | python | weakref___new__ |
| 0.04% | python | method_dealloc |
| 0.04% | python | context_tp_dealloc |
| 0.04% | python | listiter_dealloc |
| 0.04% | python | PyMethod_New |
| 0.03% | python | PySlice_New |
| 0.03% | python | PyMem_Malloc |
| 0.03% | python | PyMem_Free |
| 0.02% | python | type_new |
| 0.02% | python | _PyFloat_ExactDealloc |
| 0.02% | python | object_dealloc |
| 0.02% | python | StopIteration_dealloc |
| 0.02% | python | async_gen_wrapped_val_dealloc |
| 0.02% | python | tp_new_wrapper |
| 0.02% | python | BaseException_new |
| 0.02% | python | PyMem_Realloc |
| 0.02% | python | async_gen_asend_dealloc |
| 0.02% | python | tb_dealloc |
| 0.02% | python | _PyAsyncGenValueWrapperNew |
| 0.02% | python | _PyObject_New |
| 0.02% | python | cell_dealloc |
| 0.01% | python | tupleiter_dealloc |
| 0.01% | python | _PyIncrementalNewlineDecoder_decode |
| 0.01% | python | structseq_dealloc |
| 0.01% | python | PyWeakref_NewRef |
| 0.01% | python | range_dealloc |
| 0.01% | python | dictiter_dealloc |
| 0.01% | python | BaseException_dealloc |
| 0.01% | python | dictview_dealloc |
| 0.01% | python | reversed_new_impl |
| 0.01% | python | _PyMem_RawMalloc |
| 0.01% | python | PyCell_New |
| 0.01% | python | _PyTokenizer_translate_newlines |
| 0.01% | python | type_dealloc |
| 0.01% | python | slot_tp_new |
| 0.01% | python | match_dealloc |

### gc

9.83% total

| percentage | object | symbol |
| ---: | :--- | :--- |
| 2.93% | python | gc_collect_region.isra.0 |
| 1.55% | python | visit_decref |
| 1.44% | python | visit_reachable |
| 0.67% | python | visit_add_to_container |
| 0.48% | python | PyObject_GC_UnTrack |
| 0.37% | python | PyObject_GC_Del |
| 0.29% | python | dict_traverse |
| 0.27% | python | _PyObject_GC_New |
| 0.26% | python | list_traverse |
| 0.23% | python | subtype_traverse |
| 0.20% | python | _PyObject_GC_Link |
| 0.19% | python | PyObject_IS_GC |
| 0.17% | python | _PyGC_Collect |
| 0.14% | python | _PyObject_GC_NewVar |
| 0.11% | python | set_traverse |
| 0.09% | python | func_traverse |
| 0.07% | python | type_is_gc |
| 0.05% | python | type_traverse |
| 0.05% | python | _PyDict_MaybeUntrack |
| 0.05% | python | _PyTuple_MaybeUntrack |
| 0.04% | python | gen_traverse |
| 0.03% | python | meth_traverse |
| 0.03% | python | PyGC_Collect |
| 0.02% | python | PyObject_GC_Track |
| 0.02% | python | gc_traverse |
| 0.02% | python | context_tp_traverse |
| 0.01% | python | gc_collect_main |
| 0.01% | python | descr_traverse |
| 0.01% | python | module_traverse |
| 0.01% | python | method_traverse |

### library

9.65% total

| percentage | object | symbol |
| ---: | :--- | :--- |
| 1.57% | python | sre_ucs1_match |
| 1.22% | _pickle.cpython-313-x86_64-linux-gnu.so | save |
| 0.75% | libz.so.1.2.11 | crc32_combine64 |
| 0.57% | python | sre_ucs2_charset.isra.0 |
| 0.32% | _json.cpython-313-x86_64-linux-gnu.so | scanstring_unicode |
| 0.30% | _pickle.cpython-313-x86_64-linux-gnu.so | _Pickler_Write |
| 0.28% | libz.so.1.2.11 | inflateBackEnd |
| 0.25% | _pickle.cpython-313-x86_64-linux-gnu.so | load |
| 0.23% | python | sre_search |
| 0.17% | _json.cpython-313-x86_64-linux-gnu.so | scan_once_unicode |
| 0.17% | libpthread-2.31.so | __pthread_mutex_lock |
| 0.16% | libpthread-2.31.so | pthread_mutex_unlock |
| 0.16% | _pickle.cpython-313-x86_64-linux-gnu.so | PyMemoTable_Set |
| 0.14% | _pickle.cpython-313-x86_64-linux-gnu.so | _Pickler_Write.constprop.3 |
| 0.14% | ld-2.31.so | _dl_rtld_di_serinfo |
| 0.13% | python | sre_ucs1_count |
| 0.12% | libm-2.31.so | f64xsubf128 |
| 0.08% | _pickle.cpython-313-x86_64-linux-gnu.so | Pickler_clear |
| 0.08% | libpython3.11.so.1.0 | _PyEval_EvalFrameDefault |
| 0.07% | _json.cpython-313-x86_64-linux-gnu.so | py_encode_basestring_ascii |
| 0.07% | _pickle.cpython-313-x86_64-linux-gnu.so | memo_put.isra.0 |
| 0.07% | tracer.cpython-313-x86_64-linux-gnu.so | CTracer_trace |
| 0.07% | _pickle.cpython-313-x86_64-linux-gnu.so | Pdata_push |
| 0.05% | _pickle.cpython-313-x86_64-linux-gnu.so | do_append.isra.0 |
| 0.05% | libmagic.so.1.0.0 | 0x000000000000f936 |
| 0.05% | libsqlite3.so.0.8.6 | sqlite3_reset |
| 0.05% | python | _sre_SRE_Pattern_match |
| 0.04% | _asyncio.cpython-313-x86_64-linux-gnu.so | TaskObj_traverse |
| 0.04% | python | pattern_subx |
| 0.04% | ld-2.31.so | _dl_catch_error |
| 0.04% | array.cpython-313-x86_64-linux-gnu.so | array_subscr |
| 0.04% | libz.so.1.2.11 | inflateCodesUsed |
| 0.04% | _pickle.cpython-313-x86_64-linux-gnu.so | load_counted_binunicode |
| 0.04% | libm-2.31.so | __fmod_finite |
| 0.03% | libmagic.so.1.0.0 | 0x000000000000f932 |
| 0.03% | _json.cpython-313-x86_64-linux-gnu.so | encoder_listencode_obj |
| 0.03% | pyexpat.cpython-313-x86_64-linux-gnu.so | normal_updatePosition |
| 0.03% | python | _sre_SRE_Pattern_search |
| 0.02% | math.cpython-313-x86_64-linux-gnu.so | factorial_partial_product |
| 0.02% | pyexpat.cpython-313-x86_64-linux-gnu.so | normal_contentTok |
| 0.02% | _pickle.cpython-313-x86_64-linux-gnu.so | _Unpickler_MemoPut |
| 0.02% | _asyncio.cpython-313-x86_64-linux-gnu.so | task_step_impl |
| 0.02% | _pickle.cpython-313-x86_64-linux-gnu.so | do_setitems.isra.0 |
| 0.02% | _decimal.cpython-313-x86_64-linux-gnu.so | nm_mpd_qadd |
| 0.02% | fastbinary.cpython-313-x86_64-linux-gnu.so | apache::thrift::py::ProtocolBase<apache::thrift::py::BinaryProtocol>::encodeValue |
| 0.02% | libpthread-2.31.so | pthread_cond_signal@@GLIBC_2.3.2 |
| 0.02% | _pickle.cpython-313-x86_64-linux-gnu.so | 0x0000000000005ce4 |
| 0.02% | _pickle.cpython-313-x86_64-linux-gnu.so | memo_get.isra.0 |
| 0.02% | libz.so.1.2.11 | inflate |
| 0.02% | _decimal.cpython-313-x86_64-linux-gnu.so | mpd_setdigits |
| 0.02% | _json.cpython-313-x86_64-linux-gnu.so | encoder_encode_key_value |
| 0.02% | _pickle.cpython-313-x86_64-linux-gnu.so | Unpickler_clear |
| 0.02% | libpython3.11.so.1.0 | _PyDict_GetItem_KnownHash |
| 0.02% | _bisect.cpython-313-x86_64-linux-gnu.so | _bisect_bisect_right |
| 0.02% | _decimal.cpython-313-x86_64-linux-gnu.so | _mpd_qaddsub |
| 0.02% | _asyncio.cpython-313-x86_64-linux-gnu.so | TaskObj_clear |
| 0.02% | libsqlite3.so.0.8.6 | sqlite3_exec |
| 0.02% | _decimal.cpython-313-x86_64-linux-gnu.so | _mpd_qmul |
| 0.02% | pyexpat.cpython-313-x86_64-linux-gnu.so | sip24_update |
| 0.02% | array.cpython-313-x86_64-linux-gnu.so | array_ass_subscr |
| 0.01% | libpthread-2.31.so | __errno_location |
| 0.01% | _decimal.cpython-313-x86_64-linux-gnu.so | _mpd_check_exp |
| 0.01% | libsqlite3.so.0.8.6 | sqlite3_randomness |
| 0.01% | _pickle.cpython-313-x86_64-linux-gnu.so | marker.isra.0 |
| 0.01% | _decimal.cpython-313-x86_64-linux-gnu.so | nm_mpd_qmul |
| 0.01% | _heapq.cpython-313-x86_64-linux-gnu.so | siftup |
| 0.01% | pyexpat.cpython-313-x86_64-linux-gnu.so | accountingDiffTolerated.part.0 |
| 0.01% | pyexpat.cpython-313-x86_64-linux-gnu.so | normal_nameLength |
| 0.01% | _pickle.cpython-313-x86_64-linux-gnu.so | 0x0000000000005e64 |
| 0.01% | libpython3.11.so.1.0 | PyObject_Malloc |
| 0.01% | _asyncio.cpython-313-x86_64-linux-gnu.so | task_step |
| 0.01% | pyexpat.cpython-313-x86_64-linux-gnu.so | doContent |
| 0.01% | _decimal.cpython-313-x86_64-linux-gnu.so | _mpd_baseshiftr |
| 0.01% | libpython3.11.so.1.0 | deduce_unreachable |
| 0.01% | libpython3.11.so.1.0 | visit_decref |
| 0.01% | _asyncio.cpython-313-x86_64-linux-gnu.so | future_init |
| 0.01% | _asyncio.cpython-313-x86_64-linux-gnu.so | _asyncio_Task___init__ |
| 0.01% | pyexpat.cpython-313-x86_64-linux-gnu.so | lookup.constprop.0 |
| 0.01% | _elementtree.cpython-313-x86_64-linux-gnu.so | expat_end_handler |
| 0.01% | libpthread-2.31.so | sem_trywait@@GLIBC_2.2.5 |
| 0.01% | libpthread-2.31.so | sem_post@@GLIBC_2.2.5 |
| 0.01% | _asyncio.cpython-313-x86_64-linux-gnu.so | _asyncio_Future_add_done_callback |
| 0.01% | _elementtree.cpython-313-x86_64-linux-gnu.so | treebuilder_handle_start |
| 0.01% | _asyncio.cpython-313-x86_64-linux-gnu.so | future_schedule_callbacks |
| 0.01% | libsqlite3.so.0.8.6 | sqlite3_value_double |
| 0.01% | libssl.so.1.1 | SSL_rstate_string |
| 0.01% | libpython3.11.so.1.0 | PyDict_SetDefault |
| 0.01% | _decimal.cpython-313-x86_64-linux-gnu.so | mpd_qquantize |
| 0.01% | libpython3.11.so.1.0 | type_new |
| 0.01% | _sqlite3.cpython-313-x86_64-linux-gnu.so | _pysqlite_query_execute |
| 0.01% | libsqlite3.so.0.8.6 | sqlite3_str_value |
| 0.01% | libpython3.11.so.1.0 | visit_reachable |
| 0.01% | _asyncio.cpython-313-x86_64-linux-gnu.so | TaskStepMethWrapper_traverse |
| 0.01% | _asyncio.cpython-313-x86_64-linux-gnu.so | FutureObj_traverse |
| 0.01% | _decimal.cpython-313-x86_64-linux-gnu.so | dec_addstatus |
| 0.01% | fastbinary.cpython-313-x86_64-linux-gnu.so | apache::thrift::py::ProtocolBase<apache::thrift::py::BinaryProtocol>::decodeValue |
| 0.01% | libpython3.11.so.1.0 | gc_collect_main |
| 0.01% | _decimal.cpython-313-x86_64-linux-gnu.so | PyDecType_New |
| 0.01% | _elementtree.cpython-313-x86_64-linux-gnu.so | element_gc_traverse |
| 0.01% | _decimal.cpython-313-x86_64-linux-gnu.so | dec_mpd_qquantize |
| 0.01% | libsqlite3.so.0.8.6 | sqlite3_preupdate_old |
| 0.01% | libsqlite3.so.0.8.6 | sqlite3_value_int64 |
| 0.01% | pyexpat.cpython-313-x86_64-linux-gnu.so | normal_getAtts |
| 0.01% | libpython3.11.so.1.0 | r_object |
| 0.01% | array.cpython-313-x86_64-linux-gnu.so | d_setitem |
| 0.01% | libpython3.11.so.1.0 | PyObject_Free |
| 0.01% | _pickle.cpython-313-x86_64-linux-gnu.so | 0x0000000000005fc4 |
| 0.01% | _decimal.cpython-313-x86_64-linux-gnu.so | dec_dealloc |
| 0.01% | libsqlite3.so.0.8.6 | sqlite3_extended_errcode |
| 0.01% | _asyncio.cpython-313-x86_64-linux-gnu.so | FutureObj_clear |
| 0.01% | _asyncio.cpython-313-x86_64-linux-gnu.so | task_wakeup |
| 0.01% | math.cpython-313-x86_64-linux-gnu.so | math_sqrt |
| 0.01% | pyexpat.cpython-313-x86_64-linux-gnu.so | sip24_final |
| 0.01% | _pickle.cpython-313-x86_64-linux-gnu.so | _Unpickler_New |
| 0.01% | fastbinary.cpython-313-x86_64-linux-gnu.so | apache::thrift::py::ProtocolBase<apache::thrift::py::BinaryProtocol>::readStruct |
| 0.01% | _decimal.cpython-313-x86_64-linux-gnu.so | _mpd_baseadd |
| 0.01% | math.cpython-313-x86_64-linux-gnu.so | math_cos |
| 0.01% | _decimal.cpython-313-x86_64-linux-gnu.so | mpd_qfinalize.part.0 |
| 0.01% | fastbinary.cpython-313-x86_64-linux-gnu.so | apache::thrift::py::ProtocolBase<apache::thrift::py::BinaryProtocol>::readBytes |
| 0.01% | _decimal.cpython-313-x86_64-linux-gnu.so | mpd_qshiftr |
| 0.01% | _random.cpython-313-x86_64-linux-gnu.so | genrand_uint32 |
| 0.01% | libsqlite3.so.0.8.6 | sqlite3_step |
| 0.01% | libpython3.11.so.1.0 | tupledealloc |
| 0.01% | libsqlite3.so.0.8.6 | sqlite3_vtab_config |
| 0.01% | python | sre_ucs4_match |

### dynamic

5.63% total

| percentage | object | symbol |
| ---: | :--- | :--- |
| 0.34% | python | PyObject_GenericGetAttr |
| 0.31% | python | PyObject_RichCompareBool |
| 0.31% | python | PyType_IsSubtype |
| 0.27% | python | PyObject_Hash |
| 0.24% | python | _PyObject_GenericGetAttrWithDict |
| 0.24% | python | _PyObject_GetMethod |
| 0.20% | python | PyNumber_AsSsize_t |
| 0.18% | python | PyObject_GetAttr |
| 0.17% | python | _PyObject_MakeTpCall |
| 0.16% | python | PyObject_Malloc |
| 0.15% | python | type_ready |
| 0.15% | python | PyObject_Vectorcall |
| 0.12% | python | PyObject_IsTrue |
| 0.12% | python | _PyObject_TryGetInstanceAttribute |
| 0.11% | python | PyObject_Free |
| 0.11% | python | _PyObject_LookupSpecial |
| 0.10% | python | _PyType_GetDict |
| 0.10% | python | type_call |
| 0.10% | python | PyObject_ClearManagedDict |
| 0.09% | python | PyObject_GetOptionalAttr |
| 0.09% | python | PyObject_VisitManagedDict |
| 0.09% | python | PyObject_GetItem |
| 0.08% | python | _PyObject_GenericSetAttrWithDict |
| 0.08% | python | PyObject_ClearWeakRefs |
| 0.07% | python | PyObject_GetIter |
| 0.07% | python | PyObject_IsInstance |
| 0.07% | python | _PyObject_Call_Prepend |
| 0.07% | python | PyObject_CallOneArg |
| 0.07% | python | PyType_GetModuleByDef |
| 0.06% | python | object_isinstance |
| 0.06% | python | PyObject_RichCompare |
| 0.06% | python | getset_get |
| 0.06% | python | PyObject_Call |
| 0.05% | python | do_super_lookup |
| 0.04% | python | PyObject_SetAttr |
| 0.04% | python | PyObject_SetItem |
| 0.04% | python | PyDescr_IsData |
| 0.04% | python | PyNumber_Add |
| 0.04% | python | PyObject_Size |
| 0.04% | python | PyIter_Next |
| 0.04% | python | PyObject_VectorcallMethod |
| 0.04% | python | PyNumber_Multiply |
| 0.04% | python | _Py_type_getattro_impl |
| 0.04% | python | method_get |
| 0.03% | python | delitem_common |
| 0.03% | python | PyIter_Send |
| 0.03% | python | slot_tp_richcompare |
| 0.03% | python | StopIteration_init |
| 0.02% | python | PyObject_Str |
| 0.02% | python | PyNumber_And |
| 0.02% | python | PySequence_Fast |
| 0.02% | python | PySequence_Contains |
| 0.02% | python | PyNumber_TrueDivide |
| 0.02% | python | PySequence_Tuple |
| 0.02% | python | _PySuper_Lookup |
| 0.02% | python | object_richcompare |
| 0.02% | python | _PyObject_RealIsInstance |
| 0.02% | python | PyNumber_Subtract |
| 0.01% | python | _PyObject_CallFunctionVa |
| 0.01% | python | PyNumber_Index |
| 0.01% | python | _PyNumber_Index |
| 0.01% | python | object_get_class |
| 0.01% | python | PyNumber_Remainder |
| 0.01% | python | _PyObject_InitInlineValues |
| 0.01% | python | PyNumber_FloorDivide |
| 0.01% | python | PyNumber_Xor |
| 0.01% | python | _PyObject_StoreInstanceAttribute |
| 0.01% | python | object_recursive_isinstance |
| 0.01% | python | PyNumber_Rshift |
| 0.01% | python | PyMapping_GetOptionalItem |
| 0.01% | python | PyObject_GenericHash |
| 0.01% | python | PyObject_GetBuffer |
| 0.01% | python | PyNumber_InPlaceAdd |
| 0.01% | python | object_vacall |
| 0.01% | python | PyObject_IsSubclass |
| 0.01% | python | type_mro_modified |
| 0.01% | python | PyObject_SelfIter |
| 0.01% | python | object_init |
| 0.01% | python | PyNumber_InPlaceTrueDivide |
| 0.01% | python | PyObject_LengthHint |
| 0.01% | python | PyObject_DelItem |
| 0.01% | python | PyObject_HasAttrWithError |

### lookup

4.64% total

| percentage | object | symbol |
| ---: | :--- | :--- |
| 1.83% | python | unicodekeys_lookup_unicode |
| 1.28% | python | _Py_dict_lookup |
| 0.85% | python | _PyType_Lookup |
| 0.27% | python | find_name_in_mro |
| 0.23% | python | update_one_slot |
| 0.14% | python | _Py_type_getattro |
| 0.02% | python | builtin_getattr |
| 0.01% | python | PyMember_GetOne |
| 0.01% | python | PyMember_SetOne |

### kernel

4.44% total

| percentage | object | symbol |
| ---: | :--- | :--- |
| 0.62% | [kernel.kallsyms] | copy_user_enhanced_fast_string |
| 0.25% | [kernel.kallsyms] | clear_page_erms |
| 0.13% | [kernel.kallsyms] | native_irq_return_iret |
| 0.10% | [kernel.kallsyms] | __d_lookup_rcu |
| 0.09% | [kernel.kallsyms] | sync_regs |
| 0.08% | [kernel.kallsyms] | rmqueue |
| 0.07% | [kernel.kallsyms] | _raw_spin_lock |
| 0.07% | [kernel.kallsyms] | zap_pte_range.isra.0 |
| 0.06% | [kernel.kallsyms] | memset_erms |
| 0.05% | [kernel.kallsyms] | free_pcppages_bulk |
| 0.05% | [kernel.kallsyms] | filemap_map_pages |
| 0.05% | [kernel.kallsyms] | __handle_mm_fault |
| 0.05% | [kernel.kallsyms] | smp_call_function_single |
| 0.04% | [kernel.kallsyms] | try_charge |
| 0.04% | [kernel.kallsyms] | link_path_walk.part.0 |
| 0.04% | [kernel.kallsyms] | release_pages |
| 0.04% | [kernel.kallsyms] | get_mem_cgroup_from_mm |
| 0.04% | [kernel.kallsyms] | kmem_cache_alloc |
| 0.03% | [kernel.kallsyms] | __pagevec_lru_add_fn |
| 0.03% | [kernel.kallsyms] | syscall_return_via_sysret |
| 0.03% | [kernel.kallsyms] | mem_cgroup_throttle_swaprate |
| 0.03% | [kernel.kallsyms] | ext4_htree_store_dirent |
| 0.03% | [kernel.kallsyms] | handle_mm_fault |
| 0.03% | [kernel.kallsyms] | __ext4fs_dirhash |
| 0.03% | [kernel.kallsyms] | mem_cgroup_try_charge |
| 0.03% | [kernel.kallsyms] | copy_page |
| 0.02% | [kernel.kallsyms] | page_remove_rmap |
| 0.02% | [kernel.kallsyms] | __alloc_pages_nodemask |
| 0.02% | [kernel.kallsyms] | strncpy_from_user |
| 0.02% | [kernel.kallsyms] | filldir64 |
| 0.02% | [kernel.kallsyms] | entry_SYSCALL_64 |
| 0.02% | [kernel.kallsyms] | kmem_cache_free |
| 0.02% | [kernel.kallsyms] | memcg_kmem_get_cache |
| 0.02% | [kernel.kallsyms] | lookup_fast |
| 0.02% | [kernel.kallsyms] | __virt_addr_valid |
| 0.02% | [kernel.kallsyms] | find_get_entry |
| 0.02% | [kernel.kallsyms] | inode_permission |
| 0.02% | [kernel.kallsyms] | do_syscall_64 |
| 0.02% | [kernel.kallsyms] | do_user_addr_fault |
| 0.02% | [kernel.kallsyms] | kfree |
| 0.02% | [kernel.kallsyms] | memcpy_erms |
| 0.02% | [kernel.kallsyms] | find_vma |
| 0.02% | [kernel.kallsyms] | do_anonymous_page |
| 0.02% | [kernel.kallsyms] | prep_new_page |
| 0.02% | [kernel.kallsyms] | str2hashbuf_signed |
| 0.02% | [kernel.kallsyms] | __slab_free |
| 0.02% | [kernel.kallsyms] | _raw_spin_lock_irqsave |
| 0.02% | [kernel.kallsyms] | generic_permission |
| 0.02% | [kernel.kallsyms] | get_page_from_freelist |
| 0.02% | [kernel.kallsyms] | walk_component |
| 0.02% | [kernel.kallsyms] | vmacache_find |
| 0.02% | [kernel.kallsyms] | rb_insert_color |
| 0.01% | [kernel.kallsyms] | __count_memcg_events |
| 0.01% | [kernel.kallsyms] | rb_next |
| 0.01% | [kernel.kallsyms] | page_fault |
| 0.01% | [kernel.kallsyms] | __fget_light |
| 0.01% | [kernel.kallsyms] | perf_iterate_ctx |
| 0.01% | [kernel.kallsyms] | __mod_memcg_state |
| 0.01% | [kernel.kallsyms] | error_entry |
| 0.01% | [kernel.kallsyms] | __mod_lruvec_state |
| 0.01% | [kernel.kallsyms] | ext4_getattr |
| 0.01% | [kernel.kallsyms] | perf_event_alloc |
| 0.01% | [kernel.kallsyms] | psi_task_change |
| 0.01% | [kernel.kallsyms] | xas_load |
| 0.01% | [kernel.kallsyms] | entry_SYSCALL_64_after_hwframe |
| 0.01% | [kernel.kallsyms] | __check_object_size |
| 0.01% | [kernel.kallsyms] | security_inode_getattr |
| 0.01% | [kernel.kallsyms] | up_read |
| 0.01% | [kernel.kallsyms] | generic_file_buffered_read |
| 0.01% | [kernel.kallsyms] | tcp_sendmsg_locked |
| 0.01% | [kernel.kallsyms] | down_read_trylock |
| 0.01% | [kernel.kallsyms] | _cond_resched |
| 0.01% | [kernel.kallsyms] | __lru_cache_add |
| 0.01% | [kernel.kallsyms] | swapgs_restore_regs_and_return_to_usermode |
| 0.01% | [kernel.kallsyms] | lru_cache_add_active_or_unevictable |
| 0.01% | [kernel.kallsyms] | __kmalloc |
| 0.01% | [kernel.kallsyms] | ___slab_alloc |
| 0.01% | [kernel.kallsyms] | native_flush_tlb_one_user |
| 0.01% | [kernel.kallsyms] | __follow_mount_rcu.isra.0 |
| 0.01% | [kernel.kallsyms] | page_add_file_rmap |
| 0.01% | [kernel.kallsyms] | fsnotify |
| 0.01% | [kernel.kallsyms] | set_root |
| 0.01% | [kernel.kallsyms] | native_write_msr |
| 0.01% | [kernel.kallsyms] | alloc_pages_vma |
| 0.01% | [kernel.kallsyms] | free_unref_page_prepare.part.0 |
| 0.01% | [kernel.kallsyms] | rcu_all_qs |
| 0.01% | [kernel.kallsyms] | alloc_set_pte |
| 0.01% | [kernel.kallsyms] | pagevec_lru_move_fn |
| 0.01% | [kernel.kallsyms] | format_decode |
| 0.01% | [kernel.kallsyms] | free_pages_and_swap_cache |
| 0.01% | [kernel.kallsyms] | __ext4_check_dir_entry |
| 0.01% | [kernel.kallsyms] | __mod_node_page_state |
| 0.01% | [kernel.kallsyms] | __vma_adjust |
| 0.01% | [kernel.kallsyms] | show_cpuinfo |
| 0.01% | [kernel.kallsyms] | vsnprintf |
| 0.01% | [kernel.kallsyms] | fpregs_assert_state_consistent |
| 0.01% | [kernel.kallsyms] | page_counter_try_charge |
| 0.01% | [kernel.kallsyms] | __lock_text_start |
| 0.01% | [kernel.kallsyms] | __mod_zone_page_state |
| 0.01% | [kernel.kallsyms] | in_group_p |
| 0.01% | [kernel.kallsyms] | memcg_kmem_put_cache |
| 0.01% | [kernel.kallsyms] | free_unref_page_list |
| 0.01% | [kernel.kallsyms] | __legitimize_mnt |
| 0.01% | [kernel.kallsyms] | update_curr |
| 0.01% | [kernel.kallsyms] | __lookup_mnt |
| 0.01% | [kernel.kallsyms] | memchr |
| 0.01% | [kernel.kallsyms] | string_nocheck |
| 0.01% | [kernel.kallsyms] | mem_cgroup_commit_charge |
| 0.01% | [kernel.kallsyms] | __update_load_avg_se |
| 0.01% | [kernel.kallsyms] | page_counter_cancel |
| 0.01% | [kernel.kallsyms] | mem_cgroup_from_task |
| 0.01% | [kernel.kallsyms] | update_cfs_group |
| 0.01% | [kernel.kallsyms] | unlock_page |
| 0.01% | [kernel.kallsyms] | vma_interval_tree_insert |
| 0.01% | [kernel.kallsyms] | xas_start |
| 0.01% | [kernel.kallsyms] | security_inode_permission |
| 0.01% | [kernel.kallsyms] | kmem_cache_alloc_trace |
| 0.01% | [kernel.kallsyms] | skb_release_data |
| 0.01% | [kernel.kallsyms] | vfs_getattr_nosec |
| 0.01% | [kernel.kallsyms] | update_load_avg |
| 0.01% | [kernel.kallsyms] | free_unref_page_commit |
| 0.01% | [kernel.kallsyms] | __free_pages_ok |
| 0.01% | [kernel.kallsyms] | __check_heap_object |
| 0.01% | [kernel.kallsyms] | mem_cgroup_try_charge_delay |
| 0.01% | [kernel.kallsyms] | unmapped_area_topdown |
| 0.01% | [kernel.kallsyms] | __alloc_file |

### unknown

3.88% total

| percentage | object | symbol |
| ---: | :--- | :--- |
| 0.17% | python | _Py_hashtable_get_entry_generic |
| 0.10% | python | _PyThreadState_PushFrame |
| 0.09% | python | call_instrumentation_vector.part.0 |
| 0.07% | python | make_gen |
| 0.07% | python | slot_tp_init |
| 0.07% | python | gen_iternext |
| 0.06% | python | convertitem.constprop.0 |
| 0.06% | python | memset@plt |
| 0.06% | python | PyThreadState_Get |
| 0.06% | python | _PyIO_find_line_ending |
| 0.05% | python | compute_range_length |
| 0.05% | python | func_clear |
| 0.04% | python | memcpy@plt |
| 0.04% | python | _list_extend |
| 0.04% | python | _PySet_Contains |
| 0.04% | python | method_vectorcall |
| 0.04% | python | PyThread_get_thread_ident |
| 0.04% | python | _PyStack_UnpackDict |
| 0.04% | python | _Py_call_instrumentation_line |
| 0.04% | python | _Py_MakeCoro |
| 0.04% | python | tok_get_normal_mode |
| 0.03% | python | range_iter |
| 0.03% | python | min_max |
| 0.03% | python | _Py_HashBytes |
| 0.03% | python | async_gen_asend_iternext |
| 0.03% | python | context_run |
| 0.03% | [vdso] | __vdso_clock_gettime |
| 0.03% | python | new_keys_object.constprop.0 |
| 0.03% | python | _PyCfg_OptimizeCodeUnit |
| 0.03% | python | do_mkvalue |
| 0.02% | python | sys_audit_tstate |
| 0.02% | python | store_instance_attr_lock_held |
| 0.02% | python | _PyGen_Finalize |
| 0.02% | python | hashtable_unicode_compare |
| 0.02% | python | _io_TextIOWrapper_write |
| 0.02% | python | _PyAssemble_MakeCodeObject |
| 0.02% | python | PyContextVar_Get |
| 0.02% | python | PySys_Audit |
| 0.02% | python | pysiphash |
| 0.02% | python | tok_nextc |
| 0.02% | python | bounded_lru_cache_wrapper |
| 0.02% | python | tailmatch |
| 0.02% | python | code_hash |
| 0.02% | python | _PyArena_Malloc |
| 0.02% | python | async_gen_anext |
| 0.02% | python | _PyGen_FetchStopIterationValue |
| 0.02% | python | primary_rule |
| 0.02% | python | _PyFunction_ClearCodeByVersion |
| 0.02% | python | hashtable_unicode_hash |
| 0.02% | python | _Py_hashtable_get |
| 0.02% | python | memcmp@plt |
| 0.02% | python | term_rule |
| 0.01% | python | build_indices_generic |
| 0.01% | python | range_subscript |
| 0.01% | python | _io_BytesIO_read |
| 0.01% | python | builtin_sum |
| 0.01% | python | _PyThreadState_MustExit |
| 0.01% | python | slot_tp_hash |
| 0.01% | python | _PyCoro_GetAwaitableIter |
| 0.01% | python | _PyThreadState_Attach |
| 0.01% | python | range_vectorcall |
| 0.01% | python | _PyModule_ClearDict |
| 0.01% | python | PyContext_CopyCurrent |
| 0.01% | python | pthread_self@plt |
| 0.01% | python | PyIndex_Check |
| 0.01% | python | _Py_bytes_lower |
| 0.01% | python | _Py_Specialize_LoadAttr |
| 0.01% | python | _Py_Specialize_Call |
| 0.01% | python | unsafe_tuple_compare |
| 0.01% | python | analyze_descriptor |
| 0.01% | python | _PyThreadState_GetCurrent |
| 0.01% | python | _io_open |
| 0.01% | python | map_next |
| 0.01% | python | _PyObjectDict_SetItem |
| 0.01% | python | fill_time |
| 0.01% | python | _PyFunction_SetVersion |
| 0.01% | python | slot_tp_iternext |
| 0.01% | python | _PyGen_SetStopIterationValue |
| 0.01% | python | PySet_Add |
| 0.01% | python | any_find_slice |
| 0.01% | python | slot_mp_ass_subscript |
| 0.01% | python | countformat |
| 0.01% | python | inversion_rule |
| 0.01% | python | va_build_value |
| 0.01% | python | _PyCfg_OptimizedCfgToInstructionSequence |
| 0.01% | python | PyGen_am_send |
| 0.01% | python | _PyThreadState_Detach |
| 0.01% | python | subtype_clear |
| 0.01% | python | builtin_hasattr |
| 0.01% | python | build_string |
| 0.01% | python | member_get |
| 0.01% | python | sum_rule |
| 0.01% | python | vectorcall_maybe.constprop.0 |
| 0.01% | python | stringio_iternext |
| 0.01% | python | mro_implementation_unlocked |
| 0.01% | python | dictitems_iter |
| 0.01% | python | strlen@plt |
| 0.01% | python | shift_expr_rule |
| 0.01% | python | slot_mp_subscript |
| 0.01% | python | mro_internal_unlocked |
| 0.01% | python | _PyType_FromMetaclass_impl |
| 0.01% | python | builtin_id |
| 0.01% | python | clear_weakref_lock_held |
| 0.01% | python | _Py_convert_optional_to_ssize_t |
| 0.01% | python | slot_tp_iter |
| 0.01% | python | weakref_hash |
| 0.01% | python | func_descr_get |
| 0.01% | python | update_slot |
| 0.01% | python | binary_op1 |
| 0.01% | python | compiler_visit_expr1 |
| 0.01% | python | weakref___init__ |
| 0.01% | python | _PyCode_GetCode |
| 0.01% | python | _PyBytes_Resize |
| 0.01% | python | unsafe_long_compare |
| 0.01% | python | assign_version_tag |
| 0.01% | python | _io_FileIO___init__ |
| 0.01% | python | slot_sq_contains |
| 0.01% | python | astfold_expr |
| 0.01% | python | bitwise_or_rule |
| 0.01% | python | copy_lock_held |
| 0.01% | python | unsafe_latin_compare |
| 0.01% | python | sm_descr_get |
| 0.01% | python | _Py_call_instrumentation_jump |
| 0.01% | python | wrapperdescr_call |
| 0.01% | python | os_stat |
| 0.01% | python | delitem_knownhash_lock_held |
| 0.01% | python | symtable_visit_expr |
| 0.01% | python | 0x0000000000080740 |
| 0.01% | python | bitwise_and_rule |
| 0.01% | python | make_dict_from_instance_attributes |
| 0.01% | python | basicblock_remove_redundant_nops |
| 0.01% | python | _PyFrame_MakeAndSetFrameObject |
| 0.01% | python | sys_trace_return |
| 0.01% | python | islice_next |
| 0.01% | python | write_bytes |
| 0.01% | python | slot_tp_call |
| 0.01% | python | bitwise_xor_rule |
| 0.01% | python | write_str |
| 0.01% | python | scan_block_for_locals |
| 0.01% | python | _PyInstructionSequence_Addop |
| 0.01% | python | lru_cache_make_key |
| 0.01% | python | _Py_VaBuildStack |

### int

3.38% total

| percentage | object | symbol |
| ---: | :--- | :--- |
| 0.70% | python | k_mul |
| 0.38% | python | x_divrem |
| 0.31% | python | _PyLong_Add |
| 0.21% | python | PyLong_FromLong |
| 0.20% | python | long_hash |
| 0.15% | python | x_add |
| 0.13% | python | PyLong_AsLongAndOverflow |
| 0.11% | python | _PyLong_Subtract |
| 0.11% | python | long_to_decimal_string_internal |
| 0.11% | python | PyLong_AsSsize_t |
| 0.09% | python | long_bitwise |
| 0.09% | python | long_richcompare |
| 0.09% | python | PyLong_FromSsize_t |
| 0.09% | python | x_sub |
| 0.08% | python | PyLong_FromString |
| 0.04% | python | _PyLong_Multiply |
| 0.04% | python | long_rshift1 |
| 0.03% | python | PyLong_FromVoidPtr |
| 0.03% | python | long_and |
| 0.03% | python | PyLong_AsDouble |
| 0.03% | python | PyLong_AsLong |
| 0.03% | python | long_mul |
| 0.03% | python | l_mod |
| 0.03% | python | long_add |
| 0.03% | python | PyLong_FromUnsignedLong |
| 0.03% | python | long_div |
| 0.02% | python | long_rshift |
| 0.02% | python | long_lshift1 |
| 0.01% | python | long_to_decimal_string |
| 0.01% | python | _PyLong_GCD |
| 0.01% | python | PyLong_FromLongLong |
| 0.01% | python | long_xor |
| 0.01% | python | long_lshift |
| 0.01% | python | PyLong_AsInt |
| 0.01% | python | PyLong_FromUnsignedLongLong |
| 0.01% | python | long_float |
| 0.01% | python | long_neg |
| 0.01% | python | long_mod |
| 0.01% | python | _PyLong_FromByteArray |

### libc

3.30% total

| percentage | object | symbol |
| ---: | :--- | :--- |
| 2.05% | libc-2.31.so | __nss_database_lookup |
| 0.50% | libc-2.31.so | pthread_attr_setschedparam |
| 0.30% | libcrypto.so.1.1 | CRYPTO_secure_actual_size |
| 0.12% | libc-2.31.so | malloc |
| 0.04% | libc-2.31.so | free |
| 0.03% | libc-2.31.so | __gconv_get_alias_db |
| 0.03% | libc-2.31.so | wcsrtombs |
| 0.02% | libc-2.31.so | pthread_self |
| 0.02% | libc-2.31.so | clock_gettime |
| 0.01% | libc-2.31.so | _dl_addr |
| 0.01% | libc-2.31.so | __libc_realloc |
| 0.01% | libc-2.31.so | __xstat |
| 0.01% | libc-2.31.so | __wcsncasecmp_l |
| 0.01% | libc-2.31.so | psiginfo |

### str

2.66% total

| percentage | object | symbol |
| ---: | :--- | :--- |
| 0.46% | python | siphash13 |
| 0.14% | python | _PyUnicode_FromUCS1.part.0 |
| 0.14% | python | ascii_decode |
| 0.14% | python | _PyUnicode_InternInPlace |
| 0.13% | python | _PyUnicode_JoinArray.part.0 |
| 0.12% | python | unicode_decode_utf8 |
| 0.10% | python | replace |
| 0.10% | python | _copy_characters.part.0.constprop.0 |
| 0.09% | python | PyUnicode_Substring |
| 0.07% | python | resize_compact |
| 0.06% | python | _PyUnicode_FromUCS4.part.0 |
| 0.06% | python | _PyUnicode_Equal |
| 0.06% | python | PyUnicode_RichCompare |
| 0.05% | python | PyUnicode_Contains |
| 0.05% | python | PyBytes_FromStringAndSize |
| 0.05% | python | PyUnicode_Format |
| 0.05% | python | PyUnicode_AsUTF8AndSize |
| 0.04% | python | PyUnicode_FromFormatV |
| 0.04% | python | _PyUnicodeWriter_WriteStr |
| 0.03% | python | unicode_hash |
| 0.03% | python | split |
| 0.03% | python | unicode_replace |
| 0.03% | python | _PyUnicodeWriter_PrepareInternal |
| 0.03% | python | PyUnicode_AsUCS4 |
| 0.02% | python | PyUnicode_InternInPlace |
| 0.02% | python | PyUnicode_FromWideChar |
| 0.02% | python | bytes_subscript |
| 0.02% | python | PyUnicode_Concat |
| 0.02% | python | stringlib_bytes_join |
| 0.01% | python | unicode_rstrip |
| 0.01% | python | unicode_subscript |
| 0.01% | python | _PyUnicodeWriter_WriteSubstring.part.0 |
| 0.01% | python | unicode_lower |
| 0.01% | python | PyUnicode_Decode.part.0 |
| 0.01% | python | unicode_startswith |
| 0.01% | python | _PyUnicodeWriter_WriteASCIIString |
| 0.01% | python | unicode_join |
| 0.01% | python | _PyUnicodeWriter_Init |
| 0.01% | python | PyBytes_Repr |
| 0.01% | python | PyUnicode_FromKindAndData |
| 0.01% | python | unicode_repr |
| 0.01% | python | PyUnicode_AsEncodedString.part.0 |
| 0.01% | python | bytes_richcompare |
| 0.01% | python | unicode_encode_utf8 |
| 0.01% | python | _PyUnicodeWriter_Finish |
| 0.01% | python | _PyUnicode_ToLowercase |
| 0.01% | python | unicode_rpartition |
| 0.01% | python | PyUnicode_InternFromString |
| 0.01% | python | bytes_concat |
| 0.01% | python | PyUnicode_FindChar |
| 0.01% | python | unicode_vectorcall |
| 0.01% | python | _PyUnicode_TranslateCharmap |
| 0.01% | python | PyUnicode_Splitlines |
| 0.01% | python | unicode_fromformat_write_cstr |
| 0.01% | python | unicode_encode |
| 0.01% | python | PyUnicode_FromEncodedObject |
| 0.01% | python | unicode_endswith |
| 0.01% | python | _PyUnicode_IsAlpha |
| 0.01% | python | _PyUnicode_IsLowercase |
| 0.01% | python | PyUnicode_EncodeFSDefault |

### dict

2.59% total

| percentage | object | symbol |
| ---: | :--- | :--- |
| 0.42% | python | insertdict |
| 0.36% | python | PyDict_GetItemRef |
| 0.26% | python | PyDict_Next |
| 0.20% | python | insert_to_emptydict |
| 0.18% | python | _PyDict_GetItem_KnownHash |
| 0.15% | python | dict_setdefault_ref_lock_held |
| 0.14% | python | find_empty_slot |
| 0.11% | python | build_indices_unicode |
| 0.10% | python | dict_get |
| 0.09% | python | _PyDict_FromItems |
| 0.07% | python | PyDict_SetItem |
| 0.05% | python | dictiter_iternextitem |
| 0.04% | python | dict_merge |
| 0.04% | python | dictresize |
| 0.03% | python | _PyDict_LoadGlobal |
| 0.03% | python | PyDict_Contains |
| 0.03% | python | PyDict_GetItemWithError |
| 0.03% | python | dict_ass_sub |
| 0.03% | python | _PyDict_SetItem_Take2 |
| 0.03% | python | dict_subscript |
| 0.03% | python | PyDict_Clear |
| 0.02% | python | clone_combined_dict_keys.isra.0 |
| 0.02% | python | PyDict_GetItem |
| 0.01% | python | dictiter_iternextkey |
| 0.01% | python | dict_items |
| 0.01% | python | dictiter_iternextvalue |
| 0.01% | python | dict_tp_clear |
| 0.01% | python | _PyDict_Next |
| 0.01% | python | _PyDict_DelItem_KnownHash |

### miscobj

1.22% total

| percentage | object | symbol |
| ---: | :--- | :--- |
| 0.25% | python | set_lookkey |
| 0.20% | python | PySlice_AdjustIndices |
| 0.11% | python | set_add_entry |
| 0.10% | python | _PyBuildSlice_ConsumeRefs |
| 0.08% | python | set_issubset_impl |
| 0.07% | python | setiter_iternext |
| 0.05% | python | PySlice_Unpack |
| 0.04% | python | set_difference |
| 0.03% | python | PyBool_FromLong |
| 0.03% | python | set_table_resize |
| 0.03% | python | deque_append |
| 0.02% | python | PyBuffer_Release |
| 0.02% | python | enum_next |
| 0.02% | python | dequeiter_next |
| 0.02% | python | bytearray_ass_subscript |
| 0.02% | python | PyBuffer_FillInfo |
| 0.01% | python | set_merge_lock_held.part.0 |
| 0.01% | python | deque_popleft |
| 0.01% | python | set_intersection |
| 0.01% | python | _PySlice_GetLongIndices |
| 0.01% | python | set_update_iterable_lock_held |
| 0.01% | python | deque_clear.part.0 |
| 0.01% | python | set_richcompare |
| 0.01% | python | set_discard |

### tuple

0.98% total

| percentage | object | symbol |
| ---: | :--- | :--- |
| 0.36% | python | tuplehash |
| 0.16% | python | _PyTuple_FromArraySteal |
| 0.14% | python | _PyTuple_FromArray.part.0 |
| 0.11% | python | tupletraverse |
| 0.04% | python | tuplerichcompare |
| 0.03% | python | PyTuple_Pack |
| 0.02% | python | _PyTuple_ClearFreeList |
| 0.02% | python | _PyTuple_FromArray |
| 0.02% | python | tuple_iter |
| 0.01% | python | PyTuple_Size |
| 0.01% | python | tupleiter_next |
| 0.01% | python | tuplesubscript |
| 0.01% | python | _PyTuple_Resize |
| 0.01% | python | PyTuple_GetSlice |
| 0.01% | python | tuplecontains |

### list

0.85% total

| percentage | object | symbol |
| ---: | :--- | :--- |
| 0.19% | python | list_ass_slice_lock_held |
| 0.10% | python | list_subscript |
| 0.06% | python | list_slice_lock_held.isra.0 |
| 0.05% | python | PyList_Append |
| 0.05% | python | list_iter |
| 0.05% | python | list_sort_impl |
| 0.04% | python | listiter_next |
| 0.04% | python | list_extend_lock_held |
| 0.04% | python | list_append |
| 0.04% | python | list_contains |
| 0.03% | python | list_ass_subscript |
| 0.03% | python | _PyList_AppendTakeRefListResize |
| 0.02% | python | list_concat |
| 0.02% | python | _PyList_FromArraySteal |
| 0.02% | python | list_pop |
| 0.01% | python | list_insert |
| 0.01% | python | list_length |
| 0.01% | python | PyList_SetSlice |
| 0.01% | python | PyList_Size |
| 0.01% | python | list_richcompare |
| 0.01% | python | list_item |

### exceptions

0.58% total

| percentage | object | symbol |
| ---: | :--- | :--- |
| 0.13% | python | _PyErr_SetObject.part.0 |
| 0.07% | python | PyErr_Occurred |
| 0.07% | python | PyErr_CheckSignals |
| 0.07% | python | PyCode_Addr2Line |
| 0.03% | python | PyErr_ExceptionMatches |
| 0.03% | python | PyTraceBack_Here |
| 0.03% | python | _PyErr_Restore |
| 0.02% | python | _PyErr_ExceptionMatches |
| 0.02% | python | BaseException_init |
| 0.01% | python | PyErr_GetRaisedException |
| 0.01% | python | _PyErr_CreateException |
| 0.01% | python | BaseException_clear |
| 0.01% | python | PyException_GetTraceback |
| 0.01% | python | _PyErr_SetKeyError |
| 0.01% | python | PyErr_SetRaisedException |
| 0.01% | python | PyErr_SetObject |
| 0.01% | python | PyErr_GivenExceptionMatches |
| 0.01% | python | AttributeError_init |

### calls

0.57% total

| percentage | object | symbol |
| ---: | :--- | :--- |
| 0.09% | python | _Py_CheckFunctionResult |
| 0.07% | python | _PyFunction_Vectorcall |
| 0.06% | python | vgetargskeywords.constprop.0 |
| 0.06% | python | vgetargs1_impl |
| 0.04% | python | _PyArg_UnpackKeywords |
| 0.03% | python | PyArg_UnpackTuple |
| 0.03% | python | method_vectorcall_FASTCALL_KEYWORDS_METHOD |
| 0.02% | python | cfunction_vectorcall_O |
| 0.02% | python | cfunction_vectorcall_FASTCALL_KEYWORDS |
| 0.02% | python | cfunction_vectorcall_NOARGS |
| 0.01% | python | _PyArg_UnpackKeywordsWithVararg |
| 0.01% | python | cfunction_call |
| 0.01% | python | PyArg_ParseTupleAndKeywords |
| 0.01% | python | method_vectorcall_NOARGS |
| 0.01% | python | method_vectorcall_FASTCALL |
| 0.01% | python | method_vectorcall_VARARGS_KEYWORDS |
| 0.01% | python | method_vectorcall_O |
| 0.01% | python | PyArg_Parse |
| 0.01% | python | vectorcall_method |
| 0.01% | python | PyArg_ParseTuple |
| 0.01% | python | cfunction_vectorcall_FASTCALL_KEYWORDS_METHOD |

### import

0.38% total

| percentage | object | symbol |
| ---: | :--- | :--- |
| 0.31% | python | r_object |
| 0.03% | python | r_string |
| 0.02% | python | PyImport_ImportModuleLevelObject |
| 0.01% | python | r_byte |

### float

0.34% total

| percentage | object | symbol |
| ---: | :--- | :--- |
| 0.16% | python | PyFloat_FromDouble |
| 0.05% | python | float_div |
| 0.03% | python | float_richcompare |
| 0.02% | python | float_pow |
| 0.02% | python | float_sub |
| 0.01% | python | float_mul |
| 0.01% | python | float_rem |
| 0.01% | python | PyFloat_AsDouble.part.0 |
| 0.01% | python | PyFloat_AsDouble |

### gil

0.10% total

| percentage | object | symbol |
| ---: | :--- | :--- |
| 0.08% | python | take_gil |
| 0.02% | python | drop_gil |
