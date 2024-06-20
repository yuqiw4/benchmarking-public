# Results vs. 3.13.0b2

- fork: savannahostrowski
- ref: llvm_18
- machine: darwin-arm64
- commit hash: b2bbeb0
- commit date: 2024-04-27
- overall geometric mean: 1.03x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-darwin-arm64-savannahostrowski-llvm_18-3.13.0a6+-b2bbeb0 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 161 ms                                                     | 183 ms: 1.14x slower                                                 |
| chameleon      | 4.27 ms                                                    | 4.45 ms: 1.04x slower                                                |
| docutils       | 1.44 sec                                                   | 1.50 sec: 1.04x slower                                               |
| html5lib       | 31.2 ms                                                    | 30.7 ms: 1.01x faster                                                |
| tornado_http   | 66.7 ms                                                    | 71.5 ms: 1.07x slower                                                |
| Geometric mean | (ref)                                                      | 1.06x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-darwin-arm64-savannahostrowski-llvm_18-3.13.0a6+-b2bbeb0 |
|----------------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_none                  | 209 ms                                                     | 198 ms: 1.06x faster                                                 |
| async_tree_eager_io_tg           | 768 ms                                                     | 732 ms: 1.05x faster                                                 |
| async_tree_cpu_io_mixed          | 467 ms                                                     | 457 ms: 1.02x faster                                                 |
| async_tree_eager_cpu_io_mixed_tg | 331 ms                                                     | 334 ms: 1.01x slower                                                 |
| async_tree_eager_cpu_io_mixed    | 358 ms                                                     | 363 ms: 1.01x slower                                                 |
| async_tree_cpu_io_mixed_tg       | 451 ms                                                     | 463 ms: 1.03x slower                                                 |
| async_tree_eager_tg              | 41.4 ms                                                    | 42.9 ms: 1.04x slower                                                |
| async_tree_eager_memoization_tg  | 126 ms                                                     | 130 ms: 1.04x slower                                                 |
| async_tree_eager                 | 60.3 ms                                                    | 64.6 ms: 1.07x slower                                                |
| async_tree_memoization_tg        | 240 ms                                                     | 259 ms: 1.08x slower                                                 |
| Geometric mean                   | (ref)                                                      | 1.01x slower                                                         |

Benchmark hidden because not significant (6): async_tree_eager_io, async_tree_io_tg, async_tree_none_tg, async_tree_io, async_tree_eager_memoization, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-darwin-arm64-savannahostrowski-llvm_18-3.13.0a6+-b2bbeb0 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 48.6 ms                                                    | 50.7 ms: 1.04x slower                                                |
| nbody          | 59.6 ms                                                    | 67.9 ms: 1.14x slower                                                |
| Geometric mean | (ref)                                                      | 1.06x slower                                                         |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-darwin-arm64-savannahostrowski-llvm_18-3.13.0a6+-b2bbeb0 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_dna      | 149 ms                                                     | 149 ms: 1.00x slower                                                 |
| regex_v8       | 17.3 ms                                                    | 17.4 ms: 1.00x slower                                                |
| regex_compile  | 68.5 ms                                                    | 72.1 ms: 1.05x slower                                                |
| Geometric mean | (ref)                                                      | 1.01x slower                                                         |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-darwin-arm64-savannahostrowski-llvm_18-3.13.0a6+-b2bbeb0 |
|----------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------:|
| tomli_loads          | 1.47 sec                                                   | 1.23 sec: 1.19x faster                                               |
| unpickle_pure_python | 141 us                                                     | 132 us: 1.07x faster                                                 |
| xml_etree_parse      | 106 ms                                                     | 104 ms: 1.02x faster                                                 |
| xml_etree_process    | 37.1 ms                                                    | 36.5 ms: 1.02x faster                                                |
| xml_etree_iterparse  | 71.5 ms                                                    | 70.7 ms: 1.01x faster                                                |
| pickle_dict          | 18.3 us                                                    | 18.2 us: 1.01x faster                                                |
| pickle_list          | 2.96 us                                                    | 2.98 us: 1.01x slower                                                |
| unpickle_list        | 2.88 us                                                    | 2.91 us: 1.01x slower                                                |
| json_loads           | 16.8 us                                                    | 17.0 us: 1.01x slower                                                |
| json_dumps           | 6.23 ms                                                    | 6.31 ms: 1.01x slower                                                |
| xml_etree_generate   | 52.7 ms                                                    | 53.6 ms: 1.02x slower                                                |
| unpickle             | 9.12 us                                                    | 9.29 us: 1.02x slower                                                |
| pickle_pure_python   | 179 us                                                     | 182 us: 1.02x slower                                                 |
| Geometric mean       | (ref)                                                      | 1.01x faster                                                         |

