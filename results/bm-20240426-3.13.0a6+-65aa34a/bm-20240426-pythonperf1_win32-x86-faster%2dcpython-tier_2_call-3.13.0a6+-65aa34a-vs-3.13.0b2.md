# Results vs. 3.13.0b2

- fork: faster-cpython
- ref: tier_2_call
- machine: windows-x86
- commit hash: 65aa34a
- commit date: 2024-04-26
- overall geometric mean: 1.00x slower
- HPT reliability: 60.34%
- HPT 99th percentile: 1.00x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-pythonperf1_win32-x86-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:-------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 233 ms                                                              | 235 ms: 1.01x slower                                                             |
| docutils       | 1.81 sec                                                            | 1.80 sec: 1.00x faster                                                           |
| html5lib       | 45.4 ms                                                             | 43.1 ms: 1.05x faster                                                            |
| tornado_http   | 94.3 ms                                                             | 102 ms: 1.09x slower                                                             |
| Geometric mean | (ref)                                                               | 1.01x slower                                                                     |

Benchmark hidden because not significant (1): chameleon

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-pythonperf1_win32-x86-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------------------|:-------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed    | 471 ms                                                              | 480 ms: 1.02x slower                                                             |
| async_tree_io_tg           | 529 ms                                                              | 539 ms: 1.02x slower                                                             |
| async_tree_cpu_io_mixed_tg | 447 ms                                                              | 458 ms: 1.02x slower                                                             |
| async_tree_none_tg         | 203 ms                                                              | 209 ms: 1.03x slower                                                             |
| Geometric mean             | (ref)                                                               | 1.01x slower                                                                     |

Benchmark hidden because not significant (4): async_tree_memoization, async_tree_io, async_tree_none, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-pythonperf1_win32-x86-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:-------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pidigits       | 199 ms                                                              | 200 ms: 1.01x slower                                                             |
| float          | 52.4 ms                                                             | 53.0 ms: 1.01x slower                                                            |
| nbody          | 76.9 ms                                                             | 80.3 ms: 1.04x slower                                                            |
| Geometric mean | (ref)                                                               | 1.02x slower                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-pythonperf1_win32-x86-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:-------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 99.9 ms                                                             | 96.3 ms: 1.04x faster                                                            |
| regex_dna      | 118 ms                                                              | 121 ms: 1.02x slower                                                             |
| Geometric mean | (ref)                                                               | 1.00x faster                                                                     |

