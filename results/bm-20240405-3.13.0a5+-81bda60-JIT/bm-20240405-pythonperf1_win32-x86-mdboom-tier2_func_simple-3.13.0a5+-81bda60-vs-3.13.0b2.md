# Results vs. 3.13.0b2

- fork: mdboom
- ref: tier2_func_simple
- machine: windows-x86
- commit hash: 81bda60
- commit date: 2024-04-05
- overall geometric mean: 1.08x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240405-pythonperf1_win32-x86-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 233 ms                                                              | 255 ms: 1.09x slower                                                         |
| chameleon      | 5.71 ms                                                             | 6.16 ms: 1.08x slower                                                        |
| docutils       | 1.81 sec                                                            | 1.94 sec: 1.07x slower                                                       |
| html5lib       | 45.4 ms                                                             | 45.9 ms: 1.01x slower                                                        |
| tornado_http   | 94.3 ms                                                             | 96.6 ms: 1.02x slower                                                        |
| Geometric mean | (ref)                                                               | 1.06x slower                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240405-pythonperf1_win32-x86-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_io_tg           | 529 ms                                                              | 542 ms: 1.02x slower                                                         |
| async_tree_cpu_io_mixed    | 471 ms                                                              | 486 ms: 1.03x slower                                                         |
| async_tree_cpu_io_mixed_tg | 447 ms                                                              | 461 ms: 1.03x slower                                                         |
| async_tree_memoization     | 275 ms                                                              | 286 ms: 1.04x slower                                                         |
| async_tree_memoization_tg  | 254 ms                                                              | 265 ms: 1.04x slower                                                         |
| async_tree_none            | 228 ms                                                              | 238 ms: 1.05x slower                                                         |
| async_tree_none_tg         | 203 ms                                                              | 216 ms: 1.06x slower                                                         |
| Geometric mean             | (ref)                                                               | 1.04x slower                                                                 |

