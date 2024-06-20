# Results vs. 3.13.0b2

- fork: python
- ref: d610d821fd210dce63a1
- machine: windows-x86
- commit hash: d610d82
- commit date: 2024-03-23
- overall geometric mean: 1.10x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf1_win32-x86-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 233 ms                                                              | 262 ms: 1.12x slower                                                            |
| chameleon      | 5.71 ms                                                             | 6.15 ms: 1.08x slower                                                           |
| docutils       | 1.81 sec                                                            | 1.93 sec: 1.06x slower                                                          |
| html5lib       | 45.4 ms                                                             | 46.6 ms: 1.03x slower                                                           |
| tornado_http   | 94.3 ms                                                             | 99.2 ms: 1.05x slower                                                           |
| Geometric mean | (ref)                                                               | 1.07x slower                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf1_win32-x86-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|----------------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_io_tg           | 529 ms                                                              | 522 ms: 1.01x faster                                                            |
| async_tree_none            | 228 ms                                                              | 237 ms: 1.04x slower                                                            |
| async_tree_io              | 530 ms                                                              | 559 ms: 1.05x slower                                                            |
| async_tree_memoization     | 275 ms                                                              | 292 ms: 1.06x slower                                                            |
| async_tree_none_tg         | 203 ms                                                              | 216 ms: 1.07x slower                                                            |
| async_tree_memoization_tg  | 254 ms                                                              | 273 ms: 1.07x slower                                                            |
| async_tree_cpu_io_mixed_tg | 447 ms                                                              | 484 ms: 1.08x slower                                                            |
| async_tree_cpu_io_mixed    | 471 ms                                                              | 515 ms: 1.09x slower                                                            |
| Geometric mean             | (ref)                                                               | 1.06x slower                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf1_win32-x86-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| pidigits       | 199 ms                                                              | 201 ms: 1.01x slower                                                            |
| nbody          | 76.9 ms                                                             | 97.1 ms: 1.26x slower                                                           |
| Geometric mean | (ref)                                                               | 1.09x slower                                                                    |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf1_win32-x86-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_effbot   | 1.88 ms                                                             | 1.91 ms: 1.01x slower                                                           |
| regex_v8       | 15.7 ms                                                             | 16.1 ms: 1.03x slower                                                           |
| regex_dna      | 118 ms                                                              | 121 ms: 1.03x slower                                                            |
| regex_compile  | 99.9 ms                                                             | 113 ms: 1.13x slower                                                            |
| Geometric mean | (ref)                                                               | 1.05x slower                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf1_win32-x86-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|----------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| pickle_list          | 3.57 us                                                             | 3.22 us: 1.11x faster                                                           |
| unpickle_list        | 2.93 us                                                             | 2.72 us: 1.08x faster                                                           |
| pickle_dict          | 20.8 us                                                             | 19.8 us: 1.05x faster                                                           |
| pickle               | 8.07 us                                                             | 7.88 us: 1.03x faster                                                           |
| json_loads           | 20.5 us                                                             | 20.3 us: 1.01x faster                                                           |
| unpickle             | 9.79 us                                                             | 10.0 us: 1.02x slower                                                           |
| xml_etree_parse      | 104 ms                                                              | 108 ms: 1.03x slower                                                            |
| tomli_loads          | 1.65 sec                                                            | 1.71 sec: 1.04x slower                                                          |
| xml_etree_iterparse  | 64.2 ms                                                             | 66.7 ms: 1.04x slower                                                           |
| xml_etree_process    | 42.1 ms                                                             | 44.0 ms: 1.04x slower                                                           |
| xml_etree_generate   | 59.6 ms                                                             | 62.4 ms: 1.05x slower                                                           |
| pickle_pure_python   | 213 us                                                              | 224 us: 1.05x slower                                                            |
| unpickle_pure_python | 147 us                                                              | 168 us: 1.14x slower                                                            |
| Geometric mean       | (ref)                                                               | 1.01x slower                                                                    |