Benchmark hidden because not significant (2): regex_effbot, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-pythonperf1_win32-x86-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------------|:-------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_list          | 3.57 us                                                             | 3.26 us: 1.10x faster                                                            |
| unpickle_pure_python | 147 us                                                              | 140 us: 1.05x faster                                                             |
| tomli_loads          | 1.65 sec                                                            | 1.58 sec: 1.04x faster                                                           |
| json_loads           | 20.5 us                                                             | 19.9 us: 1.03x faster                                                            |
| pickle               | 8.07 us                                                             | 7.90 us: 1.02x faster                                                            |
| pickle_pure_python   | 213 us                                                              | 209 us: 1.02x faster                                                             |
| pickle_dict          | 20.8 us                                                             | 20.3 us: 1.02x faster                                                            |
| xml_etree_generate   | 59.6 ms                                                             | 58.8 ms: 1.01x faster                                                            |
| unpickle_list        | 2.93 us                                                             | 2.90 us: 1.01x faster                                                            |
| xml_etree_process    | 42.1 ms                                                             | 41.8 ms: 1.01x faster                                                            |
| json_dumps           | 6.84 ms                                                             | 6.79 ms: 1.01x faster                                                            |
| xml_etree_iterparse  | 64.2 ms                                                             | 65.2 ms: 1.02x slower                                                            |
| xml_etree_parse      | 104 ms                                                              | 106 ms: 1.02x slower                                                             |
| unpickle             | 9.79 us                                                             | 9.97 us: 1.02x slower                                                            |
| Geometric mean       | (ref)                                                               | 1.02x faster                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-pythonperf1_win32-x86-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|------------------------|:-------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup_no_site | 18.2 ms                                                             | 18.4 ms: 1.01x slower                                                            |
| python_startup         | 22.2 ms                                                             | 22.6 ms: 1.02x slower                                                            |
| Geometric mean         | (ref)                                                               | 1.01x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-pythonperf1_win32-x86-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|-----------------|:-------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_text     | 20.1 ms                                                             | 18.9 ms: 1.07x faster                                                            |
| genshi_xml      | 44.3 ms                                                             | 43.1 ms: 1.03x faster                                                            |
| django_template | 30.1 ms                                                             | 29.8 ms: 1.01x faster                                                            |
| Geometric mean  | (ref)                                                               | 1.02x faster                                                                     |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                  | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-pythonperf1_win32-x86-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------------------|:-------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_list                | 3.57 us                                                             | 3.26 us: 1.10x faster                                                            |
| sympy_expand               | 375 ms                                                              | 347 ms: 1.08x faster                                                             |
| richards_super             | 35.5 ms                                                             | 33.0 ms: 1.08x faster                                                            |
| genshi_text                | 20.1 ms                                                             | 18.9 ms: 1.07x faster                                                            |
| sqlglot_parse              | 964 us                                                              | 907 us: 1.06x faster                                                             |
| sympy_str                  | 211 ms                                                              | 199 ms: 1.06x faster                                                             |
| richards                   | 31.2 ms                                                             | 29.5 ms: 1.06x faster                                                            |
| pprint_pformat             | 1.24 sec                                                            | 1.17 sec: 1.06x faster                                                           |
| html5lib                   | 45.4 ms                                                             | 43.1 ms: 1.05x faster                                                            |
| unpickle_pure_python       | 147 us                                                              | 140 us: 1.05x faster                                                             |
| pprint_safe_repr           | 607 ms                                                              | 576 ms: 1.05x faster                                                             |
| sqlglot_transpile          | 1.19 ms                                                             | 1.13 ms: 1.05x faster                                                            |
| logging_simple             | 7.47 us                                                             | 7.12 us: 1.05x faster                                                            |
| logging_format             | 8.13 us                                                             | 7.80 us: 1.04x faster                                                            |
| tomli_loads                | 1.65 sec                                                            | 1.58 sec: 1.04x faster                                                           |
| raytrace                   | 189 ms                                                              | 182 ms: 1.04x faster                                                             |
| typing_runtime_protocols   | 136 us                                                              | 131 us: 1.04x faster                                                             |
| regex_compile              | 99.9 ms                                                             | 96.3 ms: 1.04x faster                                                            |
| deltablue                  | 2.23 ms                                                             | 2.16 ms: 1.04x faster                                                            |
| json_loads                 | 20.5 us                                                             | 19.9 us: 1.03x faster                                                            |
| sqlglot_normalize          | 206 ms                                                              | 200 ms: 1.03x faster                                                             |
| logging_silent             | 57.9 ns                                                             | 56.1 ns: 1.03x faster                                                            |
| sympy_integrate            | 14.6 ms                                                             | 14.2 ms: 1.03x faster                                                            |
| deepcopy                   | 280 us                                                              | 272 us: 1.03x faster                                                             |
| telco                      | 6.03 ms                                                             | 5.87 ms: 1.03x faster                                                            |
| genshi_xml                 | 44.3 ms                                                             | 43.1 ms: 1.03x faster                                                            |
| sqlglot_optimize           | 39.7 ms                                                             | 38.7 ms: 1.03x faster                                                            |
| scimark_sor                | 81.0 ms                                                             | 79.1 ms: 1.02x faster                                                            |
| pickle                     | 8.07 us                                                             | 7.90 us: 1.02x faster                                                            |
| pickle_pure_python         | 213 us                                                              | 209 us: 1.02x faster                                                             |
| pickle_dict                | 20.8 us                                                             | 20.3 us: 1.02x faster                                                            |
| create_gc_cycles           | 756 us                                                              | 740 us: 1.02x faster                                                             |
| crypto_pyaes               | 55.8 ms                                                             | 54.9 ms: 1.02x faster                                                            |
| pycparser                  | 777 ms                                                              | 766 ms: 1.01x faster                                                             |
| xml_etree_generate         | 59.6 ms                                                             | 58.8 ms: 1.01x faster                                                            |
| sympy_sum                  | 105 ms                                                              | 104 ms: 1.01x faster                                                             |
| sqlite_synth               | 1.96 us                                                             | 1.93 us: 1.01x faster                                                            |
| comprehensions             | 11.9 us                                                             | 11.7 us: 1.01x faster                                                            |
| go                         | 101 ms                                                              | 99.6 ms: 1.01x faster                                                            |
| unpickle_list              | 2.93 us                                                             | 2.90 us: 1.01x faster                                                            |
| deepcopy_memo              | 23.5 us                                                             | 23.3 us: 1.01x faster                                                            |
| chaos                      | 48.0 ms                                                             | 47.5 ms: 1.01x faster                                                            |
| django_template            | 30.1 ms                                                             | 29.8 ms: 1.01x faster                                                            |
| xml_etree_process          | 42.1 ms                                                             | 41.8 ms: 1.01x faster                                                            |
| json_dumps                 | 6.84 ms                                                             | 6.79 ms: 1.01x faster                                                            |
| nqueens                    | 68.7 ms                                                             | 68.2 ms: 1.01x faster                                                            |
| docutils                   | 1.81 sec                                                            | 1.80 sec: 1.00x faster                                                           |
| mdp                        | 1.60 sec                                                            | 1.61 sec: 1.01x slower                                                           |
| bench_mp_pool              | 69.4 ms                                                             | 69.8 ms: 1.01x slower                                                            |
| pidigits                   | 199 ms                                                              | 200 ms: 1.01x slower                                                             |
| 2to3                       | 233 ms                                                              | 235 ms: 1.01x slower                                                             |
| fannkuch                   | 270 ms                                                              | 273 ms: 1.01x slower                                                             |
| float                      | 52.4 ms                                                             | 53.0 ms: 1.01x slower                                                            |
| python_startup_no_site     | 18.2 ms                                                             | 18.4 ms: 1.01x slower                                                            |
| gc_traversal               | 1.43 ms                                                             | 1.45 ms: 1.01x slower                                                            |
| coroutines                 | 15.5 ms                                                             | 15.7 ms: 1.01x slower                                                            |
| pyflate                    | 308 ms                                                              | 313 ms: 1.02x slower                                                             |
| xml_etree_iterparse        | 64.2 ms                                                             | 65.2 ms: 1.02x slower                                                            |
| xml_etree_parse            | 104 ms                                                              | 106 ms: 1.02x slower                                                             |
| python_startup             | 22.2 ms                                                             | 22.6 ms: 1.02x slower                                                            |
| json                       | 4.10 ms                                                             | 4.17 ms: 1.02x slower                                                            |
| asyncio_tcp_ssl            | 16.9 sec                                                            | 17.2 sec: 1.02x slower                                                           |
| async_tree_cpu_io_mixed    | 471 ms                                                              | 480 ms: 1.02x slower                                                             |
| thrift                     | 9.73 ms                                                             | 9.90 ms: 1.02x slower                                                            |
| unpickle                   | 9.79 us                                                             | 9.97 us: 1.02x slower                                                            |
| async_tree_io_tg           | 529 ms                                                              | 539 ms: 1.02x slower                                                             |
| regex_dna                  | 118 ms                                                              | 121 ms: 1.02x slower                                                             |
| scimark_lu                 | 59.4 ms                                                             | 60.7 ms: 1.02x slower                                                            |
| async_tree_cpu_io_mixed_tg | 447 ms                                                              | 458 ms: 1.02x slower                                                             |
| async_tree_none_tg         | 203 ms                                                              | 209 ms: 1.03x slower                                                             |
| scimark_monte_carlo        | 45.2 ms                                                             | 46.8 ms: 1.03x slower                                                            |
| meteor_contest             | 74.1 ms                                                             | 76.9 ms: 1.04x slower                                                            |
| nbody                      | 76.9 ms                                                             | 80.3 ms: 1.04x slower                                                            |
| scimark_fft                | 198 ms                                                              | 208 ms: 1.05x slower                                                             |
| scimark_sparse_mat_mult    | 2.87 ms                                                             | 3.06 ms: 1.06x slower                                                            |
| generators                 | 21.2 ms                                                             | 22.6 ms: 1.07x slower                                                            |
| pathlib                    | 83.9 ms                                                             | 90.2 ms: 1.08x slower                                                            |
| tornado_http               | 94.3 ms                                                             | 102 ms: 1.09x slower                                                             |
| async_generators           | 266 ms                                                              | 289 ms: 1.09x slower                                                             |
| asyncio_tcp                | 662 ms                                                              | 878 ms: 1.33x slower                                                             |
| coverage                   | 307 ms                                                              | 498 ms: 1.62x slower                                                             |
| Geometric mean             | (ref)                                                               | 1.00x slower                                                                     |

Benchmark hidden because not significant (13): regex_effbot, chameleon, deepcopy_reduce, async_tree_memoization, async_tree_io, spectral_norm, async_tree_none, mako, regex_v8, hexiom, pylint, async_tree_memoization_tg, bench_thread_pool
Ignored benchmarks (1) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17.json: flaskblogging

# HPT report

- Reliability score: 60.34% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: unknown