# Results vs. 3.13.0b2

- fork: mdboom
- ref: tier2_func_simple_fr
- machine: windows-x86
- commit hash: c5564c1
- commit date: 2024-04-08
- overall geometric mean: 1.09x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 233 ms                                                              | 258 ms: 1.11x slower                                                            |
| chameleon      | 5.71 ms                                                             | 6.25 ms: 1.09x slower                                                           |
| docutils       | 1.81 sec                                                            | 1.95 sec: 1.08x slower                                                          |
| html5lib       | 45.4 ms                                                             | 46.6 ms: 1.03x slower                                                           |
| tornado_http   | 94.3 ms                                                             | 96.9 ms: 1.03x slower                                                           |
| Geometric mean | (ref)                                                               | 1.07x slower                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 447 ms                                                              | 460 ms: 1.03x slower                                                            |
| async_tree_io_tg           | 529 ms                                                              | 549 ms: 1.04x slower                                                            |
| async_tree_cpu_io_mixed    | 471 ms                                                              | 490 ms: 1.04x slower                                                            |
| async_tree_io              | 530 ms                                                              | 556 ms: 1.05x slower                                                            |
| async_tree_memoization     | 275 ms                                                              | 290 ms: 1.05x slower                                                            |
| async_tree_memoization_tg  | 254 ms                                                              | 268 ms: 1.06x slower                                                            |
| async_tree_none            | 228 ms                                                              | 241 ms: 1.06x slower                                                            |
| async_tree_none_tg         | 203 ms                                                              | 217 ms: 1.07x slower                                                            |
| Geometric mean             | (ref)                                                               | 1.05x slower                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| float          | 52.4 ms                                                             | 53.1 ms: 1.01x slower                                                           |
| nbody          | 76.9 ms                                                             | 94.8 ms: 1.23x slower                                                           |
| Geometric mean | (ref)                                                               | 1.08x slower                                                                    |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_effbot   | 1.88 ms                                                             | 1.91 ms: 1.01x slower                                                           |
| regex_dna      | 118 ms                                                              | 121 ms: 1.03x slower                                                            |
| regex_v8       | 15.7 ms                                                             | 16.2 ms: 1.03x slower                                                           |
| regex_compile  | 99.9 ms                                                             | 112 ms: 1.12x slower                                                            |
| Geometric mean | (ref)                                                               | 1.05x slower                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| pickle_list          | 3.57 us                                                             | 3.33 us: 1.07x faster                                                           |
| unpickle_list        | 2.93 us                                                             | 2.82 us: 1.04x faster                                                           |
| pickle_dict          | 20.8 us                                                             | 20.0 us: 1.04x faster                                                           |
| json_loads           | 20.5 us                                                             | 20.0 us: 1.03x faster                                                           |
| pickle               | 8.07 us                                                             | 8.13 us: 1.01x slower                                                           |
| xml_etree_iterparse  | 64.2 ms                                                             | 65.0 ms: 1.01x slower                                                           |
| xml_etree_parse      | 104 ms                                                              | 106 ms: 1.01x slower                                                            |
| unpickle             | 9.79 us                                                             | 10.1 us: 1.03x slower                                                           |
| xml_etree_generate   | 59.6 ms                                                             | 61.6 ms: 1.03x slower                                                           |
| pickle_pure_python   | 213 us                                                              | 222 us: 1.04x slower                                                            |
| xml_etree_process    | 42.1 ms                                                             | 44.2 ms: 1.05x slower                                                           |
| tomli_loads          | 1.65 sec                                                            | 1.80 sec: 1.09x slower                                                          |
| unpickle_pure_python | 147 us                                                              | 172 us: 1.17x slower                                                            |
| Geometric mean       | (ref)                                                               | 1.02x slower                                                                    |

