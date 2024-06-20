# Results vs. 3.13.0b2

- fork: python
- ref: 434bc593df4c0274b8af
- machine: windows-x86
- commit hash: 434bc59
- commit date: 2024-04-04
- overall geometric mean: 1.08x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf1_win32-x86-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 233 ms                                                              | 258 ms: 1.11x slower                                                            |
| chameleon      | 5.71 ms                                                             | 6.05 ms: 1.06x slower                                                           |
| docutils       | 1.81 sec                                                            | 1.91 sec: 1.05x slower                                                          |
| html5lib       | 45.4 ms                                                             | 45.7 ms: 1.00x slower                                                           |
| tornado_http   | 94.3 ms                                                             | 95.3 ms: 1.01x slower                                                           |
| Geometric mean | (ref)                                                               | 1.05x slower                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf1_win32-x86-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|---------------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed   | 471 ms                                                              | 483 ms: 1.02x slower                                                            |
| async_tree_io_tg          | 529 ms                                                              | 543 ms: 1.03x slower                                                            |
| async_tree_memoization    | 275 ms                                                              | 286 ms: 1.04x slower                                                            |
| async_tree_memoization_tg | 254 ms                                                              | 265 ms: 1.04x slower                                                            |
| async_tree_none           | 228 ms                                                              | 238 ms: 1.04x slower                                                            |
| async_tree_none_tg        | 203 ms                                                              | 215 ms: 1.06x slower                                                            |
| Geometric mean            | (ref)                                                               | 1.03x slower                                                                    |

Benchmark hidden because not significant (2): async_tree_cpu_io_mixed_tg, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf1_win32-x86-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| float          | 52.4 ms                                                             | 53.3 ms: 1.02x slower                                                           |
| nbody          | 76.9 ms                                                             | 101 ms: 1.31x slower                                                            |
| Geometric mean | (ref)                                                               | 1.10x slower                                                                    |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf1_win32-x86-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_dna      | 118 ms                                                              | 118 ms: 1.00x slower                                                            |
| regex_effbot   | 1.88 ms                                                             | 1.90 ms: 1.01x slower                                                           |
| regex_v8       | 15.7 ms                                                             | 16.3 ms: 1.03x slower                                                           |
| regex_compile  | 99.9 ms                                                             | 112 ms: 1.12x slower                                                            |
| Geometric mean | (ref)                                                               | 1.04x slower                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf1_win32-x86-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| pickle_list          | 3.57 us                                                             | 3.17 us: 1.12x faster                                                           |
| pickle_dict          | 20.8 us                                                             | 20.0 us: 1.04x faster                                                           |
| json_loads           | 20.5 us                                                             | 19.8 us: 1.04x faster                                                           |
| pickle               | 8.07 us                                                             | 7.87 us: 1.03x faster                                                           |
| unpickle_list        | 2.93 us                                                             | 2.91 us: 1.01x faster                                                           |
| unpickle             | 9.79 us                                                             | 9.86 us: 1.01x slower                                                           |
| xml_etree_generate   | 59.6 ms                                                             | 60.7 ms: 1.02x slower                                                           |
| xml_etree_iterparse  | 64.2 ms                                                             | 65.4 ms: 1.02x slower                                                           |
| xml_etree_process    | 42.1 ms                                                             | 43.0 ms: 1.02x slower                                                           |
| xml_etree_parse      | 104 ms                                                              | 108 ms: 1.03x slower                                                            |
| pickle_pure_python   | 213 us                                                              | 223 us: 1.04x slower                                                            |
| tomli_loads          | 1.65 sec                                                            | 1.75 sec: 1.06x slower                                                          |
| unpickle_pure_python | 147 us                                                              | 170 us: 1.16x slower                                                            |
| Geometric mean       | (ref)                                                               | 1.01x slower                                                                    |

Benchmark hidden because not significant (1): json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf1_win32-x86-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|------------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup         | 22.2 ms                                                             | 24.6 ms: 1.11x slower                                                           |
| python_startup_no_site | 18.2 ms                                                             | 22.4 ms: 1.23x slower                                                           |
| Geometric mean         | (ref)                                                               | 1.17x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf1_win32-x86-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako           | 6.94 ms                                                             | 7.13 ms: 1.03x slower                                                           |
| genshi_text    | 20.1 ms                                                             | 21.6 ms: 1.07x slower                                                           |
| genshi_xml     | 44.3 ms                                                             | 47.6 ms: 1.07x slower                                                           |
| Geometric mean | (ref)                                                               | 1.06x slower                                                                    |

All benchmarks:
===============

