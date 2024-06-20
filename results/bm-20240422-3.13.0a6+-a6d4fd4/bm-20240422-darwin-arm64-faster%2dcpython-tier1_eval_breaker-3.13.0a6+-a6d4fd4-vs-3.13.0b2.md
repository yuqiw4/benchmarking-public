# Results vs. 3.13.0b2

- fork: faster-cpython
- ref: tier1_eval_breaker
- machine: darwin-arm64
- commit hash: a6d4fd4
- commit date: 2024-04-22
- overall geometric mean: 1.03x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x slower
- Memory change: 0.97x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240422-darwin-arm64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:----------------------------------------------------------:|:------------------------------------------------------------------------------:|
| chameleon      | 4.27 ms                                                    | 4.62 ms: 1.08x slower                                                          |
| docutils       | 1.44 sec                                                   | 1.48 sec: 1.03x slower                                                         |
| html5lib       | 31.2 ms                                                    | 32.1 ms: 1.03x slower                                                          |
| tornado_http   | 66.7 ms                                                    | 78.4 ms: 1.18x slower                                                          |
| Geometric mean | (ref)                                                      | 1.06x slower                                                                   |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240422-darwin-arm64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------------------------|:----------------------------------------------------------:|:------------------------------------------------------------------------------:|
| async_tree_eager_cpu_io_mixed_tg | 331 ms                                                     | 336 ms: 1.02x slower                                                           |
| async_tree_eager_cpu_io_mixed    | 358 ms                                                     | 366 ms: 1.02x slower                                                           |
| async_tree_io                    | 563 ms                                                     | 576 ms: 1.02x slower                                                           |
| async_tree_cpu_io_mixed_tg       | 451 ms                                                     | 471 ms: 1.04x slower                                                           |
| async_tree_eager_memoization_tg  | 126 ms                                                     | 131 ms: 1.05x slower                                                           |
| async_tree_eager_tg              | 41.4 ms                                                    | 43.5 ms: 1.05x slower                                                          |
| async_tree_memoization           | 260 ms                                                     | 273 ms: 1.05x slower                                                           |
| async_tree_eager                 | 60.3 ms                                                    | 64.4 ms: 1.07x slower                                                          |
| async_tree_memoization_tg        | 240 ms                                                     | 262 ms: 1.10x slower                                                           |
| Geometric mean                   | (ref)                                                      | 1.03x slower                                                                   |

Benchmark hidden because not significant (7): async_tree_none, async_tree_cpu_io_mixed, async_tree_eager_io_tg, async_tree_io_tg, async_tree_none_tg, async_tree_eager_memoization, async_tree_eager_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240422-darwin-arm64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:----------------------------------------------------------:|:------------------------------------------------------------------------------:|
| float          | 48.6 ms                                                    | 52.2 ms: 1.07x slower                                                          |
| nbody          | 59.6 ms                                                    | 65.7 ms: 1.10x slower                                                          |
| Geometric mean | (ref)                                                      | 1.06x slower                                                                   |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240422-darwin-arm64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:----------------------------------------------------------:|:------------------------------------------------------------------------------:|
| regex_effbot   | 2.58 ms                                                    | 2.59 ms: 1.00x slower                                                          |
| regex_dna      | 149 ms                                                     | 150 ms: 1.00x slower                                                           |
| regex_v8       | 17.3 ms                                                    | 17.5 ms: 1.01x slower                                                          |
| regex_compile  | 68.5 ms                                                    | 70.9 ms: 1.03x slower                                                          |
| Geometric mean | (ref)                                                      | 1.01x slower                                                                   |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240422-darwin-arm64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------------|:----------------------------------------------------------:|:------------------------------------------------------------------------------:|
| xml_etree_parse      | 106 ms                                                     | 99.2 ms: 1.06x faster                                                          |
| xml_etree_iterparse  | 71.5 ms                                                    | 68.5 ms: 1.04x faster                                                          |
| pickle               | 7.48 us                                                    | 7.39 us: 1.01x faster                                                          |
| pickle_dict          | 18.3 us                                                    | 18.3 us: 1.00x slower                                                          |
| unpickle_list        | 2.88 us                                                    | 2.90 us: 1.01x slower                                                          |
| json_loads           | 16.8 us                                                    | 17.0 us: 1.01x slower                                                          |
| unpickle             | 9.12 us                                                    | 9.32 us: 1.02x slower                                                          |
| unpickle_pure_python | 141 us                                                     | 145 us: 1.03x slower                                                           |
| tomli_loads          | 1.47 sec                                                   | 1.51 sec: 1.03x slower                                                         |
| xml_etree_process    | 37.1 ms                                                    | 38.4 ms: 1.04x slower                                                          |
| xml_etree_generate   | 52.7 ms                                                    | 55.1 ms: 1.05x slower                                                          |
| pickle_pure_python   | 179 us                                                     | 188 us: 1.05x slower                                                           |
| Geometric mean       | (ref)                                                      | 1.01x slower                                                                   |

