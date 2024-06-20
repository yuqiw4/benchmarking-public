# Results vs. 3.13.0b2

- fork: python
- ref: bfc57d43d8766120ba0c
- machine: windows-x86
- commit hash: bfc57d4
- commit date: 2024-03-29
- overall geometric mean: 1.02x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 233 ms                                                              | 231 ms: 1.01x faster                                                            |
| chameleon      | 5.71 ms                                                             | 5.57 ms: 1.03x faster                                                           |
| docutils       | 1.81 sec                                                            | 1.77 sec: 1.02x faster                                                          |
| html5lib       | 45.4 ms                                                             | 42.8 ms: 1.06x faster                                                           |
| Geometric mean | (ref)                                                               | 1.02x faster                                                                    |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_none            | 228 ms                                                              | 213 ms: 1.07x faster                                                            |
| async_tree_cpu_io_mixed    | 471 ms                                                              | 447 ms: 1.06x faster                                                            |
| async_tree_memoization     | 275 ms                                                              | 262 ms: 1.05x faster                                                            |
| async_tree_none_tg         | 203 ms                                                              | 196 ms: 1.03x faster                                                            |
| async_tree_io              | 530 ms                                                              | 515 ms: 1.03x faster                                                            |
| async_tree_cpu_io_mixed_tg | 447 ms                                                              | 439 ms: 1.02x faster                                                            |
| async_tree_io_tg           | 529 ms                                                              | 524 ms: 1.01x faster                                                            |
| Geometric mean             | (ref)                                                               | 1.04x faster                                                                    |

