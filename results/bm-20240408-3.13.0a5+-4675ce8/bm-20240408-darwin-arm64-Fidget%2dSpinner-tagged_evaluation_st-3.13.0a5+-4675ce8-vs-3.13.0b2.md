# Results vs. 3.13.0b2

- fork: Fidget-Spinner
- ref: tagged_evaluation_st
- machine: darwin-arm64
- commit hash: 4675ce8
- commit date: 2024-04-08
- overall geometric mean: 1.02x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x slower
- Memory change: 0.96x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-darwin-arm64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 161 ms                                                     | 162 ms: 1.01x slower                                                             |
| chameleon      | 4.27 ms                                                    | 4.40 ms: 1.03x slower                                                            |
| docutils       | 1.44 sec                                                   | 1.49 sec: 1.04x slower                                                           |
| html5lib       | 31.2 ms                                                    | 33.6 ms: 1.08x slower                                                            |
| tornado_http   | 66.7 ms                                                    | 75.6 ms: 1.13x slower                                                            |
| Geometric mean | (ref)                                                      | 1.06x slower                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-darwin-arm64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none                  | 209 ms                                                     | 202 ms: 1.04x faster                                                             |
| async_tree_eager_cpu_io_mixed_tg | 331 ms                                                     | 334 ms: 1.01x slower                                                             |
| async_tree_eager_cpu_io_mixed    | 358 ms                                                     | 363 ms: 1.01x slower                                                             |
| async_tree_eager                 | 60.3 ms                                                    | 62.9 ms: 1.04x slower                                                            |
| async_tree_eager_tg              | 41.4 ms                                                    | 43.3 ms: 1.05x slower                                                            |
| async_tree_eager_memoization_tg  | 126 ms                                                     | 132 ms: 1.05x slower                                                             |
| async_tree_memoization_tg        | 240 ms                                                     | 259 ms: 1.08x slower                                                             |
| Geometric mean                   | (ref)                                                      | 1.01x slower                                                                     |

Benchmark hidden because not significant (9): async_tree_io_tg, async_tree_cpu_io_mixed, async_tree_none_tg, async_tree_eager_io_tg, async_tree_memoization, async_tree_cpu_io_mixed_tg, async_tree_eager_memoization, async_tree_io, async_tree_eager_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-darwin-arm64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| float          | 48.6 ms                                                    | 51.0 ms: 1.05x slower                                                            |
| nbody          | 59.6 ms                                                    | 65.0 ms: 1.09x slower                                                            |
| Geometric mean | (ref)                                                      | 1.05x slower                                                                     |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-darwin-arm64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_v8       | 17.3 ms                                                    | 17.4 ms: 1.01x slower                                                            |
| regex_compile  | 68.5 ms                                                    | 70.2 ms: 1.02x slower                                                            |
| regex_dna      | 149 ms                                                     | 155 ms: 1.04x slower                                                             |
| regex_effbot   | 2.58 ms                                                    | 2.72 ms: 1.05x slower                                                            |
| Geometric mean | (ref)                                                      | 1.03x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-darwin-arm64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| xml_etree_parse      | 106 ms                                                     | 99.6 ms: 1.06x faster                                                            |
| xml_etree_iterparse  | 71.5 ms                                                    | 68.8 ms: 1.04x faster                                                            |
| pickle_dict          | 18.3 us                                                    | 18.1 us: 1.01x faster                                                            |
| json_loads           | 16.8 us                                                    | 17.0 us: 1.01x slower                                                            |
| xml_etree_process    | 37.1 ms                                                    | 37.4 ms: 1.01x slower                                                            |
| unpickle             | 9.12 us                                                    | 9.30 us: 1.02x slower                                                            |
| pickle_pure_python   | 179 us                                                     | 183 us: 1.02x slower                                                             |
| tomli_loads          | 1.47 sec                                                   | 1.50 sec: 1.03x slower                                                           |
| xml_etree_generate   | 52.7 ms                                                    | 54.2 ms: 1.03x slower                                                            |
| unpickle_pure_python | 141 us                                                     | 146 us: 1.04x slower                                                             |
| unpickle_list        | 2.88 us                                                    | 3.02 us: 1.05x slower                                                            |
| Geometric mean       | (ref)                                                      | 1.01x slower                                                                     |

Benchmark hidden because not significant (3): pickle_list, pickle, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-darwin-arm64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 15.2 ms                                                    | 12.0 ms: 1.26x faster                                                            |
| python_startup_no_site | 12.3 ms                                                    | 10.3 ms: 1.19x faster                                                            |
| Geometric mean         | (ref)                                                      | 1.23x faster                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-darwin-arm64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako           | 6.99 ms                                                    | 7.14 ms: 1.02x slower                                                            |
| genshi_text    | 13.9 ms                                                    | 14.6 ms: 1.05x slower                                                            |
| genshi_xml     | 29.9 ms                                                    | 31.6 ms: 1.06x slower                                                            |
| Geometric mean | (ref)                                                      | 1.04x slower                                                                     |