Benchmark hidden because not significant (2): pickle_list, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240422-darwin-arm64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|------------------------|:----------------------------------------------------------:|:------------------------------------------------------------------------------:|
| python_startup_no_site | 12.3 ms                                                    | 9.15 ms: 1.34x faster                                                          |
| python_startup         | 15.2 ms                                                    | 11.9 ms: 1.27x faster                                                          |
| Geometric mean         | (ref)                                                      | 1.31x faster                                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240422-darwin-arm64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|-----------------|:----------------------------------------------------------:|:------------------------------------------------------------------------------:|
| mako            | 6.99 ms                                                    | 7.32 ms: 1.05x slower                                                          |
| genshi_text     | 13.9 ms                                                    | 14.6 ms: 1.05x slower                                                          |
| genshi_xml      | 29.9 ms                                                    | 31.5 ms: 1.05x slower                                                          |
| django_template | 19.4 ms                                                    | 20.6 ms: 1.06x slower                                                          |
| Geometric mean  | (ref)                                                      | 1.05x slower                                                                   |

All benchmarks:
===============

| Benchmark                        | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240422-darwin-arm64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------------------------|:----------------------------------------------------------:|:------------------------------------------------------------------------------:|
| python_startup_no_site           | 12.3 ms                                                    | 9.15 ms: 1.34x faster                                                          |
| python_startup                   | 15.2 ms                                                    | 11.9 ms: 1.27x faster                                                          |
| typing_runtime_protocols         | 87.6 us                                                    | 69.5 us: 1.26x faster                                                          |
| bench_mp_pool                    | 47.2 ms                                                    | 43.0 ms: 1.10x faster                                                          |
| xml_etree_parse                  | 106 ms                                                     | 99.2 ms: 1.06x faster                                                          |
| crypto_pyaes                     | 49.5 ms                                                    | 47.4 ms: 1.04x faster                                                          |
| xml_etree_iterparse              | 71.5 ms                                                    | 68.5 ms: 1.04x faster                                                          |
| pickle                           | 7.48 us                                                    | 7.39 us: 1.01x faster                                                          |
| asyncio_websockets               | 409 ms                                                     | 408 ms: 1.00x faster                                                           |
| regex_effbot                     | 2.58 ms                                                    | 2.59 ms: 1.00x slower                                                          |
| regex_dna                        | 149 ms                                                     | 150 ms: 1.00x slower                                                           |
| pickle_dict                      | 18.3 us                                                    | 18.3 us: 1.00x slower                                                          |
| gc_traversal                     | 2.45 ms                                                    | 2.46 ms: 1.00x slower                                                          |
| sqlite_synth                     | 1.55 us                                                    | 1.56 us: 1.01x slower                                                          |
| unpickle_list                    | 2.88 us                                                    | 2.90 us: 1.01x slower                                                          |
| telco                            | 4.60 ms                                                    | 4.63 ms: 1.01x slower                                                          |
| json_loads                       | 16.8 us                                                    | 17.0 us: 1.01x slower                                                          |
| regex_v8                         | 17.3 ms                                                    | 17.5 ms: 1.01x slower                                                          |
| sympy_integrate                  | 10.3 ms                                                    | 10.5 ms: 1.01x slower                                                          |
| meteor_contest                   | 70.3 ms                                                    | 71.4 ms: 1.02x slower                                                          |
| async_tree_eager_cpu_io_mixed_tg | 331 ms                                                     | 336 ms: 1.02x slower                                                           |
| richards_super                   | 35.2 ms                                                    | 35.8 ms: 1.02x slower                                                          |
| asyncio_tcp_ssl                  | 1.29 sec                                                   | 1.31 sec: 1.02x slower                                                         |
| richards                         | 31.8 ms                                                    | 32.4 ms: 1.02x slower                                                          |
| pathlib                          | 23.3 ms                                                    | 23.7 ms: 1.02x slower                                                          |
| go                               | 101 ms                                                     | 102 ms: 1.02x slower                                                           |
| dulwich_log                      | 27.6 ms                                                    | 28.1 ms: 1.02x slower                                                          |
| thrift                           | 435 us                                                     | 444 us: 1.02x slower                                                           |
| unpickle                         | 9.12 us                                                    | 9.32 us: 1.02x slower                                                          |
| async_tree_eager_cpu_io_mixed    | 358 ms                                                     | 366 ms: 1.02x slower                                                           |
| async_tree_io                    | 563 ms                                                     | 576 ms: 1.02x slower                                                           |
| sympy_expand                     | 226 ms                                                     | 231 ms: 1.02x slower                                                           |
| docutils                         | 1.44 sec                                                   | 1.48 sec: 1.03x slower                                                         |
| html5lib                         | 31.2 ms                                                    | 32.1 ms: 1.03x slower                                                          |
| pyflate                          | 321 ms                                                     | 330 ms: 1.03x slower                                                           |
| unpickle_pure_python             | 141 us                                                     | 145 us: 1.03x slower                                                           |
| async_generators                 | 281 ms                                                     | 290 ms: 1.03x slower                                                           |
| sympy_str                        | 131 ms                                                     | 136 ms: 1.03x slower                                                           |
| tomli_loads                      | 1.47 sec                                                   | 1.51 sec: 1.03x slower                                                         |
| fannkuch                         | 248 ms                                                     | 257 ms: 1.03x slower                                                           |
| pycparser                        | 632 ms                                                     | 654 ms: 1.03x slower                                                           |
| regex_compile                    | 68.5 ms                                                    | 70.9 ms: 1.03x slower                                                          |
| coverage                         | 45.0 ms                                                    | 46.6 ms: 1.04x slower                                                          |
| xml_etree_process                | 37.1 ms                                                    | 38.4 ms: 1.04x slower                                                          |
| sympy_sum                        | 69.2 ms                                                    | 71.7 ms: 1.04x slower                                                          |
| sqlglot_normalize                | 166 ms                                                     | 172 ms: 1.04x slower                                                           |
| sqlglot_optimize                 | 30.9 ms                                                    | 32.1 ms: 1.04x slower                                                          |
| scimark_lu                       | 66.9 ms                                                    | 69.6 ms: 1.04x slower                                                          |
| async_tree_cpu_io_mixed_tg       | 451 ms                                                     | 471 ms: 1.04x slower                                                           |
| pprint_pformat                   | 947 ms                                                     | 989 ms: 1.05x slower                                                           |
| xml_etree_generate               | 52.7 ms                                                    | 55.1 ms: 1.05x slower                                                          |
| sqlglot_transpile                | 891 us                                                     | 932 us: 1.05x slower                                                           |
| async_tree_eager_memoization_tg  | 126 ms                                                     | 131 ms: 1.05x slower                                                           |
| pprint_safe_repr                 | 465 ms                                                     | 487 ms: 1.05x slower                                                           |
| mako                             | 6.99 ms                                                    | 7.32 ms: 1.05x slower                                                          |
| deepcopy_reduce                  | 1.82 us                                                    | 1.91 us: 1.05x slower                                                          |
| logging_format                   | 3.31 us                                                    | 3.48 us: 1.05x slower                                                          |
| async_tree_eager_tg              | 41.4 ms                                                    | 43.5 ms: 1.05x slower                                                          |
| genshi_text                      | 13.9 ms                                                    | 14.6 ms: 1.05x slower                                                          |
| deepcopy                         | 204 us                                                     | 215 us: 1.05x slower                                                           |
| pickle_pure_python               | 179 us                                                     | 188 us: 1.05x slower                                                           |
| async_tree_memoization           | 260 ms                                                     | 273 ms: 1.05x slower                                                           |
| hexiom                           | 4.06 ms                                                    | 4.27 ms: 1.05x slower                                                          |
| logging_simple                   | 3.04 us                                                    | 3.21 us: 1.05x slower                                                          |
| genshi_xml                       | 29.9 ms                                                    | 31.5 ms: 1.05x slower                                                          |
| scimark_sor                      | 94.9 ms                                                    | 100 ms: 1.05x slower                                                           |
| sqlglot_parse                    | 732 us                                                     | 772 us: 1.05x slower                                                           |
| scimark_monte_carlo              | 42.5 ms                                                    | 44.8 ms: 1.06x slower                                                          |
| nqueens                          | 52.2 ms                                                    | 55.2 ms: 1.06x slower                                                          |
| bench_thread_pool                | 447 us                                                     | 473 us: 1.06x slower                                                           |
| django_template                  | 19.4 ms                                                    | 20.6 ms: 1.06x slower                                                          |
| deltablue                        | 2.14 ms                                                    | 2.28 ms: 1.07x slower                                                          |
| asyncio_tcp                      | 402 ms                                                     | 430 ms: 1.07x slower                                                           |
| async_tree_eager                 | 60.3 ms                                                    | 64.4 ms: 1.07x slower                                                          |
| raytrace                         | 147 ms                                                     | 157 ms: 1.07x slower                                                           |
| spectral_norm                    | 66.4 ms                                                    | 71.1 ms: 1.07x slower                                                          |
| deepcopy_memo                    | 22.6 us                                                    | 24.3 us: 1.07x slower                                                          |
| float                            | 48.6 ms                                                    | 52.2 ms: 1.07x slower                                                          |
| aiohttp                          | 997 us                                                     | 1.07 ms: 1.08x slower                                                          |
| scimark_fft                      | 181 ms                                                     | 195 ms: 1.08x slower                                                           |
| chameleon                        | 4.27 ms                                                    | 4.62 ms: 1.08x slower                                                          |
| chaos                            | 34.0 ms                                                    | 36.9 ms: 1.09x slower                                                          |
| scimark_sparse_mat_mult          | 2.77 ms                                                    | 3.02 ms: 1.09x slower                                                          |
| gunicorn                         | 1.04 ms                                                    | 1.13 ms: 1.09x slower                                                          |
| async_tree_memoization_tg        | 240 ms                                                     | 262 ms: 1.10x slower                                                           |
| coroutines                       | 15.8 ms                                                    | 17.4 ms: 1.10x slower                                                          |
| comprehensions                   | 10.2 us                                                    | 11.2 us: 1.10x slower                                                          |
| nbody                            | 59.6 ms                                                    | 65.7 ms: 1.10x slower                                                          |
| logging_silent                   | 60.1 ns                                                    | 66.4 ns: 1.10x slower                                                          |
| tornado_http                     | 66.7 ms                                                    | 78.4 ms: 1.18x slower                                                          |
| generators                       | 22.9 ms                                                    | 27.2 ms: 1.19x slower                                                          |
| Geometric mean                   | (ref)                                                      | 1.03x slower                                                                   |

Benchmark hidden because not significant (17): async_tree_none, dask, pickle_list, json, json_dumps, async_tree_cpu_io_mixed, pidigits, mdp, create_gc_cycles, async_tree_eager_io_tg, 2to3, pylint, async_tree_io_tg, async_tree_none_tg, mypy2, async_tree_eager_memoization, async_tree_eager_io
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.02x

# Memory
- memory change: 0.97x