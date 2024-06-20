# Results vs. 3.13.0b2

- fork: faster-cpython
- ref: tier_2_call
- machine: darwin-arm64
- commit hash: 65aa34a
- commit date: 2024-04-26
- overall geometric mean: 1.02x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x slower
- Memory change: 0.96x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-darwin-arm64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------:|
| chameleon      | 4.27 ms                                                    | 4.45 ms: 1.04x slower                                                   |
| docutils       | 1.44 sec                                                   | 1.45 sec: 1.01x slower                                                  |
| html5lib       | 31.2 ms                                                    | 31.7 ms: 1.02x slower                                                   |
| tornado_http   | 66.7 ms                                                    | 74.1 ms: 1.11x slower                                                   |
| Geometric mean | (ref)                                                      | 1.04x slower                                                            |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-darwin-arm64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_none                  | 209 ms                                                     | 202 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 331 ms                                                     | 333 ms: 1.01x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 358 ms                                                     | 362 ms: 1.01x slower                                                    |
| async_tree_eager                 | 60.3 ms                                                    | 61.7 ms: 1.02x slower                                                   |
| async_tree_eager_tg              | 41.4 ms                                                    | 42.4 ms: 1.03x slower                                                   |
| async_tree_cpu_io_mixed_tg       | 451 ms                                                     | 468 ms: 1.04x slower                                                    |
| async_tree_eager_memoization_tg  | 126 ms                                                     | 131 ms: 1.04x slower                                                    |
| async_tree_memoization_tg        | 240 ms                                                     | 261 ms: 1.09x slower                                                    |
| Geometric mean                   | (ref)                                                      | 1.01x slower                                                            |

Benchmark hidden because not significant (8): async_tree_eager_io_tg, async_tree_cpu_io_mixed, async_tree_eager_memoization, async_tree_io_tg, async_tree_none_tg, async_tree_io, async_tree_eager_io, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-darwin-arm64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 282 ms                                                     | 282 ms: 1.00x faster                                                    |
| float          | 48.6 ms                                                    | 51.1 ms: 1.05x slower                                                   |
| nbody          | 59.6 ms                                                    | 69.9 ms: 1.17x slower                                                   |
| Geometric mean | (ref)                                                      | 1.07x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-darwin-arm64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 17.3 ms                                                    | 17.4 ms: 1.01x slower                                                   |
| regex_compile  | 68.5 ms                                                    | 69.1 ms: 1.01x slower                                                   |
| regex_effbot   | 2.58 ms                                                    | 2.62 ms: 1.01x slower                                                   |
| regex_dna      | 149 ms                                                     | 153 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                      | 1.01x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-darwin-arm64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_parse      | 106 ms                                                     | 104 ms: 1.02x faster                                                    |
| pickle_dict          | 18.3 us                                                    | 18.1 us: 1.01x faster                                                   |
| json_dumps           | 6.23 ms                                                    | 6.19 ms: 1.01x faster                                                   |
| unpickle_pure_python | 141 us                                                     | 141 us: 1.01x slower                                                    |
| json_loads           | 16.8 us                                                    | 16.9 us: 1.01x slower                                                   |
| pickle_pure_python   | 179 us                                                     | 180 us: 1.01x slower                                                    |
| xml_etree_iterparse  | 71.5 ms                                                    | 72.5 ms: 1.01x slower                                                   |
| unpickle             | 9.12 us                                                    | 9.28 us: 1.02x slower                                                   |
| xml_etree_process    | 37.1 ms                                                    | 37.8 ms: 1.02x slower                                                   |
| tomli_loads          | 1.47 sec                                                   | 1.51 sec: 1.03x slower                                                  |
| xml_etree_generate   | 52.7 ms                                                    | 54.5 ms: 1.03x slower                                                   |
| unpickle_list        | 2.88 us                                                    | 2.98 us: 1.03x slower                                                   |
| Geometric mean       | (ref)                                                      | 1.01x slower                                                            |

