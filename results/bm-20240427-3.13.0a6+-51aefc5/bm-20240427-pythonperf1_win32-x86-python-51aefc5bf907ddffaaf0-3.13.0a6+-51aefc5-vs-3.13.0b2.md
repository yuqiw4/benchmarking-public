# Results vs. 3.13.0b2

- fork: python
- ref: 51aefc5bf907ddffaaf0
- machine: windows-x86
- commit hash: 51aefc5
- commit date: 2024-04-27
- overall geometric mean: 1.01x faster
- HPT reliability: 97.79%
- HPT 99th percentile: 1.00x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 233 ms                                                              | 231 ms: 1.01x faster                                                            |
| chameleon      | 5.71 ms                                                             | 5.56 ms: 1.03x faster                                                           |
| docutils       | 1.81 sec                                                            | 1.81 sec: 1.00x faster                                                          |
| html5lib       | 45.4 ms                                                             | 43.3 ms: 1.05x faster                                                           |
| tornado_http   | 94.3 ms                                                             | 104 ms: 1.10x slower                                                            |
| Geometric mean | (ref)                                                               | 1.00x slower                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark              | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|------------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_memoization | 275 ms                                                              | 267 ms: 1.03x faster                                                            |
| async_tree_none        | 228 ms                                                              | 221 ms: 1.03x faster                                                            |
| async_tree_io          | 530 ms                                                              | 517 ms: 1.03x faster                                                            |
| Geometric mean         | (ref)                                                               | 1.01x faster                                                                    |

Benchmark hidden because not significant (5): async_tree_memoization_tg, async_tree_cpu_io_mixed, async_tree_io_tg, async_tree_cpu_io_mixed_tg, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| float          | 52.4 ms                                                             | 52.7 ms: 1.01x slower                                                           |
| pidigits       | 199 ms                                                              | 200 ms: 1.01x slower                                                            |
| nbody          | 76.9 ms                                                             | 80.9 ms: 1.05x slower                                                           |
| Geometric mean | (ref)                                                               | 1.02x slower                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 99.9 ms                                                             | 95.0 ms: 1.05x faster                                                           |
| regex_dna      | 118 ms                                                              | 121 ms: 1.02x slower                                                            |
| regex_effbot   | 1.88 ms                                                             | 1.94 ms: 1.03x slower                                                           |
| regex_v8       | 15.7 ms                                                             | 16.4 ms: 1.04x slower                                                           |
| Geometric mean | (ref)                                                               | 1.01x slower                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| unpickle_pure_python | 147 us                                                              | 138 us: 1.07x faster                                                            |
| pickle_pure_python   | 213 us                                                              | 202 us: 1.06x faster                                                            |
| pickle_dict          | 20.8 us                                                             | 20.2 us: 1.03x faster                                                           |
| pickle               | 8.07 us                                                             | 7.92 us: 1.02x faster                                                           |
| json_loads           | 20.5 us                                                             | 20.2 us: 1.02x faster                                                           |
| xml_etree_parse      | 104 ms                                                              | 103 ms: 1.02x faster                                                            |
| json_dumps           | 6.84 ms                                                             | 6.75 ms: 1.01x faster                                                           |
| tomli_loads          | 1.65 sec                                                            | 1.63 sec: 1.01x faster                                                          |
| pickle_list          | 3.57 us                                                             | 3.59 us: 1.01x slower                                                           |
| unpickle             | 9.79 us                                                             | 9.94 us: 1.02x slower                                                           |
| xml_etree_iterparse  | 64.2 ms                                                             | 65.5 ms: 1.02x slower                                                           |
| Geometric mean       | (ref)                                                               | 1.01x faster                                                                    |

Benchmark hidden because not significant (3): unpickle_list, xml_etree_process, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|------------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup         | 22.2 ms                                                             | 22.4 ms: 1.01x slower                                                           |
| python_startup_no_site | 18.2 ms                                                             | 18.7 ms: 1.03x slower                                                           |
| Geometric mean         | (ref)                                                               | 1.02x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|-----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| genshi_text     | 20.1 ms                                                             | 18.2 ms: 1.11x faster                                                           |
| django_template | 30.1 ms                                                             | 28.1 ms: 1.07x faster                                                           |
| genshi_xml      | 44.3 ms                                                             | 42.8 ms: 1.03x faster                                                           |
| mako            | 6.94 ms                                                             | 6.87 ms: 1.01x faster                                                           |
| Geometric mean  | (ref)                                                               | 1.05x faster                                                                    |

