# Results vs. 3.13.0b2

- fork: python
- ref: d610d821fd210dce63a1
- machine: windows-x86
- commit hash: d610d82
- commit date: 2024-03-23
- overall geometric mean: 1.03x faster
- HPT reliability: 99.93%
- HPT 99th percentile: 1.00x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf1_win32-x86-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 233 ms                                                              | 228 ms: 1.02x faster                                                            |
| chameleon      | 5.71 ms                                                             | 5.65 ms: 1.01x faster                                                           |
| docutils       | 1.81 sec                                                            | 1.75 sec: 1.04x faster                                                          |
| html5lib       | 45.4 ms                                                             | 42.6 ms: 1.07x faster                                                           |
| Geometric mean | (ref)                                                               | 1.03x faster                                                                    |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf1_win32-x86-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|----------------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_io_tg           | 529 ms                                                              | 489 ms: 1.08x faster                                                            |
| async_tree_none            | 228 ms                                                              | 215 ms: 1.06x faster                                                            |
| async_tree_memoization     | 275 ms                                                              | 265 ms: 1.04x faster                                                            |
| async_tree_none_tg         | 203 ms                                                              | 198 ms: 1.03x faster                                                            |
| async_tree_cpu_io_mixed    | 471 ms                                                              | 461 ms: 1.02x faster                                                            |
| async_tree_cpu_io_mixed_tg | 447 ms                                                              | 458 ms: 1.02x slower                                                            |
| Geometric mean             | (ref)                                                               | 1.03x faster                                                                    |

Benchmark hidden because not significant (2): async_tree_io, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf1_win32-x86-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| float          | 52.4 ms                                                             | 51.5 ms: 1.02x faster                                                           |
| pidigits       | 199 ms                                                              | 197 ms: 1.01x faster                                                            |
| Geometric mean | (ref)                                                               | 1.01x faster                                                                    |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf1_win32-x86-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 99.9 ms                                                             | 94.4 ms: 1.06x faster                                                           |
| Geometric mean | (ref)                                                               | 1.01x faster                                                                    |