Benchmark hidden because not significant (1): async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240405-pythonperf1_win32-x86-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pidigits       | 199 ms                                                              | 198 ms: 1.00x faster                                                         |
| float          | 52.4 ms                                                             | 54.0 ms: 1.03x slower                                                        |
| nbody          | 76.9 ms                                                             | 96.4 ms: 1.25x slower                                                        |
| Geometric mean | (ref)                                                               | 1.09x slower                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240405-pythonperf1_win32-x86-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_v8       | 15.7 ms                                                             | 16.2 ms: 1.03x slower                                                        |
| regex_dna      | 118 ms                                                              | 124 ms: 1.05x slower                                                         |
| regex_compile  | 99.9 ms                                                             | 112 ms: 1.12x slower                                                         |
| Geometric mean | (ref)                                                               | 1.05x slower                                                                 |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240405-pythonperf1_win32-x86-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pickle_list          | 3.57 us                                                             | 3.17 us: 1.12x faster                                                        |
| unpickle_list        | 2.93 us                                                             | 2.75 us: 1.07x faster                                                        |
| pickle_dict          | 20.8 us                                                             | 19.8 us: 1.05x faster                                                        |
| json_loads           | 20.5 us                                                             | 20.1 us: 1.02x faster                                                        |
| pickle               | 8.07 us                                                             | 7.95 us: 1.02x faster                                                        |
| json_dumps           | 6.84 ms                                                             | 6.76 ms: 1.01x faster                                                        |
| xml_etree_generate   | 59.6 ms                                                             | 60.4 ms: 1.01x slower                                                        |
| unpickle             | 9.79 us                                                             | 9.95 us: 1.02x slower                                                        |
| xml_etree_iterparse  | 64.2 ms                                                             | 65.4 ms: 1.02x slower                                                        |
| xml_etree_parse      | 104 ms                                                              | 107 ms: 1.02x slower                                                         |
| xml_etree_process    | 42.1 ms                                                             | 43.2 ms: 1.03x slower                                                        |
| pickle_pure_python   | 213 us                                                              | 221 us: 1.04x slower                                                         |
| tomli_loads          | 1.65 sec                                                            | 1.75 sec: 1.06x slower                                                       |
| unpickle_pure_python | 147 us                                                              | 173 us: 1.18x slower                                                         |
| Geometric mean       | (ref)                                                               | 1.01x slower                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240405-pythonperf1_win32-x86-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|------------------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 22.2 ms                                                             | 24.1 ms: 1.08x slower                                                        |
| python_startup_no_site | 18.2 ms                                                             | 21.7 ms: 1.19x slower                                                        |
| Geometric mean         | (ref)                                                               | 1.14x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240405-pythonperf1_win32-x86-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako           | 6.94 ms                                                             | 7.14 ms: 1.03x slower                                                        |
| genshi_text    | 20.1 ms                                                             | 21.6 ms: 1.08x slower                                                        |
| genshi_xml     | 44.3 ms                                                             | 47.8 ms: 1.08x slower                                                        |
| Geometric mean | (ref)                                                               | 1.06x slower                                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240405-pythonperf1_win32-x86-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 136 us                                                              | 98.7 us: 1.37x faster                                                        |
| pickle_list                | 3.57 us                                                             | 3.17 us: 1.12x faster                                                        |
| unpickle_list              | 2.93 us                                                             | 2.75 us: 1.07x faster                                                        |
| asyncio_tcp                | 662 ms                                                              | 628 ms: 1.05x faster                                                         |
| pickle_dict                | 20.8 us                                                             | 19.8 us: 1.05x faster                                                        |
| coroutines                 | 15.5 ms                                                             | 14.9 ms: 1.04x faster                                                        |
| sqlite_synth               | 1.96 us                                                             | 1.90 us: 1.03x faster                                                        |
| create_gc_cycles           | 756 us                                                              | 738 us: 1.02x faster                                                         |
| json_loads                 | 20.5 us                                                             | 20.1 us: 1.02x faster                                                        |
| sympy_expand               | 375 ms                                                              | 368 ms: 1.02x faster                                                         |
| pickle                     | 8.07 us                                                             | 7.95 us: 1.02x faster                                                        |
| json                       | 4.10 ms                                                             | 4.04 ms: 1.01x faster                                                        |
| json_dumps                 | 6.84 ms                                                             | 6.76 ms: 1.01x faster                                                        |
| pidigits                   | 199 ms                                                              | 198 ms: 1.00x faster                                                         |
| html5lib                   | 45.4 ms                                                             | 45.9 ms: 1.01x slower                                                        |
| gc_traversal               | 1.43 ms                                                             | 1.45 ms: 1.01x slower                                                        |
| deepcopy_reduce            | 2.59 us                                                             | 2.62 us: 1.01x slower                                                        |
| xml_etree_generate         | 59.6 ms                                                             | 60.4 ms: 1.01x slower                                                        |
| unpickle                   | 9.79 us                                                             | 9.95 us: 1.02x slower                                                        |
| xml_etree_iterparse        | 64.2 ms                                                             | 65.4 ms: 1.02x slower                                                        |
| async_tree_io_tg           | 529 ms                                                              | 542 ms: 1.02x slower                                                         |
| pylint                     | 217 ms                                                              | 222 ms: 1.02x slower                                                         |
| tornado_http               | 94.3 ms                                                             | 96.6 ms: 1.02x slower                                                        |
| xml_etree_parse            | 104 ms                                                              | 107 ms: 1.02x slower                                                         |
| xml_etree_process          | 42.1 ms                                                             | 43.2 ms: 1.03x slower                                                        |
| sympy_str                  | 211 ms                                                              | 217 ms: 1.03x slower                                                         |
| mako                       | 6.94 ms                                                             | 7.14 ms: 1.03x slower                                                        |
| async_tree_cpu_io_mixed    | 471 ms                                                              | 486 ms: 1.03x slower                                                         |
| float                      | 52.4 ms                                                             | 54.0 ms: 1.03x slower                                                        |
| async_tree_cpu_io_mixed_tg | 447 ms                                                              | 461 ms: 1.03x slower                                                         |
| regex_v8                   | 15.7 ms                                                             | 16.2 ms: 1.03x slower                                                        |
| sympy_sum                  | 105 ms                                                              | 109 ms: 1.03x slower                                                         |
| pathlib                    | 83.9 ms                                                             | 86.7 ms: 1.03x slower                                                        |
| pickle_pure_python         | 213 us                                                              | 221 us: 1.04x slower                                                         |
| logging_silent             | 57.9 ns                                                             | 60.0 ns: 1.04x slower                                                        |
| async_tree_memoization     | 275 ms                                                              | 286 ms: 1.04x slower                                                         |
| sqlglot_transpile          | 1.19 ms                                                             | 1.24 ms: 1.04x slower                                                        |
| sqlglot_parse              | 964 us                                                              | 1.00 ms: 1.04x slower                                                        |
| async_tree_memoization_tg  | 254 ms                                                              | 265 ms: 1.04x slower                                                         |
| bench_mp_pool              | 69.4 ms                                                             | 72.5 ms: 1.04x slower                                                        |
| async_tree_none            | 228 ms                                                              | 238 ms: 1.05x slower                                                         |
| regex_dna                  | 118 ms                                                              | 124 ms: 1.05x slower                                                         |
| deepcopy                   | 280 us                                                              | 294 us: 1.05x slower                                                         |
| generators                 | 21.2 ms                                                             | 22.4 ms: 1.06x slower                                                        |
| tomli_loads                | 1.65 sec                                                            | 1.75 sec: 1.06x slower                                                       |
| spectral_norm              | 68.0 ms                                                             | 72.3 ms: 1.06x slower                                                        |
| telco                      | 6.03 ms                                                             | 6.42 ms: 1.06x slower                                                        |
| async_generators           | 266 ms                                                              | 283 ms: 1.06x slower                                                         |
| async_tree_none_tg         | 203 ms                                                              | 216 ms: 1.06x slower                                                         |
| docutils                   | 1.81 sec                                                            | 1.94 sec: 1.07x slower                                                       |
| logging_format             | 8.13 us                                                             | 8.73 us: 1.07x slower                                                        |
| genshi_text                | 20.1 ms                                                             | 21.6 ms: 1.08x slower                                                        |
| deepcopy_memo              | 23.5 us                                                             | 25.3 us: 1.08x slower                                                        |
| chameleon                  | 5.71 ms                                                             | 6.16 ms: 1.08x slower                                                        |
| logging_simple             | 7.47 us                                                             | 8.06 us: 1.08x slower                                                        |
| genshi_xml                 | 44.3 ms                                                             | 47.8 ms: 1.08x slower                                                        |
| pycparser                  | 777 ms                                                              | 841 ms: 1.08x slower                                                         |
| python_startup             | 22.2 ms                                                             | 24.1 ms: 1.08x slower                                                        |
| 2to3                       | 233 ms                                                              | 255 ms: 1.09x slower                                                         |
| thrift                     | 9.73 ms                                                             | 10.7 ms: 1.10x slower                                                        |
| mdp                        | 1.60 sec                                                            | 1.76 sec: 1.10x slower                                                       |
| sympy_integrate            | 14.6 ms                                                             | 16.2 ms: 1.11x slower                                                        |
| scimark_sparse_mat_mult    | 2.87 ms                                                             | 3.18 ms: 1.11x slower                                                        |
| richards                   | 31.2 ms                                                             | 35.1 ms: 1.12x slower                                                        |
| regex_compile              | 99.9 ms                                                             | 112 ms: 1.12x slower                                                         |
| meteor_contest             | 74.1 ms                                                             | 83.4 ms: 1.13x slower                                                        |
| richards_super             | 35.5 ms                                                             | 40.0 ms: 1.13x slower                                                        |
| crypto_pyaes               | 55.8 ms                                                             | 63.4 ms: 1.14x slower                                                        |
| sqlglot_normalize          | 206 ms                                                              | 235 ms: 1.14x slower                                                         |
| sqlglot_optimize           | 39.7 ms                                                             | 46.4 ms: 1.17x slower                                                        |
| unpickle_pure_python       | 147 us                                                              | 173 us: 1.18x slower                                                         |
| raytrace                   | 189 ms                                                              | 222 ms: 1.18x slower                                                         |
| python_startup_no_site     | 18.2 ms                                                             | 21.7 ms: 1.19x slower                                                        |
| pyflate                    | 308 ms                                                              | 368 ms: 1.20x slower                                                         |
| scimark_fft                | 198 ms                                                              | 237 ms: 1.20x slower                                                         |
| scimark_sor                | 81.0 ms                                                             | 97.3 ms: 1.20x slower                                                        |
| go                         | 101 ms                                                              | 121 ms: 1.20x slower                                                         |
| fannkuch                   | 270 ms                                                              | 327 ms: 1.21x slower                                                         |
| chaos                      | 48.0 ms                                                             | 58.8 ms: 1.23x slower                                                        |
| deltablue                  | 2.23 ms                                                             | 2.74 ms: 1.23x slower                                                        |
| pprint_pformat             | 1.24 sec                                                            | 1.54 sec: 1.25x slower                                                       |
| pprint_safe_repr           | 607 ms                                                              | 757 ms: 1.25x slower                                                         |
| nbody                      | 76.9 ms                                                             | 96.4 ms: 1.25x slower                                                        |
| comprehensions             | 11.9 us                                                             | 15.7 us: 1.32x slower                                                        |
| nqueens                    | 68.7 ms                                                             | 93.0 ms: 1.35x slower                                                        |
| scimark_monte_carlo        | 45.2 ms                                                             | 61.2 ms: 1.35x slower                                                        |
| scimark_lu                 | 59.4 ms                                                             | 86.1 ms: 1.45x slower                                                        |
| hexiom                     | 4.23 ms                                                             | 6.14 ms: 1.45x slower                                                        |
| coverage                   | 307 ms                                                              | 505 ms: 1.65x slower                                                         |
| Geometric mean             | (ref)                                                               | 1.08x slower                                                                 |

Benchmark hidden because not significant (4): asyncio_tcp_ssl, bench_thread_pool, regex_effbot, async_tree_io
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17.json: django_template, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.05x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: unknown