Benchmark hidden because not significant (1): json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf1_win32-x86-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|------------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup         | 22.2 ms                                                             | 26.1 ms: 1.17x slower                                                           |
| python_startup_no_site | 18.2 ms                                                             | 23.3 ms: 1.28x slower                                                           |
| Geometric mean         | (ref)                                                               | 1.23x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf1_win32-x86-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|-----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako            | 6.94 ms                                                             | 7.20 ms: 1.04x slower                                                           |
| django_template | 30.1 ms                                                             | 32.7 ms: 1.09x slower                                                           |
| genshi_xml      | 44.3 ms                                                             | 49.8 ms: 1.13x slower                                                           |
| genshi_text     | 20.1 ms                                                             | 23.8 ms: 1.18x slower                                                           |
| Geometric mean  | (ref)                                                               | 1.11x slower                                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf1_win32-x86-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|----------------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 136 us                                                              | 93.9 us: 1.44x faster                                                           |
| create_gc_cycles           | 756 us                                                              | 646 us: 1.17x faster                                                            |
| pickle_list                | 3.57 us                                                             | 3.22 us: 1.11x faster                                                           |
| unpickle_list              | 2.93 us                                                             | 2.72 us: 1.08x faster                                                           |
| pickle_dict                | 20.8 us                                                             | 19.8 us: 1.05x faster                                                           |
| asyncio_tcp                | 662 ms                                                              | 634 ms: 1.04x faster                                                            |
| gc_traversal               | 1.43 ms                                                             | 1.38 ms: 1.04x faster                                                           |
| coroutines                 | 15.5 ms                                                             | 15.1 ms: 1.03x faster                                                           |
| pickle                     | 8.07 us                                                             | 7.88 us: 1.03x faster                                                           |
| sqlite_synth               | 1.96 us                                                             | 1.92 us: 1.02x faster                                                           |
| async_tree_io_tg           | 529 ms                                                              | 522 ms: 1.01x faster                                                            |
| asyncio_tcp_ssl            | 16.9 sec                                                            | 16.7 sec: 1.01x faster                                                          |
| json_loads                 | 20.5 us                                                             | 20.3 us: 1.01x faster                                                           |
| pidigits                   | 199 ms                                                              | 201 ms: 1.01x slower                                                            |
| regex_effbot               | 1.88 ms                                                             | 1.91 ms: 1.01x slower                                                           |
| unpickle                   | 9.79 us                                                             | 10.0 us: 1.02x slower                                                           |
| regex_v8                   | 15.7 ms                                                             | 16.1 ms: 1.03x slower                                                           |
| html5lib                   | 45.4 ms                                                             | 46.6 ms: 1.03x slower                                                           |
| sympy_str                  | 211 ms                                                              | 217 ms: 1.03x slower                                                            |
| regex_dna                  | 118 ms                                                              | 121 ms: 1.03x slower                                                            |
| bench_thread_pool          | 985 us                                                              | 1.01 ms: 1.03x slower                                                           |
| pathlib                    | 83.9 ms                                                             | 86.4 ms: 1.03x slower                                                           |
| xml_etree_parse            | 104 ms                                                              | 108 ms: 1.03x slower                                                            |
| deepcopy                   | 280 us                                                              | 289 us: 1.04x slower                                                            |
| mako                       | 6.94 ms                                                             | 7.20 ms: 1.04x slower                                                           |
| tomli_loads                | 1.65 sec                                                            | 1.71 sec: 1.04x slower                                                          |
| xml_etree_iterparse        | 64.2 ms                                                             | 66.7 ms: 1.04x slower                                                           |
| async_tree_none            | 228 ms                                                              | 237 ms: 1.04x slower                                                            |
| xml_etree_process          | 42.1 ms                                                             | 44.0 ms: 1.04x slower                                                           |
| xml_etree_generate         | 59.6 ms                                                             | 62.4 ms: 1.05x slower                                                           |
| tornado_http               | 94.3 ms                                                             | 99.2 ms: 1.05x slower                                                           |
| pickle_pure_python         | 213 us                                                              | 224 us: 1.05x slower                                                            |
| spectral_norm              | 68.0 ms                                                             | 71.6 ms: 1.05x slower                                                           |
| async_tree_io              | 530 ms                                                              | 559 ms: 1.05x slower                                                            |
| async_tree_memoization     | 275 ms                                                              | 292 ms: 1.06x slower                                                            |
| sympy_sum                  | 105 ms                                                              | 111 ms: 1.06x slower                                                            |
| docutils                   | 1.81 sec                                                            | 1.93 sec: 1.06x slower                                                          |
| sqlglot_parse              | 964 us                                                              | 1.03 ms: 1.06x slower                                                           |
| async_tree_none_tg         | 203 ms                                                              | 216 ms: 1.07x slower                                                            |
| bench_mp_pool              | 69.4 ms                                                             | 74.1 ms: 1.07x slower                                                           |
| telco                      | 6.03 ms                                                             | 6.46 ms: 1.07x slower                                                           |
| sqlglot_transpile          | 1.19 ms                                                             | 1.28 ms: 1.07x slower                                                           |
| async_tree_memoization_tg  | 254 ms                                                              | 273 ms: 1.07x slower                                                            |
| chameleon                  | 5.71 ms                                                             | 6.15 ms: 1.08x slower                                                           |
| async_tree_cpu_io_mixed_tg | 447 ms                                                              | 484 ms: 1.08x slower                                                            |
| django_template            | 30.1 ms                                                             | 32.7 ms: 1.09x slower                                                           |
| async_tree_cpu_io_mixed    | 471 ms                                                              | 515 ms: 1.09x slower                                                            |
| crypto_pyaes               | 55.8 ms                                                             | 61.0 ms: 1.09x slower                                                           |
| scimark_sparse_mat_mult    | 2.87 ms                                                             | 3.14 ms: 1.09x slower                                                           |
| pycparser                  | 777 ms                                                              | 854 ms: 1.10x slower                                                            |
| async_generators           | 266 ms                                                              | 293 ms: 1.10x slower                                                            |
| pylint                     | 217 ms                                                              | 240 ms: 1.11x slower                                                            |
| logging_format             | 8.13 us                                                             | 9.06 us: 1.11x slower                                                           |
| mdp                        | 1.60 sec                                                            | 1.79 sec: 1.12x slower                                                          |
| 2to3                       | 233 ms                                                              | 262 ms: 1.12x slower                                                            |
| meteor_contest             | 74.1 ms                                                             | 83.3 ms: 1.12x slower                                                           |
| genshi_xml                 | 44.3 ms                                                             | 49.8 ms: 1.13x slower                                                           |
| logging_simple             | 7.47 us                                                             | 8.44 us: 1.13x slower                                                           |
| regex_compile              | 99.9 ms                                                             | 113 ms: 1.13x slower                                                            |
| thrift                     | 9.73 ms                                                             | 11.0 ms: 1.13x slower                                                           |
| sympy_integrate            | 14.6 ms                                                             | 16.6 ms: 1.13x slower                                                           |
| unpickle_pure_python       | 147 us                                                              | 168 us: 1.14x slower                                                            |
| deepcopy_memo              | 23.5 us                                                             | 27.3 us: 1.16x slower                                                           |
| richards_super             | 35.5 ms                                                             | 41.3 ms: 1.16x slower                                                           |
| richards                   | 31.2 ms                                                             | 36.3 ms: 1.16x slower                                                           |
| sqlglot_optimize           | 39.7 ms                                                             | 46.2 ms: 1.16x slower                                                           |
| sqlglot_normalize          | 206 ms                                                              | 240 ms: 1.17x slower                                                            |
| deltablue                  | 2.23 ms                                                             | 2.62 ms: 1.17x slower                                                           |
| python_startup             | 22.2 ms                                                             | 26.1 ms: 1.17x slower                                                           |
| genshi_text                | 20.1 ms                                                             | 23.8 ms: 1.18x slower                                                           |
| generators                 | 21.2 ms                                                             | 25.0 ms: 1.18x slower                                                           |
| logging_silent             | 57.9 ns                                                             | 69.4 ns: 1.20x slower                                                           |
| pprint_safe_repr           | 607 ms                                                              | 731 ms: 1.21x slower                                                            |
| pprint_pformat             | 1.24 sec                                                            | 1.50 sec: 1.21x slower                                                          |
| pyflate                    | 308 ms                                                              | 377 ms: 1.22x slower                                                            |
| scimark_fft                | 198 ms                                                              | 244 ms: 1.23x slower                                                            |
| chaos                      | 48.0 ms                                                             | 59.7 ms: 1.24x slower                                                           |
| fannkuch                   | 270 ms                                                              | 337 ms: 1.25x slower                                                            |
| go                         | 101 ms                                                              | 127 ms: 1.26x slower                                                            |
| nbody                      | 76.9 ms                                                             | 97.1 ms: 1.26x slower                                                           |
| scimark_sor                | 81.0 ms                                                             | 103 ms: 1.28x slower                                                            |
| python_startup_no_site     | 18.2 ms                                                             | 23.3 ms: 1.28x slower                                                           |
| comprehensions             | 11.9 us                                                             | 15.6 us: 1.32x slower                                                           |
| nqueens                    | 68.7 ms                                                             | 92.2 ms: 1.34x slower                                                           |
| scimark_lu                 | 59.4 ms                                                             | 85.0 ms: 1.43x slower                                                           |
| hexiom                     | 4.23 ms                                                             | 6.07 ms: 1.43x slower                                                           |
| scimark_monte_carlo        | 45.2 ms                                                             | 65.6 ms: 1.45x slower                                                           |
| raytrace                   | 189 ms                                                              | 280 ms: 1.48x slower                                                            |
| coverage                   | 307 ms                                                              | 484 ms: 1.58x slower                                                            |
| Geometric mean             | (ref)                                                               | 1.10x slower                                                                    |

Benchmark hidden because not significant (5): json_dumps, deepcopy_reduce, sympy_expand, json, float
Ignored benchmarks (1) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17.json: flaskblogging
Ignored benchmarks (1) of results/bm-20240323-3.13.0a5+-d610d82-JIT/bm-20240323-pythonperf1_win32-x86-python-d610d821fd210dce63a1-3.13.0a5+-d610d82.json: unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.06x

# Memory
- memory change: unknown