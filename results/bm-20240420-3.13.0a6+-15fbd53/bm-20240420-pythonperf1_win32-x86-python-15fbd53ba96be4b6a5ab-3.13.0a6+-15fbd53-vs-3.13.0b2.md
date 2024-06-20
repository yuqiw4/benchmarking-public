# Results vs. 3.13.0b2

- fork: python
- ref: 15fbd53ba96be4b6a5ab
- machine: windows-x86
- commit hash: 15fbd53
- commit date: 2024-04-20
- overall geometric mean: 1.02x faster
- HPT reliability: 99.88%
- HPT 99th percentile: 1.00x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 233 ms                                                              | 229 ms: 1.02x faster                                                            |
| docutils       | 1.81 sec                                                            | 1.79 sec: 1.01x faster                                                          |
| html5lib       | 45.4 ms                                                             | 42.2 ms: 1.08x faster                                                           |
| tornado_http   | 94.3 ms                                                             | 92.8 ms: 1.02x faster                                                           |
| Geometric mean | (ref)                                                               | 1.02x faster                                                                    |

Benchmark hidden because not significant (1): chameleon

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_memoization     | 275 ms                                                              | 270 ms: 1.02x faster                                                            |
| async_tree_none            | 228 ms                                                              | 225 ms: 1.01x faster                                                            |
| async_tree_io_tg           | 529 ms                                                              | 523 ms: 1.01x faster                                                            |
| async_tree_cpu_io_mixed    | 471 ms                                                              | 488 ms: 1.04x slower                                                            |
| async_tree_cpu_io_mixed_tg | 447 ms                                                              | 470 ms: 1.05x slower                                                            |
| Geometric mean             | (ref)                                                               | 1.00x slower                                                                    |

Benchmark hidden because not significant (3): async_tree_io, async_tree_memoization_tg, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| pidigits       | 199 ms                                                              | 196 ms: 1.01x faster                                                            |
| float          | 52.4 ms                                                             | 54.0 ms: 1.03x slower                                                           |
| nbody          | 76.9 ms                                                             | 80.7 ms: 1.05x slower                                                           |
| Geometric mean | (ref)                                                               | 1.02x slower                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 99.9 ms                                                             | 94.7 ms: 1.05x faster                                                           |
| regex_v8       | 15.7 ms                                                             | 15.8 ms: 1.01x slower                                                           |
| regex_effbot   | 1.88 ms                                                             | 1.92 ms: 1.02x slower                                                           |
| regex_dna      | 118 ms                                                              | 124 ms: 1.05x slower                                                            |
| Geometric mean | (ref)                                                               | 1.00x slower                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| pickle_list          | 3.57 us                                                             | 3.20 us: 1.11x faster                                                           |
| unpickle_pure_python | 147 us                                                              | 137 us: 1.08x faster                                                            |
| pickle_pure_python   | 213 us                                                              | 199 us: 1.07x faster                                                            |
| pickle_dict          | 20.8 us                                                             | 20.0 us: 1.04x faster                                                           |
| json_loads           | 20.5 us                                                             | 19.9 us: 1.03x faster                                                           |
| pickle               | 8.07 us                                                             | 7.84 us: 1.03x faster                                                           |
| tomli_loads          | 1.65 sec                                                            | 1.61 sec: 1.03x faster                                                          |
| json_dumps           | 6.84 ms                                                             | 6.76 ms: 1.01x faster                                                           |
| xml_etree_generate   | 59.6 ms                                                             | 60.6 ms: 1.02x slower                                                           |
| xml_etree_iterparse  | 64.2 ms                                                             | 65.4 ms: 1.02x slower                                                           |
| xml_etree_parse      | 104 ms                                                              | 108 ms: 1.03x slower                                                            |
| Geometric mean       | (ref)                                                               | 1.02x faster                                                                    |