All benchmarks:
===============

| Benchmark                | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|--------------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| genshi_text              | 20.1 ms                                                             | 18.2 ms: 1.11x faster                                                           |
| pprint_safe_repr         | 607 ms                                                              | 549 ms: 1.11x faster                                                            |
| pprint_pformat           | 1.24 sec                                                            | 1.12 sec: 1.10x faster                                                          |
| sqlglot_parse            | 964 us                                                              | 883 us: 1.09x faster                                                            |
| chaos                    | 48.0 ms                                                             | 44.8 ms: 1.07x faster                                                           |
| django_template          | 30.1 ms                                                             | 28.1 ms: 1.07x faster                                                           |
| sympy_expand             | 375 ms                                                              | 351 ms: 1.07x faster                                                            |
| sqlglot_transpile        | 1.19 ms                                                             | 1.12 ms: 1.07x faster                                                           |
| sqlglot_normalize        | 206 ms                                                              | 193 ms: 1.07x faster                                                            |
| unpickle_pure_python     | 147 us                                                              | 138 us: 1.07x faster                                                            |
| richards_super           | 35.5 ms                                                             | 33.4 ms: 1.06x faster                                                           |
| logging_format           | 8.13 us                                                             | 7.66 us: 1.06x faster                                                           |
| pickle_pure_python       | 213 us                                                              | 202 us: 1.06x faster                                                            |
| regex_compile            | 99.9 ms                                                             | 95.0 ms: 1.05x faster                                                           |
| html5lib                 | 45.4 ms                                                             | 43.3 ms: 1.05x faster                                                           |
| deepcopy_reduce          | 2.59 us                                                             | 2.47 us: 1.05x faster                                                           |
| richards                 | 31.2 ms                                                             | 29.8 ms: 1.05x faster                                                           |
| logging_simple           | 7.47 us                                                             | 7.13 us: 1.05x faster                                                           |
| go                       | 101 ms                                                              | 96.2 ms: 1.05x faster                                                           |
| sympy_str                | 211 ms                                                              | 202 ms: 1.04x faster                                                            |
| deepcopy_memo            | 23.5 us                                                             | 22.6 us: 1.04x faster                                                           |
| deltablue                | 2.23 ms                                                             | 2.15 ms: 1.04x faster                                                           |
| nqueens                  | 68.7 ms                                                             | 66.0 ms: 1.04x faster                                                           |
| deepcopy                 | 280 us                                                              | 269 us: 1.04x faster                                                            |
| sqlglot_optimize         | 39.7 ms                                                             | 38.3 ms: 1.04x faster                                                           |
| typing_runtime_protocols | 136 us                                                              | 131 us: 1.03x faster                                                            |
| genshi_xml               | 44.3 ms                                                             | 42.8 ms: 1.03x faster                                                           |
| async_tree_memoization   | 275 ms                                                              | 267 ms: 1.03x faster                                                            |
| scimark_sor              | 81.0 ms                                                             | 78.5 ms: 1.03x faster                                                           |
| async_tree_none          | 228 ms                                                              | 221 ms: 1.03x faster                                                            |
| chameleon                | 5.71 ms                                                             | 5.56 ms: 1.03x faster                                                           |
| raytrace                 | 189 ms                                                              | 184 ms: 1.03x faster                                                            |
| sympy_sum                | 105 ms                                                              | 102 ms: 1.03x faster                                                            |
| pickle_dict              | 20.8 us                                                             | 20.2 us: 1.03x faster                                                           |
| async_tree_io            | 530 ms                                                              | 517 ms: 1.03x faster                                                            |
| pickle                   | 8.07 us                                                             | 7.92 us: 1.02x faster                                                           |
| json_loads               | 20.5 us                                                             | 20.2 us: 1.02x faster                                                           |
| sympy_integrate          | 14.6 ms                                                             | 14.4 ms: 1.02x faster                                                           |
| create_gc_cycles         | 756 us                                                              | 743 us: 1.02x faster                                                            |
| comprehensions           | 11.9 us                                                             | 11.7 us: 1.02x faster                                                           |
| xml_etree_parse          | 104 ms                                                              | 103 ms: 1.02x faster                                                            |
| json_dumps               | 6.84 ms                                                             | 6.75 ms: 1.01x faster                                                           |
| crypto_pyaes             | 55.8 ms                                                             | 55.1 ms: 1.01x faster                                                           |
| sqlite_synth             | 1.96 us                                                             | 1.94 us: 1.01x faster                                                           |
| tomli_loads              | 1.65 sec                                                            | 1.63 sec: 1.01x faster                                                          |
| hexiom                   | 4.23 ms                                                             | 4.18 ms: 1.01x faster                                                           |
| mako                     | 6.94 ms                                                             | 6.87 ms: 1.01x faster                                                           |
| 2to3                     | 233 ms                                                              | 231 ms: 1.01x faster                                                            |
| telco                    | 6.03 ms                                                             | 5.98 ms: 1.01x faster                                                           |
| docutils                 | 1.81 sec                                                            | 1.81 sec: 1.00x faster                                                          |
| meteor_contest           | 74.1 ms                                                             | 74.4 ms: 1.00x slower                                                           |
| mdp                      | 1.60 sec                                                            | 1.61 sec: 1.00x slower                                                          |
| float                    | 52.4 ms                                                             | 52.7 ms: 1.01x slower                                                           |
| pickle_list              | 3.57 us                                                             | 3.59 us: 1.01x slower                                                           |
| python_startup           | 22.2 ms                                                             | 22.4 ms: 1.01x slower                                                           |
| thrift                   | 9.73 ms                                                             | 9.80 ms: 1.01x slower                                                           |
| pidigits                 | 199 ms                                                              | 200 ms: 1.01x slower                                                            |
| bench_mp_pool            | 69.4 ms                                                             | 70.0 ms: 1.01x slower                                                           |
| json                     | 4.10 ms                                                             | 4.14 ms: 1.01x slower                                                           |
| gc_traversal             | 1.43 ms                                                             | 1.45 ms: 1.01x slower                                                           |
| scimark_lu               | 59.4 ms                                                             | 60.2 ms: 1.01x slower                                                           |
| coroutines               | 15.5 ms                                                             | 15.7 ms: 1.01x slower                                                           |
| unpickle                 | 9.79 us                                                             | 9.94 us: 1.02x slower                                                           |
| asyncio_tcp_ssl          | 16.9 sec                                                            | 17.2 sec: 1.02x slower                                                          |
| pyflate                  | 308 ms                                                              | 314 ms: 1.02x slower                                                            |
| xml_etree_iterparse      | 64.2 ms                                                             | 65.5 ms: 1.02x slower                                                           |
| scimark_monte_carlo      | 45.2 ms                                                             | 46.1 ms: 1.02x slower                                                           |
| regex_dna                | 118 ms                                                              | 121 ms: 1.02x slower                                                            |
| python_startup_no_site   | 18.2 ms                                                             | 18.7 ms: 1.03x slower                                                           |
| regex_effbot             | 1.88 ms                                                             | 1.94 ms: 1.03x slower                                                           |
| scimark_sparse_mat_mult  | 2.87 ms                                                             | 2.99 ms: 1.04x slower                                                           |
| regex_v8                 | 15.7 ms                                                             | 16.4 ms: 1.04x slower                                                           |
| generators               | 21.2 ms                                                             | 22.1 ms: 1.04x slower                                                           |
| nbody                    | 76.9 ms                                                             | 80.9 ms: 1.05x slower                                                           |
| pathlib                  | 83.9 ms                                                             | 88.7 ms: 1.06x slower                                                           |
| async_generators         | 266 ms                                                              | 283 ms: 1.07x slower                                                            |
| scimark_fft              | 198 ms                                                              | 212 ms: 1.07x slower                                                            |
| tornado_http             | 94.3 ms                                                             | 104 ms: 1.10x slower                                                            |
| asyncio_tcp              | 662 ms                                                              | 812 ms: 1.23x slower                                                            |
| coverage                 | 307 ms                                                              | 399 ms: 1.30x slower                                                            |
| Geometric mean           | (ref)                                                               | 1.01x faster                                                                    |

Benchmark hidden because not significant (14): async_tree_memoization_tg, async_tree_cpu_io_mixed, async_tree_io_tg, pycparser, unpickle_list, xml_etree_process, spectral_norm, fannkuch, async_tree_cpu_io_mixed_tg, xml_etree_generate, logging_silent, pylint, async_tree_none_tg, bench_thread_pool
Ignored benchmarks (1) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17.json: flaskblogging

# HPT report

- Reliability score: 97.79% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: unknown