Benchmark hidden because not significant (3): regex_dna, regex_v8, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf1_win32-x86-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|----------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| pickle_list          | 3.57 us                                                             | 3.34 us: 1.07x faster                                                           |
| unpickle_pure_python | 147 us                                                              | 139 us: 1.06x faster                                                            |
| unpickle_list        | 2.93 us                                                             | 2.81 us: 1.04x faster                                                           |
| json_dumps           | 6.84 ms                                                             | 6.60 ms: 1.04x faster                                                           |
| xml_etree_process    | 42.1 ms                                                             | 40.8 ms: 1.03x faster                                                           |
| pickle_dict          | 20.8 us                                                             | 20.2 us: 1.03x faster                                                           |
| json_loads           | 20.5 us                                                             | 20.0 us: 1.03x faster                                                           |
| pickle               | 8.07 us                                                             | 7.85 us: 1.03x faster                                                           |
| tomli_loads          | 1.65 sec                                                            | 1.60 sec: 1.03x faster                                                          |
| pickle_pure_python   | 213 us                                                              | 211 us: 1.01x faster                                                            |
| xml_etree_generate   | 59.6 ms                                                             | 59.1 ms: 1.01x faster                                                           |
| unpickle             | 9.79 us                                                             | 9.75 us: 1.00x faster                                                           |
| xml_etree_iterparse  | 64.2 ms                                                             | 64.7 ms: 1.01x slower                                                           |
| xml_etree_parse      | 104 ms                                                              | 107 ms: 1.03x slower                                                            |
| Geometric mean       | (ref)                                                               | 1.02x faster                                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf1_win32-x86-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|------------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup_no_site | 18.2 ms                                                             | 19.7 ms: 1.08x slower                                                           |
| Geometric mean         | (ref)                                                               | 1.04x slower                                                                    |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf1_win32-x86-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|-----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| genshi_xml      | 44.3 ms                                                             | 40.1 ms: 1.10x faster                                                           |
| genshi_text     | 20.1 ms                                                             | 18.4 ms: 1.10x faster                                                           |
| django_template | 30.1 ms                                                             | 28.6 ms: 1.05x faster                                                           |
| Geometric mean  | (ref)                                                               | 1.07x faster                                                                    |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                  | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf1_win32-x86-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|----------------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 136 us                                                              | 89.9 us: 1.51x faster                                                           |
| create_gc_cycles           | 756 us                                                              | 646 us: 1.17x faster                                                            |
| pprint_safe_repr           | 607 ms                                                              | 540 ms: 1.12x faster                                                            |
| pprint_pformat             | 1.24 sec                                                            | 1.11 sec: 1.12x faster                                                          |
| sqlglot_parse              | 964 us                                                              | 859 us: 1.12x faster                                                            |
| genshi_xml                 | 44.3 ms                                                             | 40.1 ms: 1.10x faster                                                           |
| deepcopy_reduce            | 2.59 us                                                             | 2.35 us: 1.10x faster                                                           |
| sqlglot_transpile          | 1.19 ms                                                             | 1.08 ms: 1.10x faster                                                           |
| sympy_expand               | 375 ms                                                              | 342 ms: 1.10x faster                                                            |
| genshi_text                | 20.1 ms                                                             | 18.4 ms: 1.10x faster                                                           |
| richards_super             | 35.5 ms                                                             | 32.4 ms: 1.09x faster                                                           |
| sympy_str                  | 211 ms                                                              | 194 ms: 1.09x faster                                                            |
| async_tree_io_tg           | 529 ms                                                              | 489 ms: 1.08x faster                                                            |
| richards                   | 31.2 ms                                                             | 28.9 ms: 1.08x faster                                                           |
| crypto_pyaes               | 55.8 ms                                                             | 52.1 ms: 1.07x faster                                                           |
| pickle_list                | 3.57 us                                                             | 3.34 us: 1.07x faster                                                           |
| html5lib                   | 45.4 ms                                                             | 42.6 ms: 1.07x faster                                                           |
| deepcopy                   | 280 us                                                              | 263 us: 1.06x faster                                                            |
| sympy_sum                  | 105 ms                                                              | 98.9 ms: 1.06x faster                                                           |
| coroutines                 | 15.5 ms                                                             | 14.6 ms: 1.06x faster                                                           |
| regex_compile              | 99.9 ms                                                             | 94.4 ms: 1.06x faster                                                           |
| async_tree_none            | 228 ms                                                              | 215 ms: 1.06x faster                                                            |
| unpickle_pure_python       | 147 us                                                              | 139 us: 1.06x faster                                                            |
| sqlglot_normalize          | 206 ms                                                              | 196 ms: 1.05x faster                                                            |
| asyncio_tcp                | 662 ms                                                              | 629 ms: 1.05x faster                                                            |
| django_template            | 30.1 ms                                                             | 28.6 ms: 1.05x faster                                                           |
| sympy_integrate            | 14.6 ms                                                             | 13.9 ms: 1.05x faster                                                           |
| deltablue                  | 2.23 ms                                                             | 2.13 ms: 1.05x faster                                                           |
| sqlglot_optimize           | 39.7 ms                                                             | 38.1 ms: 1.04x faster                                                           |
| unpickle_list              | 2.93 us                                                             | 2.81 us: 1.04x faster                                                           |
| async_tree_memoization     | 275 ms                                                              | 265 ms: 1.04x faster                                                            |
| comprehensions             | 11.9 us                                                             | 11.4 us: 1.04x faster                                                           |
| docutils                   | 1.81 sec                                                            | 1.75 sec: 1.04x faster                                                          |
| json_dumps                 | 6.84 ms                                                             | 6.60 ms: 1.04x faster                                                           |
| go                         | 101 ms                                                              | 97.5 ms: 1.03x faster                                                           |
| xml_etree_process          | 42.1 ms                                                             | 40.8 ms: 1.03x faster                                                           |
| pickle_dict                | 20.8 us                                                             | 20.2 us: 1.03x faster                                                           |
| json_loads                 | 20.5 us                                                             | 20.0 us: 1.03x faster                                                           |
| pickle                     | 8.07 us                                                             | 7.85 us: 1.03x faster                                                           |
| tomli_loads                | 1.65 sec                                                            | 1.60 sec: 1.03x faster                                                          |
| async_tree_none_tg         | 203 ms                                                              | 198 ms: 1.03x faster                                                            |
| mdp                        | 1.60 sec                                                            | 1.56 sec: 1.02x faster                                                          |
| bench_thread_pool          | 985 us                                                              | 963 us: 1.02x faster                                                            |
| gc_traversal               | 1.43 ms                                                             | 1.40 ms: 1.02x faster                                                           |
| async_tree_cpu_io_mixed    | 471 ms                                                              | 461 ms: 1.02x faster                                                            |
| sqlite_synth               | 1.96 us                                                             | 1.92 us: 1.02x faster                                                           |
| spectral_norm              | 68.0 ms                                                             | 66.6 ms: 1.02x faster                                                           |
| deepcopy_memo              | 23.5 us                                                             | 23.0 us: 1.02x faster                                                           |
| 2to3                       | 233 ms                                                              | 228 ms: 1.02x faster                                                            |
| bench_mp_pool              | 69.4 ms                                                             | 68.1 ms: 1.02x faster                                                           |
| float                      | 52.4 ms                                                             | 51.5 ms: 1.02x faster                                                           |
| chameleon                  | 5.71 ms                                                             | 5.65 ms: 1.01x faster                                                           |
| pickle_pure_python         | 213 us                                                              | 211 us: 1.01x faster                                                            |
| hexiom                     | 4.23 ms                                                             | 4.19 ms: 1.01x faster                                                           |
| xml_etree_generate         | 59.6 ms                                                             | 59.1 ms: 1.01x faster                                                           |
| logging_silent             | 57.9 ns                                                             | 57.3 ns: 1.01x faster                                                           |
| asyncio_tcp_ssl            | 16.9 sec                                                            | 16.7 sec: 1.01x faster                                                          |
| pidigits                   | 199 ms                                                              | 197 ms: 1.01x faster                                                            |
| unpickle                   | 9.79 us                                                             | 9.75 us: 1.00x faster                                                           |
| scimark_monte_carlo        | 45.2 ms                                                             | 45.4 ms: 1.01x slower                                                           |
| async_generators           | 266 ms                                                              | 267 ms: 1.01x slower                                                            |
| thrift                     | 9.73 ms                                                             | 9.78 ms: 1.01x slower                                                           |
| scimark_lu                 | 59.4 ms                                                             | 59.8 ms: 1.01x slower                                                           |
| xml_etree_iterparse        | 64.2 ms                                                             | 64.7 ms: 1.01x slower                                                           |
| pyflate                    | 308 ms                                                              | 312 ms: 1.01x slower                                                            |
| meteor_contest             | 74.1 ms                                                             | 75.1 ms: 1.01x slower                                                           |
| scimark_sor                | 81.0 ms                                                             | 82.2 ms: 1.01x slower                                                           |
| json                       | 4.10 ms                                                             | 4.16 ms: 1.02x slower                                                           |
| nqueens                    | 68.7 ms                                                             | 69.8 ms: 1.02x slower                                                           |
| logging_format             | 8.13 us                                                             | 8.28 us: 1.02x slower                                                           |
| scimark_fft                | 198 ms                                                              | 202 ms: 1.02x slower                                                            |
| fannkuch                   | 270 ms                                                              | 276 ms: 1.02x slower                                                            |
| logging_simple             | 7.47 us                                                             | 7.64 us: 1.02x slower                                                           |
| telco                      | 6.03 ms                                                             | 6.17 ms: 1.02x slower                                                           |
| async_tree_cpu_io_mixed_tg | 447 ms                                                              | 458 ms: 1.02x slower                                                            |
| pathlib                    | 83.9 ms                                                             | 86.3 ms: 1.03x slower                                                           |
| xml_etree_parse            | 104 ms                                                              | 107 ms: 1.03x slower                                                            |
| raytrace                   | 189 ms                                                              | 198 ms: 1.05x slower                                                            |
| generators                 | 21.2 ms                                                             | 22.3 ms: 1.06x slower                                                           |
| python_startup_no_site     | 18.2 ms                                                             | 19.7 ms: 1.08x slower                                                           |
| coverage                   | 307 ms                                                              | 476 ms: 1.55x slower                                                            |
| Geometric mean             | (ref)                                                               | 1.03x faster                                                                    |

Benchmark hidden because not significant (13): async_tree_io, async_tree_memoization_tg, mako, pylint, tornado_http, pycparser, chaos, python_startup, regex_dna, regex_v8, nbody, regex_effbot, scimark_sparse_mat_mult
Ignored benchmarks (1) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17.json: flaskblogging
Ignored benchmarks (1) of results/bm-20240323-3.13.0a5+-d610d82/bm-20240323-pythonperf1_win32-x86-python-d610d821fd210dce63a1-3.13.0a5+-d610d82.json: unpack_sequence

# HPT report

- Reliability score: 99.93% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: unknown