| Benchmark                 | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf1_win32-x86-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|---------------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols  | 136 us                                                              | 99.8 us: 1.36x faster                                                           |
| pickle_list               | 3.57 us                                                             | 3.17 us: 1.12x faster                                                           |
| asyncio_tcp               | 662 ms                                                              | 626 ms: 1.06x faster                                                            |
| pickle_dict               | 20.8 us                                                             | 20.0 us: 1.04x faster                                                           |
| json_loads                | 20.5 us                                                             | 19.8 us: 1.04x faster                                                           |
| coroutines                | 15.5 ms                                                             | 15.0 ms: 1.03x faster                                                           |
| pickle                    | 8.07 us                                                             | 7.87 us: 1.03x faster                                                           |
| json                      | 4.10 ms                                                             | 4.01 ms: 1.02x faster                                                           |
| create_gc_cycles          | 756 us                                                              | 740 us: 1.02x faster                                                            |
| sqlite_synth              | 1.96 us                                                             | 1.94 us: 1.01x faster                                                           |
| unpickle_list             | 2.93 us                                                             | 2.91 us: 1.01x faster                                                           |
| regex_dna                 | 118 ms                                                              | 118 ms: 1.00x slower                                                            |
| html5lib                  | 45.4 ms                                                             | 45.7 ms: 1.00x slower                                                           |
| unpickle                  | 9.79 us                                                             | 9.86 us: 1.01x slower                                                           |
| regex_effbot              | 1.88 ms                                                             | 1.90 ms: 1.01x slower                                                           |
| tornado_http              | 94.3 ms                                                             | 95.3 ms: 1.01x slower                                                           |
| xml_etree_generate        | 59.6 ms                                                             | 60.7 ms: 1.02x slower                                                           |
| gc_traversal              | 1.43 ms                                                             | 1.46 ms: 1.02x slower                                                           |
| float                     | 52.4 ms                                                             | 53.3 ms: 1.02x slower                                                           |
| xml_etree_iterparse       | 64.2 ms                                                             | 65.4 ms: 1.02x slower                                                           |
| sympy_expand              | 375 ms                                                              | 383 ms: 1.02x slower                                                            |
| xml_etree_process         | 42.1 ms                                                             | 43.0 ms: 1.02x slower                                                           |
| pylint                    | 217 ms                                                              | 222 ms: 1.02x slower                                                            |
| pathlib                   | 83.9 ms                                                             | 85.9 ms: 1.02x slower                                                           |
| async_tree_cpu_io_mixed   | 471 ms                                                              | 483 ms: 1.02x slower                                                            |
| async_tree_io_tg          | 529 ms                                                              | 543 ms: 1.03x slower                                                            |
| mako                      | 6.94 ms                                                             | 7.13 ms: 1.03x slower                                                           |
| sqlglot_parse             | 964 us                                                              | 990 us: 1.03x slower                                                            |
| xml_etree_parse           | 104 ms                                                              | 108 ms: 1.03x slower                                                            |
| regex_v8                  | 15.7 ms                                                             | 16.3 ms: 1.03x slower                                                           |
| deepcopy_reduce           | 2.59 us                                                             | 2.68 us: 1.03x slower                                                           |
| deepcopy                  | 280 us                                                              | 290 us: 1.04x slower                                                            |
| logging_silent            | 57.9 ns                                                             | 60.1 ns: 1.04x slower                                                           |
| async_tree_memoization    | 275 ms                                                              | 286 ms: 1.04x slower                                                            |
| sqlglot_transpile         | 1.19 ms                                                             | 1.24 ms: 1.04x slower                                                           |
| async_tree_memoization_tg | 254 ms                                                              | 265 ms: 1.04x slower                                                            |
| async_tree_none           | 228 ms                                                              | 238 ms: 1.04x slower                                                            |
| pickle_pure_python        | 213 us                                                              | 223 us: 1.04x slower                                                            |
| bench_mp_pool             | 69.4 ms                                                             | 72.5 ms: 1.05x slower                                                           |
| spectral_norm             | 68.0 ms                                                             | 71.5 ms: 1.05x slower                                                           |
| docutils                  | 1.81 sec                                                            | 1.91 sec: 1.05x slower                                                          |
| sympy_str                 | 211 ms                                                              | 222 ms: 1.05x slower                                                            |
| deepcopy_memo             | 23.5 us                                                             | 24.9 us: 1.06x slower                                                           |
| chameleon                 | 5.71 ms                                                             | 6.05 ms: 1.06x slower                                                           |
| async_tree_none_tg        | 203 ms                                                              | 215 ms: 1.06x slower                                                            |
| telco                     | 6.03 ms                                                             | 6.40 ms: 1.06x slower                                                           |
| logging_format            | 8.13 us                                                             | 8.65 us: 1.06x slower                                                           |
| tomli_loads               | 1.65 sec                                                            | 1.75 sec: 1.06x slower                                                          |
| sympy_sum                 | 105 ms                                                              | 112 ms: 1.07x slower                                                            |
| richards                  | 31.2 ms                                                             | 33.4 ms: 1.07x slower                                                           |
| genshi_text               | 20.1 ms                                                             | 21.6 ms: 1.07x slower                                                           |
| genshi_xml                | 44.3 ms                                                             | 47.6 ms: 1.07x slower                                                           |
| logging_simple            | 7.47 us                                                             | 8.02 us: 1.07x slower                                                           |
| generators                | 21.2 ms                                                             | 22.8 ms: 1.08x slower                                                           |
| richards_super            | 35.5 ms                                                             | 38.2 ms: 1.08x slower                                                           |
| async_generators          | 266 ms                                                              | 287 ms: 1.08x slower                                                            |
| pycparser                 | 777 ms                                                              | 839 ms: 1.08x slower                                                            |
| thrift                    | 9.73 ms                                                             | 10.6 ms: 1.09x slower                                                           |
| mdp                       | 1.60 sec                                                            | 1.77 sec: 1.10x slower                                                          |
| 2to3                      | 233 ms                                                              | 258 ms: 1.11x slower                                                            |
| python_startup            | 22.2 ms                                                             | 24.6 ms: 1.11x slower                                                           |
| meteor_contest            | 74.1 ms                                                             | 82.5 ms: 1.11x slower                                                           |
| regex_compile             | 99.9 ms                                                             | 112 ms: 1.12x slower                                                            |
| sympy_integrate           | 14.6 ms                                                             | 16.4 ms: 1.12x slower                                                           |
| scimark_sparse_mat_mult   | 2.87 ms                                                             | 3.22 ms: 1.12x slower                                                           |
| crypto_pyaes              | 55.8 ms                                                             | 63.6 ms: 1.14x slower                                                           |
| sqlglot_normalize         | 206 ms                                                              | 235 ms: 1.14x slower                                                            |
| unpickle_pure_python      | 147 us                                                              | 170 us: 1.16x slower                                                            |
| raytrace                  | 189 ms                                                              | 222 ms: 1.18x slower                                                            |
| sqlglot_optimize          | 39.7 ms                                                             | 46.8 ms: 1.18x slower                                                           |
| pyflate                   | 308 ms                                                              | 364 ms: 1.18x slower                                                            |
| go                        | 101 ms                                                              | 119 ms: 1.18x slower                                                            |
| deltablue                 | 2.23 ms                                                             | 2.70 ms: 1.21x slower                                                           |
| pprint_safe_repr          | 607 ms                                                              | 732 ms: 1.21x slower                                                            |
| fannkuch                  | 270 ms                                                              | 327 ms: 1.21x slower                                                            |
| pprint_pformat            | 1.24 sec                                                            | 1.50 sec: 1.21x slower                                                          |
| python_startup_no_site    | 18.2 ms                                                             | 22.4 ms: 1.23x slower                                                           |
| scimark_fft               | 198 ms                                                              | 244 ms: 1.23x slower                                                            |
| chaos                     | 48.0 ms                                                             | 60.2 ms: 1.26x slower                                                           |
| scimark_sor               | 81.0 ms                                                             | 103 ms: 1.27x slower                                                            |
| nbody                     | 76.9 ms                                                             | 101 ms: 1.31x slower                                                            |
| comprehensions            | 11.9 us                                                             | 15.6 us: 1.31x slower                                                           |
| nqueens                   | 68.7 ms                                                             | 92.2 ms: 1.34x slower                                                           |
| scimark_monte_carlo       | 45.2 ms                                                             | 60.9 ms: 1.35x slower                                                           |
| hexiom                    | 4.23 ms                                                             | 6.09 ms: 1.44x slower                                                           |
| scimark_lu                | 59.4 ms                                                             | 88.9 ms: 1.50x slower                                                           |
| coverage                  | 307 ms                                                              | 514 ms: 1.67x slower                                                            |
| Geometric mean            | (ref)                                                               | 1.08x slower                                                                    |

Benchmark hidden because not significant (6): asyncio_tcp_ssl, json_dumps, pidigits, async_tree_cpu_io_mixed_tg, async_tree_io, bench_thread_pool
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17.json: django_template, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.05x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: unknown