Benchmark hidden because not significant (1): async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| nbody          | 76.9 ms                                                             | 74.3 ms: 1.03x faster                                                           |
| float          | 52.4 ms                                                             | 51.3 ms: 1.02x faster                                                           |
| pidigits       | 199 ms                                                              | 200 ms: 1.01x slower                                                            |
| Geometric mean | (ref)                                                               | 1.02x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 99.9 ms                                                             | 95.0 ms: 1.05x faster                                                           |
| regex_effbot   | 1.88 ms                                                             | 1.91 ms: 1.01x slower                                                           |
| regex_v8       | 15.7 ms                                                             | 16.1 ms: 1.02x slower                                                           |
| regex_dna      | 118 ms                                                              | 131 ms: 1.11x slower                                                            |
| Geometric mean | (ref)                                                               | 1.02x slower                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| pickle_list          | 3.57 us                                                             | 3.22 us: 1.11x faster                                                           |
| unpickle_pure_python | 147 us                                                              | 139 us: 1.06x faster                                                            |
| pickle_pure_python   | 213 us                                                              | 202 us: 1.05x faster                                                            |
| tomli_loads          | 1.65 sec                                                            | 1.60 sec: 1.03x faster                                                          |
| pickle_dict          | 20.8 us                                                             | 20.2 us: 1.03x faster                                                           |
| xml_etree_generate   | 59.6 ms                                                             | 57.9 ms: 1.03x faster                                                           |
| pickle               | 8.07 us                                                             | 7.87 us: 1.03x faster                                                           |
| unpickle_list        | 2.93 us                                                             | 2.87 us: 1.02x faster                                                           |
| json_loads           | 20.5 us                                                             | 20.3 us: 1.01x faster                                                           |
| json_dumps           | 6.84 ms                                                             | 6.79 ms: 1.01x faster                                                           |
| xml_etree_parse      | 104 ms                                                              | 105 ms: 1.01x slower                                                            |
| unpickle             | 9.79 us                                                             | 9.93 us: 1.01x slower                                                           |
| xml_etree_process    | 42.1 ms                                                             | 42.9 ms: 1.02x slower                                                           |
| Geometric mean       | (ref)                                                               | 1.02x faster                                                                    |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|------------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup_no_site | 18.2 ms                                                             | 19.8 ms: 1.09x slower                                                           |
| Geometric mean         | (ref)                                                               | 1.04x slower                                                                    |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|-----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| genshi_text     | 20.1 ms                                                             | 18.8 ms: 1.07x faster                                                           |
| django_template | 30.1 ms                                                             | 28.8 ms: 1.04x faster                                                           |
| genshi_xml      | 44.3 ms                                                             | 43.2 ms: 1.02x faster                                                           |
| mako            | 6.94 ms                                                             | 6.89 ms: 1.01x faster                                                           |
| Geometric mean  | (ref)                                                               | 1.04x faster                                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 136 us                                                              | 90.5 us: 1.50x faster                                                           |
| sqlglot_parse              | 964 us                                                              | 860 us: 1.12x faster                                                            |
| richards                   | 31.2 ms                                                             | 28.1 ms: 1.11x faster                                                           |
| coroutines                 | 15.5 ms                                                             | 13.9 ms: 1.11x faster                                                           |
| pickle_list                | 3.57 us                                                             | 3.22 us: 1.11x faster                                                           |
| richards_super             | 35.5 ms                                                             | 32.2 ms: 1.10x faster                                                           |
| deepcopy_reduce            | 2.59 us                                                             | 2.36 us: 1.09x faster                                                           |
| sqlglot_transpile          | 1.19 ms                                                             | 1.09 ms: 1.09x faster                                                           |
| sympy_expand               | 375 ms                                                              | 345 ms: 1.09x faster                                                            |
| pprint_pformat             | 1.24 sec                                                            | 1.14 sec: 1.09x faster                                                          |
| pprint_safe_repr           | 607 ms                                                              | 562 ms: 1.08x faster                                                            |
| sympy_str                  | 211 ms                                                              | 196 ms: 1.08x faster                                                            |
| genshi_text                | 20.1 ms                                                             | 18.8 ms: 1.07x faster                                                           |
| async_tree_none            | 228 ms                                                              | 213 ms: 1.07x faster                                                            |
| deepcopy_memo              | 23.5 us                                                             | 22.0 us: 1.07x faster                                                           |
| pylint                     | 217 ms                                                              | 204 ms: 1.07x faster                                                            |
| html5lib                   | 45.4 ms                                                             | 42.8 ms: 1.06x faster                                                           |
| asyncio_tcp                | 662 ms                                                              | 623 ms: 1.06x faster                                                            |
| unpickle_pure_python       | 147 us                                                              | 139 us: 1.06x faster                                                            |
| comprehensions             | 11.9 us                                                             | 11.2 us: 1.06x faster                                                           |
| async_tree_cpu_io_mixed    | 471 ms                                                              | 447 ms: 1.06x faster                                                            |
| pickle_pure_python         | 213 us                                                              | 202 us: 1.05x faster                                                            |
| deepcopy                   | 280 us                                                              | 266 us: 1.05x faster                                                            |
| regex_compile              | 99.9 ms                                                             | 95.0 ms: 1.05x faster                                                           |
| async_tree_memoization     | 275 ms                                                              | 262 ms: 1.05x faster                                                            |
| sympy_integrate            | 14.6 ms                                                             | 14.0 ms: 1.05x faster                                                           |
| django_template            | 30.1 ms                                                             | 28.8 ms: 1.04x faster                                                           |
| go                         | 101 ms                                                              | 96.6 ms: 1.04x faster                                                           |
| sympy_sum                  | 105 ms                                                              | 101 ms: 1.04x faster                                                            |
| nqueens                    | 68.7 ms                                                             | 66.0 ms: 1.04x faster                                                           |
| create_gc_cycles           | 756 us                                                              | 726 us: 1.04x faster                                                            |
| deltablue                  | 2.23 ms                                                             | 2.15 ms: 1.04x faster                                                           |
| sqlglot_optimize           | 39.7 ms                                                             | 38.3 ms: 1.04x faster                                                           |
| nbody                      | 76.9 ms                                                             | 74.3 ms: 1.03x faster                                                           |
| async_tree_none_tg         | 203 ms                                                              | 196 ms: 1.03x faster                                                            |
| scimark_sor                | 81.0 ms                                                             | 78.5 ms: 1.03x faster                                                           |
| chaos                      | 48.0 ms                                                             | 46.5 ms: 1.03x faster                                                           |
| crypto_pyaes               | 55.8 ms                                                             | 54.1 ms: 1.03x faster                                                           |
| sqlglot_normalize          | 206 ms                                                              | 200 ms: 1.03x faster                                                            |
| async_tree_io              | 530 ms                                                              | 515 ms: 1.03x faster                                                            |
| tomli_loads                | 1.65 sec                                                            | 1.60 sec: 1.03x faster                                                          |
| pickle_dict                | 20.8 us                                                             | 20.2 us: 1.03x faster                                                           |
| telco                      | 6.03 ms                                                             | 5.86 ms: 1.03x faster                                                           |
| xml_etree_generate         | 59.6 ms                                                             | 57.9 ms: 1.03x faster                                                           |
| raytrace                   | 189 ms                                                              | 184 ms: 1.03x faster                                                            |
| pickle                     | 8.07 us                                                             | 7.87 us: 1.03x faster                                                           |
| chameleon                  | 5.71 ms                                                             | 5.57 ms: 1.03x faster                                                           |
| spectral_norm              | 68.0 ms                                                             | 66.3 ms: 1.03x faster                                                           |
| genshi_xml                 | 44.3 ms                                                             | 43.2 ms: 1.02x faster                                                           |
| docutils                   | 1.81 sec                                                            | 1.77 sec: 1.02x faster                                                          |
| unpickle_list              | 2.93 us                                                             | 2.87 us: 1.02x faster                                                           |
| float                      | 52.4 ms                                                             | 51.3 ms: 1.02x faster                                                           |
| bench_mp_pool              | 69.4 ms                                                             | 68.0 ms: 1.02x faster                                                           |
| async_tree_cpu_io_mixed_tg | 447 ms                                                              | 439 ms: 1.02x faster                                                            |
| mdp                        | 1.60 sec                                                            | 1.57 sec: 1.02x faster                                                          |
| sqlite_synth               | 1.96 us                                                             | 1.93 us: 1.02x faster                                                           |
| hexiom                     | 4.23 ms                                                             | 4.18 ms: 1.01x faster                                                           |
| json_loads                 | 20.5 us                                                             | 20.3 us: 1.01x faster                                                           |
| logging_silent             | 57.9 ns                                                             | 57.2 ns: 1.01x faster                                                           |
| 2to3                       | 233 ms                                                              | 231 ms: 1.01x faster                                                            |
| scimark_monte_carlo        | 45.2 ms                                                             | 44.7 ms: 1.01x faster                                                           |
| async_tree_io_tg           | 529 ms                                                              | 524 ms: 1.01x faster                                                            |
| asyncio_tcp_ssl            | 16.9 sec                                                            | 16.7 sec: 1.01x faster                                                          |
| json_dumps                 | 6.84 ms                                                             | 6.79 ms: 1.01x faster                                                           |
| mako                       | 6.94 ms                                                             | 6.89 ms: 1.01x faster                                                           |
| pycparser                  | 777 ms                                                              | 772 ms: 1.01x faster                                                            |
| pidigits                   | 199 ms                                                              | 200 ms: 1.01x slower                                                            |
| xml_etree_parse            | 104 ms                                                              | 105 ms: 1.01x slower                                                            |
| unpickle                   | 9.79 us                                                             | 9.93 us: 1.01x slower                                                           |
| regex_effbot               | 1.88 ms                                                             | 1.91 ms: 1.01x slower                                                           |
| json                       | 4.10 ms                                                             | 4.17 ms: 1.02x slower                                                           |
| thrift                     | 9.73 ms                                                             | 9.91 ms: 1.02x slower                                                           |
| xml_etree_process          | 42.1 ms                                                             | 42.9 ms: 1.02x slower                                                           |
| regex_v8                   | 15.7 ms                                                             | 16.1 ms: 1.02x slower                                                           |
| pathlib                    | 83.9 ms                                                             | 86.4 ms: 1.03x slower                                                           |
| scimark_lu                 | 59.4 ms                                                             | 61.7 ms: 1.04x slower                                                           |
| generators                 | 21.2 ms                                                             | 22.3 ms: 1.05x slower                                                           |
| scimark_fft                | 198 ms                                                              | 210 ms: 1.06x slower                                                            |
| async_generators           | 266 ms                                                              | 286 ms: 1.07x slower                                                            |
| python_startup_no_site     | 18.2 ms                                                             | 19.8 ms: 1.09x slower                                                           |
| regex_dna                  | 118 ms                                                              | 131 ms: 1.11x slower                                                            |
| coverage                   | 307 ms                                                              | 470 ms: 1.53x slower                                                            |
| Geometric mean             | (ref)                                                               | 1.02x faster                                                                    |

Benchmark hidden because not significant (12): async_tree_memoization_tg, xml_etree_iterparse, bench_thread_pool, pyflate, logging_format, python_startup, meteor_contest, logging_simple, gc_traversal, fannkuch, tornado_http, scimark_sparse_mat_mult
Ignored benchmarks (1) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17.json: flaskblogging
Ignored benchmarks (1) of results/bm-20240329-3.13.0a5+-bfc57d4/bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4.json: unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: unknown