All benchmarks:
===============

| Benchmark                        | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-darwin-arm64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup                   | 15.2 ms                                                    | 12.0 ms: 1.26x faster                                                            |
| typing_runtime_protocols         | 87.6 us                                                    | 69.4 us: 1.26x faster                                                            |
| python_startup_no_site           | 12.3 ms                                                    | 10.3 ms: 1.19x faster                                                            |
| pylint                           | 170 ms                                                     | 144 ms: 1.18x faster                                                             |
| bench_mp_pool                    | 47.2 ms                                                    | 42.8 ms: 1.10x faster                                                            |
| crypto_pyaes                     | 49.5 ms                                                    | 46.3 ms: 1.07x faster                                                            |
| xml_etree_parse                  | 106 ms                                                     | 99.6 ms: 1.06x faster                                                            |
| xml_etree_iterparse              | 71.5 ms                                                    | 68.8 ms: 1.04x faster                                                            |
| richards                         | 31.8 ms                                                    | 30.6 ms: 1.04x faster                                                            |
| async_tree_none                  | 209 ms                                                     | 202 ms: 1.04x faster                                                             |
| richards_super                   | 35.2 ms                                                    | 34.5 ms: 1.02x faster                                                            |
| create_gc_cycles                 | 897 us                                                     | 885 us: 1.01x faster                                                             |
| pickle_dict                      | 18.3 us                                                    | 18.1 us: 1.01x faster                                                            |
| gc_traversal                     | 2.45 ms                                                    | 2.44 ms: 1.00x faster                                                            |
| asyncio_websockets               | 409 ms                                                     | 408 ms: 1.00x faster                                                             |
| sqlite_synth                     | 1.55 us                                                    | 1.56 us: 1.00x slower                                                            |
| comprehensions                   | 10.2 us                                                    | 10.2 us: 1.01x slower                                                            |
| 2to3                             | 161 ms                                                     | 162 ms: 1.01x slower                                                             |
| regex_v8                         | 17.3 ms                                                    | 17.4 ms: 1.01x slower                                                            |
| json_loads                       | 16.8 us                                                    | 17.0 us: 1.01x slower                                                            |
| telco                            | 4.60 ms                                                    | 4.65 ms: 1.01x slower                                                            |
| xml_etree_process                | 37.1 ms                                                    | 37.4 ms: 1.01x slower                                                            |
| sympy_integrate                  | 10.3 ms                                                    | 10.5 ms: 1.01x slower                                                            |
| async_tree_eager_cpu_io_mixed_tg | 331 ms                                                     | 334 ms: 1.01x slower                                                             |
| pyflate                          | 321 ms                                                     | 325 ms: 1.01x slower                                                             |
| async_tree_eager_cpu_io_mixed    | 358 ms                                                     | 363 ms: 1.01x slower                                                             |
| thrift                           | 435 us                                                     | 442 us: 1.02x slower                                                             |
| sympy_expand                     | 226 ms                                                     | 230 ms: 1.02x slower                                                             |
| pycparser                        | 632 ms                                                     | 644 ms: 1.02x slower                                                             |
| sqlglot_transpile                | 891 us                                                     | 907 us: 1.02x slower                                                             |
| meteor_contest                   | 70.3 ms                                                    | 71.7 ms: 1.02x slower                                                            |
| unpickle                         | 9.12 us                                                    | 9.30 us: 1.02x slower                                                            |
| sqlglot_parse                    | 732 us                                                     | 747 us: 1.02x slower                                                             |
| mako                             | 6.99 ms                                                    | 7.14 ms: 1.02x slower                                                            |
| async_generators                 | 281 ms                                                     | 287 ms: 1.02x slower                                                             |
| dulwich_log                      | 27.6 ms                                                    | 28.2 ms: 1.02x slower                                                            |
| scimark_lu                       | 66.9 ms                                                    | 68.5 ms: 1.02x slower                                                            |
| pickle_pure_python               | 179 us                                                     | 183 us: 1.02x slower                                                             |
| regex_compile                    | 68.5 ms                                                    | 70.2 ms: 1.02x slower                                                            |
| sympy_sum                        | 69.2 ms                                                    | 71.0 ms: 1.03x slower                                                            |
| tomli_loads                      | 1.47 sec                                                   | 1.50 sec: 1.03x slower                                                           |
| deltablue                        | 2.14 ms                                                    | 2.20 ms: 1.03x slower                                                            |
| deepcopy                         | 204 us                                                     | 209 us: 1.03x slower                                                             |
| sympy_str                        | 131 ms                                                     | 135 ms: 1.03x slower                                                             |
| xml_etree_generate               | 52.7 ms                                                    | 54.2 ms: 1.03x slower                                                            |
| chameleon                        | 4.27 ms                                                    | 4.40 ms: 1.03x slower                                                            |
| coverage                         | 45.0 ms                                                    | 46.4 ms: 1.03x slower                                                            |
| sqlglot_normalize                | 166 ms                                                     | 171 ms: 1.03x slower                                                             |
| deepcopy_reduce                  | 1.82 us                                                    | 1.88 us: 1.03x slower                                                            |
| sqlglot_optimize                 | 30.9 ms                                                    | 31.9 ms: 1.03x slower                                                            |
| logging_format                   | 3.31 us                                                    | 3.42 us: 1.03x slower                                                            |
| hexiom                           | 4.06 ms                                                    | 4.20 ms: 1.04x slower                                                            |
| docutils                         | 1.44 sec                                                   | 1.49 sec: 1.04x slower                                                           |
| logging_simple                   | 3.04 us                                                    | 3.16 us: 1.04x slower                                                            |
| pprint_pformat                   | 947 ms                                                     | 983 ms: 1.04x slower                                                             |
| unpickle_pure_python             | 141 us                                                     | 146 us: 1.04x slower                                                             |
| scimark_monte_carlo              | 42.5 ms                                                    | 44.1 ms: 1.04x slower                                                            |
| regex_dna                        | 149 ms                                                     | 155 ms: 1.04x slower                                                             |
| pprint_safe_repr                 | 465 ms                                                     | 483 ms: 1.04x slower                                                             |
| raytrace                         | 147 ms                                                     | 153 ms: 1.04x slower                                                             |
| async_tree_eager                 | 60.3 ms                                                    | 62.9 ms: 1.04x slower                                                            |
| scimark_sor                      | 94.9 ms                                                    | 99.2 ms: 1.05x slower                                                            |
| fannkuch                         | 248 ms                                                     | 260 ms: 1.05x slower                                                             |
| unpickle_list                    | 2.88 us                                                    | 3.02 us: 1.05x slower                                                            |
| async_tree_eager_tg              | 41.4 ms                                                    | 43.3 ms: 1.05x slower                                                            |
| deepcopy_memo                    | 22.6 us                                                    | 23.7 us: 1.05x slower                                                            |
| float                            | 48.6 ms                                                    | 51.0 ms: 1.05x slower                                                            |
| genshi_text                      | 13.9 ms                                                    | 14.6 ms: 1.05x slower                                                            |
| async_tree_eager_memoization_tg  | 126 ms                                                     | 132 ms: 1.05x slower                                                             |
| regex_effbot                     | 2.58 ms                                                    | 2.72 ms: 1.05x slower                                                            |
| bench_thread_pool                | 447 us                                                     | 471 us: 1.05x slower                                                             |
| genshi_xml                       | 29.9 ms                                                    | 31.6 ms: 1.06x slower                                                            |
| chaos                            | 34.0 ms                                                    | 35.9 ms: 1.06x slower                                                            |
| pathlib                          | 23.3 ms                                                    | 24.8 ms: 1.06x slower                                                            |
| logging_silent                   | 60.1 ns                                                    | 64.3 ns: 1.07x slower                                                            |
| nqueens                          | 52.2 ms                                                    | 56.0 ms: 1.07x slower                                                            |
| spectral_norm                    | 66.4 ms                                                    | 71.2 ms: 1.07x slower                                                            |
| coroutines                       | 15.8 ms                                                    | 17.0 ms: 1.07x slower                                                            |
| html5lib                         | 31.2 ms                                                    | 33.6 ms: 1.08x slower                                                            |
| scimark_sparse_mat_mult          | 2.77 ms                                                    | 3.00 ms: 1.08x slower                                                            |
| scimark_fft                      | 181 ms                                                     | 195 ms: 1.08x slower                                                             |
| async_tree_memoization_tg        | 240 ms                                                     | 259 ms: 1.08x slower                                                             |
| nbody                            | 59.6 ms                                                    | 65.0 ms: 1.09x slower                                                            |
| aiohttp                          | 997 us                                                     | 1.10 ms: 1.10x slower                                                            |
| gunicorn                         | 1.04 ms                                                    | 1.16 ms: 1.12x slower                                                            |
| tornado_http                     | 66.7 ms                                                    | 75.6 ms: 1.13x slower                                                            |
| generators                       | 22.9 ms                                                    | 27.4 ms: 1.20x slower                                                            |
| Geometric mean                   | (ref)                                                      | 1.02x slower                                                                     |

Benchmark hidden because not significant (20): async_tree_io_tg, dask, async_tree_cpu_io_mixed, async_tree_none_tg, async_tree_eager_io_tg, pickle_list, mdp, pickle, pidigits, go, async_tree_memoization, async_tree_cpu_io_mixed_tg, json_dumps, mypy2, async_tree_eager_memoization, async_tree_io, json, asyncio_tcp_ssl, async_tree_eager_io, asyncio_tcp
Ignored benchmarks (3) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, django_template, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 0.96x