Benchmark hidden because not significant (1): json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|------------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup         | 22.2 ms                                                             | 24.2 ms: 1.09x slower                                                           |
| python_startup_no_site | 18.2 ms                                                             | 22.0 ms: 1.21x slower                                                           |
| Geometric mean         | (ref)                                                               | 1.15x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako           | 6.94 ms                                                             | 6.99 ms: 1.01x slower                                                           |
| genshi_xml     | 44.3 ms                                                             | 48.4 ms: 1.09x slower                                                           |
| genshi_text    | 20.1 ms                                                             | 22.8 ms: 1.13x slower                                                           |
| Geometric mean | (ref)                                                               | 1.08x slower                                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 136 us                                                              | 101 us: 1.35x faster                                                            |
| pickle_list                | 3.57 us                                                             | 3.33 us: 1.07x faster                                                           |
| unpickle_list              | 2.93 us                                                             | 2.82 us: 1.04x faster                                                           |
| pickle_dict                | 20.8 us                                                             | 20.0 us: 1.04x faster                                                           |
| json_loads                 | 20.5 us                                                             | 20.0 us: 1.03x faster                                                           |
| coroutines                 | 15.5 ms                                                             | 15.1 ms: 1.02x faster                                                           |
| create_gc_cycles           | 756 us                                                              | 745 us: 1.01x faster                                                            |
| pickle                     | 8.07 us                                                             | 8.13 us: 1.01x slower                                                           |
| mako                       | 6.94 ms                                                             | 6.99 ms: 1.01x slower                                                           |
| json                       | 4.10 ms                                                             | 4.13 ms: 1.01x slower                                                           |
| deepcopy_reduce            | 2.59 us                                                             | 2.61 us: 1.01x slower                                                           |
| sqlite_synth               | 1.96 us                                                             | 1.98 us: 1.01x slower                                                           |
| xml_etree_iterparse        | 64.2 ms                                                             | 65.0 ms: 1.01x slower                                                           |
| regex_effbot               | 1.88 ms                                                             | 1.91 ms: 1.01x slower                                                           |
| xml_etree_parse            | 104 ms                                                              | 106 ms: 1.01x slower                                                            |
| float                      | 52.4 ms                                                             | 53.1 ms: 1.01x slower                                                           |
| sympy_expand               | 375 ms                                                              | 382 ms: 1.02x slower                                                            |
| regex_dna                  | 118 ms                                                              | 121 ms: 1.03x slower                                                            |
| html5lib                   | 45.4 ms                                                             | 46.6 ms: 1.03x slower                                                           |
| tornado_http               | 94.3 ms                                                             | 96.9 ms: 1.03x slower                                                           |
| async_tree_cpu_io_mixed_tg | 447 ms                                                              | 460 ms: 1.03x slower                                                            |
| unpickle                   | 9.79 us                                                             | 10.1 us: 1.03x slower                                                           |
| regex_v8                   | 15.7 ms                                                             | 16.2 ms: 1.03x slower                                                           |
| pylint                     | 217 ms                                                              | 224 ms: 1.03x slower                                                            |
| xml_etree_generate         | 59.6 ms                                                             | 61.6 ms: 1.03x slower                                                           |
| sqlglot_parse              | 964 us                                                              | 997 us: 1.03x slower                                                            |
| async_tree_io_tg           | 529 ms                                                              | 549 ms: 1.04x slower                                                            |
| async_tree_cpu_io_mixed    | 471 ms                                                              | 490 ms: 1.04x slower                                                            |
| pathlib                    | 83.9 ms                                                             | 87.1 ms: 1.04x slower                                                           |
| deepcopy                   | 280 us                                                              | 291 us: 1.04x slower                                                            |
| generators                 | 21.2 ms                                                             | 22.0 ms: 1.04x slower                                                           |
| pickle_pure_python         | 213 us                                                              | 222 us: 1.04x slower                                                            |
| sympy_str                  | 211 ms                                                              | 221 ms: 1.05x slower                                                            |
| sqlglot_transpile          | 1.19 ms                                                             | 1.25 ms: 1.05x slower                                                           |
| async_tree_io              | 530 ms                                                              | 556 ms: 1.05x slower                                                            |
| xml_etree_process          | 42.1 ms                                                             | 44.2 ms: 1.05x slower                                                           |
| deepcopy_memo              | 23.5 us                                                             | 24.8 us: 1.05x slower                                                           |
| logging_silent             | 57.9 ns                                                             | 61.0 ns: 1.05x slower                                                           |
| async_tree_memoization     | 275 ms                                                              | 290 ms: 1.05x slower                                                            |
| async_tree_memoization_tg  | 254 ms                                                              | 268 ms: 1.06x slower                                                            |
| async_tree_none            | 228 ms                                                              | 241 ms: 1.06x slower                                                            |
| bench_mp_pool              | 69.4 ms                                                             | 73.8 ms: 1.06x slower                                                           |
| telco                      | 6.03 ms                                                             | 6.43 ms: 1.07x slower                                                           |
| sympy_sum                  | 105 ms                                                              | 112 ms: 1.07x slower                                                            |
| async_tree_none_tg         | 203 ms                                                              | 217 ms: 1.07x slower                                                            |
| docutils                   | 1.81 sec                                                            | 1.95 sec: 1.08x slower                                                          |
| logging_format             | 8.13 us                                                             | 8.76 us: 1.08x slower                                                           |
| spectral_norm              | 68.0 ms                                                             | 73.6 ms: 1.08x slower                                                           |
| async_generators           | 266 ms                                                              | 288 ms: 1.08x slower                                                            |
| logging_simple             | 7.47 us                                                             | 8.11 us: 1.09x slower                                                           |
| python_startup             | 22.2 ms                                                             | 24.2 ms: 1.09x slower                                                           |
| tomli_loads                | 1.65 sec                                                            | 1.80 sec: 1.09x slower                                                          |
| chameleon                  | 5.71 ms                                                             | 6.25 ms: 1.09x slower                                                           |
| pycparser                  | 777 ms                                                              | 850 ms: 1.09x slower                                                            |
| genshi_xml                 | 44.3 ms                                                             | 48.4 ms: 1.09x slower                                                           |
| thrift                     | 9.73 ms                                                             | 10.7 ms: 1.10x slower                                                           |
| 2to3                       | 233 ms                                                              | 258 ms: 1.11x slower                                                            |
| richards_super             | 35.5 ms                                                             | 39.5 ms: 1.11x slower                                                           |
| meteor_contest             | 74.1 ms                                                             | 82.6 ms: 1.12x slower                                                           |
| crypto_pyaes               | 55.8 ms                                                             | 62.4 ms: 1.12x slower                                                           |
| regex_compile              | 99.9 ms                                                             | 112 ms: 1.12x slower                                                            |
| scimark_sparse_mat_mult    | 2.87 ms                                                             | 3.22 ms: 1.12x slower                                                           |
| mdp                        | 1.60 sec                                                            | 1.80 sec: 1.13x slower                                                          |
| richards                   | 31.2 ms                                                             | 35.2 ms: 1.13x slower                                                           |
| sympy_integrate            | 14.6 ms                                                             | 16.6 ms: 1.13x slower                                                           |
| sqlglot_normalize          | 206 ms                                                              | 233 ms: 1.13x slower                                                            |
| genshi_text                | 20.1 ms                                                             | 22.8 ms: 1.13x slower                                                           |
| sqlglot_optimize           | 39.7 ms                                                             | 46.2 ms: 1.16x slower                                                           |
| unpickle_pure_python       | 147 us                                                              | 172 us: 1.17x slower                                                            |
| pyflate                    | 308 ms                                                              | 362 ms: 1.17x slower                                                            |
| fannkuch                   | 270 ms                                                              | 321 ms: 1.19x slower                                                            |
| python_startup_no_site     | 18.2 ms                                                             | 22.0 ms: 1.21x slower                                                           |
| raytrace                   | 189 ms                                                              | 231 ms: 1.22x slower                                                            |
| deltablue                  | 2.23 ms                                                             | 2.74 ms: 1.23x slower                                                           |
| nbody                      | 76.9 ms                                                             | 94.8 ms: 1.23x slower                                                           |
| go                         | 101 ms                                                              | 124 ms: 1.23x slower                                                            |
| scimark_fft                | 198 ms                                                              | 245 ms: 1.24x slower                                                            |
| scimark_sor                | 81.0 ms                                                             | 101 ms: 1.24x slower                                                            |
| pprint_safe_repr           | 607 ms                                                              | 769 ms: 1.27x slower                                                            |
| pprint_pformat             | 1.24 sec                                                            | 1.58 sec: 1.27x slower                                                          |
| chaos                      | 48.0 ms                                                             | 61.2 ms: 1.28x slower                                                           |
| comprehensions             | 11.9 us                                                             | 15.6 us: 1.32x slower                                                           |
| nqueens                    | 68.7 ms                                                             | 94.2 ms: 1.37x slower                                                           |
| scimark_monte_carlo        | 45.2 ms                                                             | 63.3 ms: 1.40x slower                                                           |
| hexiom                     | 4.23 ms                                                             | 6.10 ms: 1.44x slower                                                           |
| scimark_lu                 | 59.4 ms                                                             | 86.2 ms: 1.45x slower                                                           |
| coverage                   | 307 ms                                                              | 531 ms: 1.73x slower                                                            |
| Geometric mean             | (ref)                                                               | 1.09x slower                                                                    |

Benchmark hidden because not significant (6): asyncio_tcp, pidigits, asyncio_tcp_ssl, gc_traversal, json_dumps, bench_thread_pool
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17.json: django_template, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.05x

# Memory
- memory change: unknown