Benchmark hidden because not significant (1): pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-darwin-arm64-savannahostrowski-llvm_18-3.13.0a6+-b2bbeb0 |
|------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 12.3 ms                                                    | 11.1 ms: 1.10x faster                                                |
| python_startup         | 15.2 ms                                                    | 14.1 ms: 1.07x faster                                                |
| Geometric mean         | (ref)                                                      | 1.09x faster                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-darwin-arm64-savannahostrowski-llvm_18-3.13.0a6+-b2bbeb0 |
|-----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------:|
| mako            | 6.99 ms                                                    | 6.40 ms: 1.09x faster                                                |
| django_template | 19.4 ms                                                    | 20.8 ms: 1.07x slower                                                |
| genshi_text     | 13.9 ms                                                    | 15.6 ms: 1.12x slower                                                |
| genshi_xml      | 29.9 ms                                                    | 35.9 ms: 1.20x slower                                                |
| Geometric mean  | (ref)                                                      | 1.07x slower                                                         |

All benchmarks:
===============

| Benchmark                        | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-darwin-arm64-savannahostrowski-llvm_18-3.13.0a6+-b2bbeb0 |
|----------------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------:|
| tomli_loads                      | 1.47 sec                                                   | 1.23 sec: 1.19x faster                                               |
| python_startup_no_site           | 12.3 ms                                                    | 11.1 ms: 1.10x faster                                                |
| mako                             | 6.99 ms                                                    | 6.40 ms: 1.09x faster                                                |
| python_startup                   | 15.2 ms                                                    | 14.1 ms: 1.07x faster                                                |
| unpickle_pure_python             | 141 us                                                     | 132 us: 1.07x faster                                                 |
| richards                         | 31.8 ms                                                    | 29.8 ms: 1.07x faster                                                |
| async_tree_none                  | 209 ms                                                     | 198 ms: 1.06x faster                                                 |
| fannkuch                         | 248 ms                                                     | 236 ms: 1.05x faster                                                 |
| async_tree_eager_io_tg           | 768 ms                                                     | 732 ms: 1.05x faster                                                 |
| richards_super                   | 35.2 ms                                                    | 33.8 ms: 1.04x faster                                                |
| telco                            | 4.60 ms                                                    | 4.46 ms: 1.03x faster                                                |
| async_tree_cpu_io_mixed          | 467 ms                                                     | 457 ms: 1.02x faster                                                 |
| bench_mp_pool                    | 47.2 ms                                                    | 46.2 ms: 1.02x faster                                                |
| xml_etree_parse                  | 106 ms                                                     | 104 ms: 1.02x faster                                                 |
| xml_etree_process                | 37.1 ms                                                    | 36.5 ms: 1.02x faster                                                |
| html5lib                         | 31.2 ms                                                    | 30.7 ms: 1.01x faster                                                |
| pyflate                          | 321 ms                                                     | 317 ms: 1.01x faster                                                 |
| crypto_pyaes                     | 49.5 ms                                                    | 48.9 ms: 1.01x faster                                                |
| xml_etree_iterparse              | 71.5 ms                                                    | 70.7 ms: 1.01x faster                                                |
| mdp                              | 1.53 sec                                                   | 1.52 sec: 1.01x faster                                               |
| json                             | 2.93 ms                                                    | 2.91 ms: 1.01x faster                                                |
| pickle_dict                      | 18.3 us                                                    | 18.2 us: 1.01x faster                                                |
| asyncio_websockets               | 409 ms                                                     | 408 ms: 1.00x faster                                                 |
| regex_dna                        | 149 ms                                                     | 149 ms: 1.00x slower                                                 |
| gc_traversal                     | 2.45 ms                                                    | 2.46 ms: 1.00x slower                                                |
| regex_v8                         | 17.3 ms                                                    | 17.4 ms: 1.00x slower                                                |
| pickle_list                      | 2.96 us                                                    | 2.98 us: 1.01x slower                                                |
| coverage                         | 45.0 ms                                                    | 45.3 ms: 1.01x slower                                                |
| thrift                           | 435 us                                                     | 439 us: 1.01x slower                                                 |
| async_tree_eager_cpu_io_mixed_tg | 331 ms                                                     | 334 ms: 1.01x slower                                                 |
| unpickle_list                    | 2.88 us                                                    | 2.91 us: 1.01x slower                                                |
| sqlite_synth                     | 1.55 us                                                    | 1.57 us: 1.01x slower                                                |
| json_loads                       | 16.8 us                                                    | 17.0 us: 1.01x slower                                                |
| create_gc_cycles                 | 897 us                                                     | 908 us: 1.01x slower                                                 |
| json_dumps                       | 6.23 ms                                                    | 6.31 ms: 1.01x slower                                                |
| async_tree_eager_cpu_io_mixed    | 358 ms                                                     | 363 ms: 1.01x slower                                                 |
| pycparser                        | 632 ms                                                     | 642 ms: 1.02x slower                                                 |
| xml_etree_generate               | 52.7 ms                                                    | 53.6 ms: 1.02x slower                                                |
| unpickle                         | 9.12 us                                                    | 9.29 us: 1.02x slower                                                |
| deepcopy_reduce                  | 1.82 us                                                    | 1.86 us: 1.02x slower                                                |
| pickle_pure_python               | 179 us                                                     | 182 us: 1.02x slower                                                 |
| asyncio_tcp_ssl                  | 1.29 sec                                                   | 1.32 sec: 1.02x slower                                               |
| logging_format                   | 3.31 us                                                    | 3.38 us: 1.02x slower                                                |
| pprint_safe_repr                 | 465 ms                                                     | 475 ms: 1.02x slower                                                 |
| logging_simple                   | 3.04 us                                                    | 3.12 us: 1.02x slower                                                |
| async_tree_cpu_io_mixed_tg       | 451 ms                                                     | 463 ms: 1.03x slower                                                 |
| coroutines                       | 15.8 ms                                                    | 16.3 ms: 1.03x slower                                                |
| sympy_expand                     | 226 ms                                                     | 233 ms: 1.03x slower                                                 |
| meteor_contest                   | 70.3 ms                                                    | 72.8 ms: 1.04x slower                                                |
| pprint_pformat                   | 947 ms                                                     | 980 ms: 1.04x slower                                                 |
| go                               | 101 ms                                                     | 104 ms: 1.04x slower                                                 |
| sympy_str                        | 131 ms                                                     | 136 ms: 1.04x slower                                                 |
| async_tree_eager_tg              | 41.4 ms                                                    | 42.9 ms: 1.04x slower                                                |
| async_tree_eager_memoization_tg  | 126 ms                                                     | 130 ms: 1.04x slower                                                 |
| docutils                         | 1.44 sec                                                   | 1.50 sec: 1.04x slower                                               |
| float                            | 48.6 ms                                                    | 50.7 ms: 1.04x slower                                                |
| chameleon                        | 4.27 ms                                                    | 4.45 ms: 1.04x slower                                                |
| deepcopy                         | 204 us                                                     | 213 us: 1.05x slower                                                 |
| dulwich_log                      | 27.6 ms                                                    | 28.8 ms: 1.05x slower                                                |
| async_generators                 | 281 ms                                                     | 294 ms: 1.05x slower                                                 |
| sympy_integrate                  | 10.3 ms                                                    | 10.9 ms: 1.05x slower                                                |
| scimark_monte_carlo              | 42.5 ms                                                    | 44.7 ms: 1.05x slower                                                |
| regex_compile                    | 68.5 ms                                                    | 72.1 ms: 1.05x slower                                                |
| sympy_sum                        | 69.2 ms                                                    | 72.8 ms: 1.05x slower                                                |
| sqlglot_parse                    | 732 us                                                     | 772 us: 1.06x slower                                                 |
| sqlglot_transpile                | 891 us                                                     | 942 us: 1.06x slower                                                 |
| spectral_norm                    | 66.4 ms                                                    | 70.3 ms: 1.06x slower                                                |
| sqlglot_normalize                | 166 ms                                                     | 176 ms: 1.06x slower                                                 |
| scimark_fft                      | 181 ms                                                     | 192 ms: 1.07x slower                                                 |
| logging_silent                   | 60.1 ns                                                    | 64.2 ns: 1.07x slower                                                |
| deepcopy_memo                    | 22.6 us                                                    | 24.1 us: 1.07x slower                                                |
| django_template                  | 19.4 ms                                                    | 20.8 ms: 1.07x slower                                                |
| async_tree_eager                 | 60.3 ms                                                    | 64.6 ms: 1.07x slower                                                |
| tornado_http                     | 66.7 ms                                                    | 71.5 ms: 1.07x slower                                                |
| asyncio_tcp                      | 402 ms                                                     | 431 ms: 1.07x slower                                                 |
| sqlglot_optimize                 | 30.9 ms                                                    | 33.3 ms: 1.08x slower                                                |
| async_tree_memoization_tg        | 240 ms                                                     | 259 ms: 1.08x slower                                                 |
| bench_thread_pool                | 447 us                                                     | 487 us: 1.09x slower                                                 |
| aiohttp                          | 997 us                                                     | 1.09 ms: 1.09x slower                                                |
| scimark_sparse_mat_mult          | 2.77 ms                                                    | 3.03 ms: 1.09x slower                                                |
| scimark_sor                      | 94.9 ms                                                    | 104 ms: 1.10x slower                                                 |
| hexiom                           | 4.06 ms                                                    | 4.48 ms: 1.10x slower                                                |
| gunicorn                         | 1.04 ms                                                    | 1.16 ms: 1.12x slower                                                |
| nqueens                          | 52.2 ms                                                    | 58.3 ms: 1.12x slower                                                |
| genshi_text                      | 13.9 ms                                                    | 15.6 ms: 1.12x slower                                                |
| deltablue                        | 2.14 ms                                                    | 2.43 ms: 1.14x slower                                                |
| nbody                            | 59.6 ms                                                    | 67.9 ms: 1.14x slower                                                |
| 2to3                             | 161 ms                                                     | 183 ms: 1.14x slower                                                 |
| raytrace                         | 147 ms                                                     | 169 ms: 1.15x slower                                                 |
| generators                       | 22.9 ms                                                    | 26.9 ms: 1.18x slower                                                |
| typing_runtime_protocols         | 87.6 us                                                    | 103 us: 1.18x slower                                                 |
| chaos                            | 34.0 ms                                                    | 40.4 ms: 1.19x slower                                                |
| scimark_lu                       | 66.9 ms                                                    | 80.0 ms: 1.20x slower                                                |
| genshi_xml                       | 29.9 ms                                                    | 35.9 ms: 1.20x slower                                                |
| comprehensions                   | 10.2 us                                                    | 12.6 us: 1.24x slower                                                |
| mypy2                            | 379 ms                                                     | 487 ms: 1.28x slower                                                 |
| Geometric mean                   | (ref)                                                      | 1.03x slower                                                         |

Benchmark hidden because not significant (12): async_tree_eager_io, async_tree_io_tg, async_tree_none_tg, async_tree_io, pathlib, dask, regex_effbot, pickle, pidigits, async_tree_eager_memoization, async_tree_memoization, pylint
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.18x