Benchmark hidden because not significant (3): unpickle, unpickle_list, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|------------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup         | 22.2 ms                                                             | 21.8 ms: 1.02x faster                                                           |
| python_startup_no_site | 18.2 ms                                                             | 18.1 ms: 1.01x faster                                                           |
| Geometric mean         | (ref)                                                               | 1.01x faster                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| genshi_text     | 20.1 ms                                                             | 18.6 ms: 1.08x faster                                                           |
| genshi_xml      | 44.3 ms                                                             | 41.4 ms: 1.07x faster                                                           |
| django_template | 30.1 ms                                                             | 28.8 ms: 1.04x faster                                                           |
| mako            | 6.94 ms                                                             | 6.73 ms: 1.03x faster                                                           |
| Geometric mean  | (ref)                                                               | 1.06x faster                                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 136 us                                                              | 89.8 us: 1.51x faster                                                           |
| deepcopy_reduce            | 2.59 us                                                             | 2.30 us: 1.13x faster                                                           |
| pickle_list                | 3.57 us                                                             | 3.20 us: 1.11x faster                                                           |
| sqlglot_parse              | 964 us                                                              | 873 us: 1.10x faster                                                            |
| pprint_pformat             | 1.24 sec                                                            | 1.13 sec: 1.10x faster                                                          |
| pprint_safe_repr           | 607 ms                                                              | 553 ms: 1.10x faster                                                            |
| richards_super             | 35.5 ms                                                             | 32.7 ms: 1.09x faster                                                           |
| genshi_text                | 20.1 ms                                                             | 18.6 ms: 1.08x faster                                                           |
| sqlglot_transpile          | 1.19 ms                                                             | 1.10 ms: 1.08x faster                                                           |
| sympy_expand               | 375 ms                                                              | 348 ms: 1.08x faster                                                            |
| html5lib                   | 45.4 ms                                                             | 42.2 ms: 1.08x faster                                                           |
| unpickle_pure_python       | 147 us                                                              | 137 us: 1.08x faster                                                            |
| pickle_pure_python         | 213 us                                                              | 199 us: 1.07x faster                                                            |
| coroutines                 | 15.5 ms                                                             | 14.5 ms: 1.07x faster                                                           |
| genshi_xml                 | 44.3 ms                                                             | 41.4 ms: 1.07x faster                                                           |
| chaos                      | 48.0 ms                                                             | 45.0 ms: 1.07x faster                                                           |
| deepcopy                   | 280 us                                                              | 263 us: 1.06x faster                                                            |
| richards                   | 31.2 ms                                                             | 29.4 ms: 1.06x faster                                                           |
| sympy_str                  | 211 ms                                                              | 200 ms: 1.06x faster                                                            |
| regex_compile              | 99.9 ms                                                             | 94.7 ms: 1.05x faster                                                           |
| deltablue                  | 2.23 ms                                                             | 2.13 ms: 1.05x faster                                                           |
| django_template            | 30.1 ms                                                             | 28.8 ms: 1.04x faster                                                           |
| sympy_sum                  | 105 ms                                                              | 101 ms: 1.04x faster                                                            |
| create_gc_cycles           | 756 us                                                              | 728 us: 1.04x faster                                                            |
| pickle_dict                | 20.8 us                                                             | 20.0 us: 1.04x faster                                                           |
| go                         | 101 ms                                                              | 97.2 ms: 1.04x faster                                                           |
| raytrace                   | 189 ms                                                              | 182 ms: 1.04x faster                                                            |
| sympy_integrate            | 14.6 ms                                                             | 14.2 ms: 1.03x faster                                                           |
| mako                       | 6.94 ms                                                             | 6.73 ms: 1.03x faster                                                           |
| deepcopy_memo              | 23.5 us                                                             | 22.8 us: 1.03x faster                                                           |
| json_loads                 | 20.5 us                                                             | 19.9 us: 1.03x faster                                                           |
| pickle                     | 8.07 us                                                             | 7.84 us: 1.03x faster                                                           |
| sqlglot_normalize          | 206 ms                                                              | 201 ms: 1.03x faster                                                            |
| comprehensions             | 11.9 us                                                             | 11.6 us: 1.03x faster                                                           |
| sqlglot_optimize           | 39.7 ms                                                             | 38.7 ms: 1.03x faster                                                           |
| tomli_loads                | 1.65 sec                                                            | 1.61 sec: 1.03x faster                                                          |
| pycparser                  | 777 ms                                                              | 758 ms: 1.03x faster                                                            |
| sqlite_synth               | 1.96 us                                                             | 1.92 us: 1.02x faster                                                           |
| python_startup             | 22.2 ms                                                             | 21.8 ms: 1.02x faster                                                           |
| async_tree_memoization     | 275 ms                                                              | 270 ms: 1.02x faster                                                            |
| bench_mp_pool              | 69.4 ms                                                             | 68.1 ms: 1.02x faster                                                           |
| scimark_sor                | 81.0 ms                                                             | 79.5 ms: 1.02x faster                                                           |
| spectral_norm              | 68.0 ms                                                             | 66.8 ms: 1.02x faster                                                           |
| 2to3                       | 233 ms                                                              | 229 ms: 1.02x faster                                                            |
| tornado_http               | 94.3 ms                                                             | 92.8 ms: 1.02x faster                                                           |
| bench_thread_pool          | 985 us                                                              | 971 us: 1.01x faster                                                            |
| thrift                     | 9.73 ms                                                             | 9.59 ms: 1.01x faster                                                           |
| pidigits                   | 199 ms                                                              | 196 ms: 1.01x faster                                                            |
| async_tree_none            | 228 ms                                                              | 225 ms: 1.01x faster                                                            |
| async_tree_io_tg           | 529 ms                                                              | 523 ms: 1.01x faster                                                            |
| json_dumps                 | 6.84 ms                                                             | 6.76 ms: 1.01x faster                                                           |
| logging_format             | 8.13 us                                                             | 8.04 us: 1.01x faster                                                           |
| gc_traversal               | 1.43 ms                                                             | 1.42 ms: 1.01x faster                                                           |
| docutils                   | 1.81 sec                                                            | 1.79 sec: 1.01x faster                                                          |
| python_startup_no_site     | 18.2 ms                                                             | 18.1 ms: 1.01x faster                                                           |
| json                       | 4.10 ms                                                             | 4.07 ms: 1.01x faster                                                           |
| pathlib                    | 83.9 ms                                                             | 84.2 ms: 1.00x slower                                                           |
| regex_v8                   | 15.7 ms                                                             | 15.8 ms: 1.01x slower                                                           |
| fannkuch                   | 270 ms                                                              | 273 ms: 1.01x slower                                                            |
| nqueens                    | 68.7 ms                                                             | 69.4 ms: 1.01x slower                                                           |
| hexiom                     | 4.23 ms                                                             | 4.29 ms: 1.01x slower                                                           |
| scimark_lu                 | 59.4 ms                                                             | 60.2 ms: 1.01x slower                                                           |
| xml_etree_generate         | 59.6 ms                                                             | 60.6 ms: 1.02x slower                                                           |
| scimark_monte_carlo        | 45.2 ms                                                             | 46.0 ms: 1.02x slower                                                           |
| meteor_contest             | 74.1 ms                                                             | 75.5 ms: 1.02x slower                                                           |
| xml_etree_iterparse        | 64.2 ms                                                             | 65.4 ms: 1.02x slower                                                           |
| regex_effbot               | 1.88 ms                                                             | 1.92 ms: 1.02x slower                                                           |
| xml_etree_parse            | 104 ms                                                              | 108 ms: 1.03x slower                                                            |
| float                      | 52.4 ms                                                             | 54.0 ms: 1.03x slower                                                           |
| async_tree_cpu_io_mixed    | 471 ms                                                              | 488 ms: 1.04x slower                                                            |
| telco                      | 6.03 ms                                                             | 6.25 ms: 1.04x slower                                                           |
| scimark_fft                | 198 ms                                                              | 206 ms: 1.04x slower                                                            |
| mdp                        | 1.60 sec                                                            | 1.67 sec: 1.04x slower                                                          |
| regex_dna                  | 118 ms                                                              | 124 ms: 1.05x slower                                                            |
| nbody                      | 76.9 ms                                                             | 80.7 ms: 1.05x slower                                                           |
| async_tree_cpu_io_mixed_tg | 447 ms                                                              | 470 ms: 1.05x slower                                                            |
| generators                 | 21.2 ms                                                             | 22.4 ms: 1.06x slower                                                           |
| scimark_sparse_mat_mult    | 2.87 ms                                                             | 3.07 ms: 1.07x slower                                                           |
| async_generators           | 266 ms                                                              | 298 ms: 1.12x slower                                                            |
| coverage                   | 307 ms                                                              | 489 ms: 1.59x slower                                                            |
| Geometric mean             | (ref)                                                               | 1.02x faster                                                                    |

Benchmark hidden because not significant (14): asyncio_tcp, async_tree_io, async_tree_memoization_tg, crypto_pyaes, chameleon, asyncio_tcp_ssl, unpickle, pylint, unpickle_list, pyflate, logging_simple, logging_silent, xml_etree_process, async_tree_none_tg
Ignored benchmarks (1) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17.json: flaskblogging

# HPT report

- Reliability score: 99.88% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: unknown