Benchmark hidden because not significant (2): pickle, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-darwin-arm64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|------------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 12.3 ms                                                    | 10.2 ms: 1.21x faster                                                   |
| python_startup         | 15.2 ms                                                    | 13.0 ms: 1.17x faster                                                   |
| Geometric mean         | (ref)                                                      | 1.19x faster                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-darwin-arm64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|-----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 6.99 ms                                                    | 7.12 ms: 1.02x slower                                                   |
| django_template | 19.4 ms                                                    | 20.1 ms: 1.03x slower                                                   |
| genshi_text     | 13.9 ms                                                    | 14.5 ms: 1.05x slower                                                   |
| genshi_xml      | 29.9 ms                                                    | 31.5 ms: 1.05x slower                                                   |
| Geometric mean  | (ref)                                                      | 1.04x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-darwin-arm64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site           | 12.3 ms                                                    | 10.2 ms: 1.21x faster                                                   |
| python_startup                   | 15.2 ms                                                    | 13.0 ms: 1.17x faster                                                   |
| bench_mp_pool                    | 47.2 ms                                                    | 43.5 ms: 1.09x faster                                                   |
| crypto_pyaes                     | 49.5 ms                                                    | 46.7 ms: 1.06x faster                                                   |
| async_tree_none                  | 209 ms                                                     | 202 ms: 1.04x faster                                                    |
| telco                            | 4.60 ms                                                    | 4.46 ms: 1.03x faster                                                   |
| xml_etree_parse                  | 106 ms                                                     | 104 ms: 1.02x faster                                                    |
| richards_super                   | 35.2 ms                                                    | 34.8 ms: 1.01x faster                                                   |
| pickle_dict                      | 18.3 us                                                    | 18.1 us: 1.01x faster                                                   |
| json_dumps                       | 6.23 ms                                                    | 6.19 ms: 1.01x faster                                                   |
| gc_traversal                     | 2.45 ms                                                    | 2.44 ms: 1.00x faster                                                   |
| create_gc_cycles                 | 897 us                                                     | 895 us: 1.00x faster                                                    |
| pidigits                         | 282 ms                                                     | 282 ms: 1.00x faster                                                    |
| sympy_integrate                  | 10.3 ms                                                    | 10.4 ms: 1.00x slower                                                   |
| go                               | 101 ms                                                     | 101 ms: 1.00x slower                                                    |
| unpickle_pure_python             | 141 us                                                     | 141 us: 1.01x slower                                                    |
| json_loads                       | 16.8 us                                                    | 16.9 us: 1.01x slower                                                   |
| regex_v8                         | 17.3 ms                                                    | 17.4 ms: 1.01x slower                                                   |
| pyflate                          | 321 ms                                                     | 323 ms: 1.01x slower                                                    |
| regex_compile                    | 68.5 ms                                                    | 69.1 ms: 1.01x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 331 ms                                                     | 333 ms: 1.01x slower                                                    |
| docutils                         | 1.44 sec                                                   | 1.45 sec: 1.01x slower                                                  |
| async_tree_eager_cpu_io_mixed    | 358 ms                                                     | 362 ms: 1.01x slower                                                    |
| pickle_pure_python               | 179 us                                                     | 180 us: 1.01x slower                                                    |
| pprint_safe_repr                 | 465 ms                                                     | 470 ms: 1.01x slower                                                    |
| pprint_pformat                   | 947 ms                                                     | 958 ms: 1.01x slower                                                    |
| xml_etree_iterparse              | 71.5 ms                                                    | 72.5 ms: 1.01x slower                                                   |
| regex_effbot                     | 2.58 ms                                                    | 2.62 ms: 1.01x slower                                                   |
| meteor_contest                   | 70.3 ms                                                    | 71.3 ms: 1.01x slower                                                   |
| async_generators                 | 281 ms                                                     | 285 ms: 1.02x slower                                                    |
| sqlglot_transpile                | 891 us                                                     | 906 us: 1.02x slower                                                    |
| unpickle                         | 9.12 us                                                    | 9.28 us: 1.02x slower                                                   |
| html5lib                         | 31.2 ms                                                    | 31.7 ms: 1.02x slower                                                   |
| mako                             | 6.99 ms                                                    | 7.12 ms: 1.02x slower                                                   |
| sympy_str                        | 131 ms                                                     | 134 ms: 1.02x slower                                                    |
| asyncio_tcp_ssl                  | 1.29 sec                                                   | 1.32 sec: 1.02x slower                                                  |
| xml_etree_process                | 37.1 ms                                                    | 37.8 ms: 1.02x slower                                                   |
| sqlglot_normalize                | 166 ms                                                     | 169 ms: 1.02x slower                                                    |
| sympy_sum                        | 69.2 ms                                                    | 70.7 ms: 1.02x slower                                                   |
| sqlglot_parse                    | 732 us                                                     | 747 us: 1.02x slower                                                    |
| sqlglot_optimize                 | 30.9 ms                                                    | 31.6 ms: 1.02x slower                                                   |
| sympy_expand                     | 226 ms                                                     | 231 ms: 1.02x slower                                                    |
| scimark_lu                       | 66.9 ms                                                    | 68.4 ms: 1.02x slower                                                   |
| deltablue                        | 2.14 ms                                                    | 2.19 ms: 1.02x slower                                                   |
| async_tree_eager                 | 60.3 ms                                                    | 61.7 ms: 1.02x slower                                                   |
| deepcopy                         | 204 us                                                     | 209 us: 1.03x slower                                                    |
| async_tree_eager_tg              | 41.4 ms                                                    | 42.4 ms: 1.03x slower                                                   |
| regex_dna                        | 149 ms                                                     | 153 ms: 1.03x slower                                                    |
| coverage                         | 45.0 ms                                                    | 46.2 ms: 1.03x slower                                                   |
| thrift                           | 435 us                                                     | 448 us: 1.03x slower                                                    |
| deepcopy_memo                    | 22.6 us                                                    | 23.2 us: 1.03x slower                                                   |
| pathlib                          | 23.3 ms                                                    | 24.0 ms: 1.03x slower                                                   |
| fannkuch                         | 248 ms                                                     | 256 ms: 1.03x slower                                                    |
| tomli_loads                      | 1.47 sec                                                   | 1.51 sec: 1.03x slower                                                  |
| django_template                  | 19.4 ms                                                    | 20.1 ms: 1.03x slower                                                   |
| xml_etree_generate               | 52.7 ms                                                    | 54.5 ms: 1.03x slower                                                   |
| comprehensions                   | 10.2 us                                                    | 10.5 us: 1.03x slower                                                   |
| unpickle_list                    | 2.88 us                                                    | 2.98 us: 1.03x slower                                                   |
| deepcopy_reduce                  | 1.82 us                                                    | 1.89 us: 1.04x slower                                                   |
| logging_silent                   | 60.1 ns                                                    | 62.3 ns: 1.04x slower                                                   |
| scimark_sor                      | 94.9 ms                                                    | 98.5 ms: 1.04x slower                                                   |
| async_tree_cpu_io_mixed_tg       | 451 ms                                                     | 468 ms: 1.04x slower                                                    |
| hexiom                           | 4.06 ms                                                    | 4.22 ms: 1.04x slower                                                   |
| async_tree_eager_memoization_tg  | 126 ms                                                     | 131 ms: 1.04x slower                                                    |
| logging_simple                   | 3.04 us                                                    | 3.17 us: 1.04x slower                                                   |
| scimark_monte_carlo              | 42.5 ms                                                    | 44.3 ms: 1.04x slower                                                   |
| chameleon                        | 4.27 ms                                                    | 4.45 ms: 1.04x slower                                                   |
| logging_format                   | 3.31 us                                                    | 3.46 us: 1.05x slower                                                   |
| genshi_text                      | 13.9 ms                                                    | 14.5 ms: 1.05x slower                                                   |
| float                            | 48.6 ms                                                    | 51.1 ms: 1.05x slower                                                   |
| raytrace                         | 147 ms                                                     | 155 ms: 1.05x slower                                                    |
| genshi_xml                       | 29.9 ms                                                    | 31.5 ms: 1.05x slower                                                   |
| bench_thread_pool                | 447 us                                                     | 471 us: 1.05x slower                                                    |
| coroutines                       | 15.8 ms                                                    | 16.8 ms: 1.06x slower                                                   |
| aiohttp                          | 997 us                                                     | 1.06 ms: 1.06x slower                                                   |
| typing_runtime_protocols         | 87.6 us                                                    | 93.1 us: 1.06x slower                                                   |
| gunicorn                         | 1.04 ms                                                    | 1.11 ms: 1.07x slower                                                   |
| chaos                            | 34.0 ms                                                    | 36.4 ms: 1.07x slower                                                   |
| nqueens                          | 52.2 ms                                                    | 55.9 ms: 1.07x slower                                                   |
| scimark_sparse_mat_mult          | 2.77 ms                                                    | 2.97 ms: 1.07x slower                                                   |
| scimark_fft                      | 181 ms                                                     | 195 ms: 1.08x slower                                                    |
| spectral_norm                    | 66.4 ms                                                    | 72.1 ms: 1.09x slower                                                   |
| async_tree_memoization_tg        | 240 ms                                                     | 261 ms: 1.09x slower                                                    |
| tornado_http                     | 66.7 ms                                                    | 74.1 ms: 1.11x slower                                                   |
| nbody                            | 59.6 ms                                                    | 69.9 ms: 1.17x slower                                                   |
| mypy2                            | 379 ms                                                     | 462 ms: 1.22x slower                                                    |
| generators                       | 22.9 ms                                                    | 28.9 ms: 1.26x slower                                                   |
| Geometric mean                   | (ref)                                                      | 1.02x slower                                                            |

Benchmark hidden because not significant (21): async_tree_eager_io_tg, async_tree_cpu_io_mixed, async_tree_eager_memoization, async_tree_io_tg, mdp, async_tree_none_tg, asyncio_websockets, richards, pickle, json, 2to3, pickle_list, dask, dulwich_log, sqlite_synth, pycparser, async_tree_io, pylint, async_tree_eager_io, asyncio_tcp, async_tree_memoization
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 0.96x