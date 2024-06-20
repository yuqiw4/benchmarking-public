# Results vs. 3.13.0b2

- fork: python
- ref: dcaf33a41d5d220523d7
- machine: windows-x86
- commit hash: dcaf33a
- commit date: 2024-03-20
- overall geometric mean: 1.28x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240320-pythonperf1_win32-x86-python-dcaf33a41d5d220523d7-3.13.0a5+-dcaf33a |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 233 ms                                                              | 266 ms: 1.14x slower                                                            |
| chameleon      | 5.71 ms                                                             | 5.84 ms: 1.02x slower                                                           |
| docutils       | 1.81 sec                                                            | 2.45 sec: 1.35x slower                                                          |
| html5lib       | 45.4 ms                                                             | 50.2 ms: 1.10x slower                                                           |
| tornado_http   | 94.3 ms                                                             | 97.2 ms: 1.03x slower                                                           |
| Geometric mean | (ref)                                                               | 1.12x slower                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240320-pythonperf1_win32-x86-python-dcaf33a41d5d220523d7-3.13.0a5+-dcaf33a |
|----------------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed    | 471 ms                                                              | 1.57 sec: 3.32x slower                                                          |
| async_tree_cpu_io_mixed_tg | 447 ms                                                              | 1.61 sec: 3.59x slower                                                          |
| async_tree_none            | 228 ms                                                              | 1.20 sec: 5.26x slower                                                          |
| async_tree_memoization     | 275 ms                                                              | 1.47 sec: 5.33x slower                                                          |
| async_tree_memoization_tg  | 254 ms                                                              | 1.47 sec: 5.81x slower                                                          |
| async_tree_none_tg         | 203 ms                                                              | 1.24 sec: 6.09x slower                                                          |
| async_tree_io              | 530 ms                                                              | 4.63 sec: 8.74x slower                                                          |
| async_tree_io_tg           | 529 ms                                                              | 4.73 sec: 8.93x slower                                                          |
| Geometric mean             | (ref)                                                               | 5.57x slower                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240320-pythonperf1_win32-x86-python-dcaf33a41d5d220523d7-3.13.0a5+-dcaf33a |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| nbody          | 76.9 ms                                                             | 100 ms: 1.30x slower                                                            |
| float          | 52.4 ms                                                             | 82.2 ms: 1.57x slower                                                           |
| Geometric mean | (ref)                                                               | 1.27x slower                                                                    |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240320-pythonperf1_win32-x86-python-dcaf33a41d5d220523d7-3.13.0a5+-dcaf33a |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_v8       | 15.7 ms                                                             | 16.0 ms: 1.02x slower                                                           |
| regex_effbot   | 1.88 ms                                                             | 1.95 ms: 1.03x slower                                                           |
| regex_dna      | 118 ms                                                              | 124 ms: 1.05x slower                                                            |
| regex_compile  | 99.9 ms                                                             | 110 ms: 1.10x slower                                                            |
| Geometric mean | (ref)                                                               | 1.05x slower                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240320-pythonperf1_win32-x86-python-dcaf33a41d5d220523d7-3.13.0a5+-dcaf33a |
|----------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| pickle_dict          | 20.8 us                                                             | 20.0 us: 1.04x faster                                                           |
| pickle_list          | 3.57 us                                                             | 3.46 us: 1.03x faster                                                           |
| json_loads           | 20.5 us                                                             | 20.1 us: 1.02x faster                                                           |
| pickle               | 8.07 us                                                             | 8.00 us: 1.01x faster                                                           |
| pickle_pure_python   | 213 us                                                              | 215 us: 1.01x slower                                                            |
| json_dumps           | 6.84 ms                                                             | 6.93 ms: 1.01x slower                                                           |
| unpickle_list        | 2.93 us                                                             | 3.04 us: 1.04x slower                                                           |
| tomli_loads          | 1.65 sec                                                            | 1.72 sec: 1.04x slower                                                          |
| unpickle             | 9.79 us                                                             | 10.5 us: 1.07x slower                                                           |
| xml_etree_process    | 42.1 ms                                                             | 47.6 ms: 1.13x slower                                                           |
| xml_etree_generate   | 59.6 ms                                                             | 69.1 ms: 1.16x slower                                                           |
| unpickle_pure_python | 147 us                                                              | 174 us: 1.18x slower                                                            |
| xml_etree_parse      | 104 ms                                                              | 133 ms: 1.28x slower                                                            |
| xml_etree_iterparse  | 64.2 ms                                                             | 93.8 ms: 1.46x slower                                                           |
| Geometric mean       | (ref)                                                               | 1.08x slower                                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240320-pythonperf1_win32-x86-python-dcaf33a41d5d220523d7-3.13.0a5+-dcaf33a |
|------------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup         | 22.2 ms                                                             | 26.6 ms: 1.20x slower                                                           |
| python_startup_no_site | 18.2 ms                                                             | 24.2 ms: 1.33x slower                                                           |
| Geometric mean         | (ref)                                                               | 1.26x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240320-pythonperf1_win32-x86-python-dcaf33a41d5d220523d7-3.13.0a5+-dcaf33a |
|-----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako            | 6.94 ms                                                             | 7.15 ms: 1.03x slower                                                           |
| django_template | 30.1 ms                                                             | 31.1 ms: 1.03x slower                                                           |
| genshi_xml      | 44.3 ms                                                             | 50.0 ms: 1.13x slower                                                           |
| genshi_text     | 20.1 ms                                                             | 22.8 ms: 1.13x slower                                                           |
| Geometric mean  | (ref)                                                               | 1.08x slower                                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240320-pythonperf1_win32-x86-python-dcaf33a41d5d220523d7-3.13.0a5+-dcaf33a |
|----------------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 136 us                                                              | 98.8 us: 1.37x faster                                                           |
| create_gc_cycles           | 756 us                                                              | 664 us: 1.14x faster                                                            |
| gc_traversal               | 1.43 ms                                                             | 1.27 ms: 1.13x faster                                                           |
| asyncio_tcp                | 662 ms                                                              | 629 ms: 1.05x faster                                                            |
| coroutines                 | 15.5 ms                                                             | 14.9 ms: 1.04x faster                                                           |
| pickle_dict                | 20.8 us                                                             | 20.0 us: 1.04x faster                                                           |
| deepcopy_reduce            | 2.59 us                                                             | 2.51 us: 1.03x faster                                                           |
| pickle_list                | 3.57 us                                                             | 3.46 us: 1.03x faster                                                           |
| json_loads                 | 20.5 us                                                             | 20.1 us: 1.02x faster                                                           |
| asyncio_tcp_ssl            | 16.9 sec                                                            | 16.7 sec: 1.01x faster                                                          |
| sympy_expand               | 375 ms                                                              | 371 ms: 1.01x faster                                                            |
| pickle                     | 8.07 us                                                             | 8.00 us: 1.01x faster                                                           |
| sqlite_synth               | 1.96 us                                                             | 1.95 us: 1.01x faster                                                           |
| pickle_pure_python         | 213 us                                                              | 215 us: 1.01x slower                                                            |
| json_dumps                 | 6.84 ms                                                             | 6.93 ms: 1.01x slower                                                           |
| regex_v8                   | 15.7 ms                                                             | 16.0 ms: 1.02x slower                                                           |
| chameleon                  | 5.71 ms                                                             | 5.84 ms: 1.02x slower                                                           |
| bench_thread_pool          | 985 us                                                              | 1.01 ms: 1.03x slower                                                           |
| pathlib                    | 83.9 ms                                                             | 86.3 ms: 1.03x slower                                                           |
| tornado_http               | 94.3 ms                                                             | 97.2 ms: 1.03x slower                                                           |
| mako                       | 6.94 ms                                                             | 7.15 ms: 1.03x slower                                                           |
| deepcopy                   | 280 us                                                              | 289 us: 1.03x slower                                                            |
| django_template            | 30.1 ms                                                             | 31.1 ms: 1.03x slower                                                           |
| regex_effbot               | 1.88 ms                                                             | 1.95 ms: 1.03x slower                                                           |
| unpickle_list              | 2.93 us                                                             | 3.04 us: 1.04x slower                                                           |
| tomli_loads                | 1.65 sec                                                            | 1.72 sec: 1.04x slower                                                          |
| logging_silent             | 57.9 ns                                                             | 60.6 ns: 1.05x slower                                                           |
| sympy_integrate            | 14.6 ms                                                             | 15.3 ms: 1.05x slower                                                           |
| json                       | 4.10 ms                                                             | 4.30 ms: 1.05x slower                                                           |
| regex_dna                  | 118 ms                                                              | 124 ms: 1.05x slower                                                            |
| spectral_norm              | 68.0 ms                                                             | 71.6 ms: 1.05x slower                                                           |
| generators                 | 21.2 ms                                                             | 22.4 ms: 1.06x slower                                                           |
| unpickle                   | 9.79 us                                                             | 10.5 us: 1.07x slower                                                           |
| sqlglot_normalize          | 206 ms                                                              | 221 ms: 1.07x slower                                                            |
| deepcopy_memo              | 23.5 us                                                             | 25.2 us: 1.07x slower                                                           |
| sqlglot_parse              | 964 us                                                              | 1.03 ms: 1.07x slower                                                           |
| sqlglot_transpile          | 1.19 ms                                                             | 1.29 ms: 1.08x slower                                                           |
| telco                      | 6.03 ms                                                             | 6.53 ms: 1.08x slower                                                           |
| mdp                        | 1.60 sec                                                            | 1.74 sec: 1.08x slower                                                          |
| bench_mp_pool              | 69.4 ms                                                             | 75.6 ms: 1.09x slower                                                           |
| scimark_sparse_mat_mult    | 2.87 ms                                                             | 3.13 ms: 1.09x slower                                                           |
| regex_compile              | 99.9 ms                                                             | 110 ms: 1.10x slower                                                            |
| crypto_pyaes               | 55.8 ms                                                             | 61.5 ms: 1.10x slower                                                           |
| html5lib                   | 45.4 ms                                                             | 50.2 ms: 1.10x slower                                                           |
| logging_format             | 8.13 us                                                             | 9.02 us: 1.11x slower                                                           |
| thrift                     | 9.73 ms                                                             | 10.8 ms: 1.11x slower                                                           |
| logging_simple             | 7.47 us                                                             | 8.38 us: 1.12x slower                                                           |
| meteor_contest             | 74.1 ms                                                             | 83.4 ms: 1.13x slower                                                           |
| genshi_xml                 | 44.3 ms                                                             | 50.0 ms: 1.13x slower                                                           |
| xml_etree_process          | 42.1 ms                                                             | 47.6 ms: 1.13x slower                                                           |
| genshi_text                | 20.1 ms                                                             | 22.8 ms: 1.13x slower                                                           |
| 2to3                       | 233 ms                                                              | 266 ms: 1.14x slower                                                            |
| richards                   | 31.2 ms                                                             | 35.7 ms: 1.14x slower                                                           |
| sqlglot_optimize           | 39.7 ms                                                             | 45.8 ms: 1.15x slower                                                           |
| richards_super             | 35.5 ms                                                             | 40.9 ms: 1.15x slower                                                           |
| xml_etree_generate         | 59.6 ms                                                             | 69.1 ms: 1.16x slower                                                           |
| pprint_safe_repr           | 607 ms                                                              | 715 ms: 1.18x slower                                                            |
| unpickle_pure_python       | 147 us                                                              | 174 us: 1.18x slower                                                            |
| pprint_pformat             | 1.24 sec                                                            | 1.46 sec: 1.18x slower                                                          |
| deltablue                  | 2.23 ms                                                             | 2.67 ms: 1.19x slower                                                           |
| python_startup             | 22.2 ms                                                             | 26.6 ms: 1.20x slower                                                           |
| scimark_fft                | 198 ms                                                              | 239 ms: 1.21x slower                                                            |
| async_generators           | 266 ms                                                              | 322 ms: 1.21x slower                                                            |
| comprehensions             | 11.9 us                                                             | 14.4 us: 1.22x slower                                                           |
| fannkuch                   | 270 ms                                                              | 329 ms: 1.22x slower                                                            |
| pyflate                    | 308 ms                                                              | 376 ms: 1.22x slower                                                            |
| scimark_sor                | 81.0 ms                                                             | 99.3 ms: 1.23x slower                                                           |
| go                         | 101 ms                                                              | 126 ms: 1.25x slower                                                            |
| chaos                      | 48.0 ms                                                             | 60.9 ms: 1.27x slower                                                           |
| pycparser                  | 777 ms                                                              | 989 ms: 1.27x slower                                                            |
| xml_etree_parse            | 104 ms                                                              | 133 ms: 1.28x slower                                                            |
| nbody                      | 76.9 ms                                                             | 100 ms: 1.30x slower                                                            |
| nqueens                    | 68.7 ms                                                             | 90.2 ms: 1.31x slower                                                           |
| python_startup_no_site     | 18.2 ms                                                             | 24.2 ms: 1.33x slower                                                           |
| docutils                   | 1.81 sec                                                            | 2.45 sec: 1.35x slower                                                          |
| raytrace                   | 189 ms                                                              | 264 ms: 1.40x slower                                                            |
| scimark_lu                 | 59.4 ms                                                             | 83.3 ms: 1.40x slower                                                           |
| hexiom                     | 4.23 ms                                                             | 5.98 ms: 1.41x slower                                                           |
| scimark_monte_carlo        | 45.2 ms                                                             | 64.6 ms: 1.43x slower                                                           |
| xml_etree_iterparse        | 64.2 ms                                                             | 93.8 ms: 1.46x slower                                                           |
| float                      | 52.4 ms                                                             | 82.2 ms: 1.57x slower                                                           |
| coverage                   | 307 ms                                                              | 508 ms: 1.65x slower                                                            |
| pylint                     | 217 ms                                                              | 405 ms: 1.87x slower                                                            |
| async_tree_cpu_io_mixed    | 471 ms                                                              | 1.57 sec: 3.32x slower                                                          |
| async_tree_cpu_io_mixed_tg | 447 ms                                                              | 1.61 sec: 3.59x slower                                                          |
| async_tree_none            | 228 ms                                                              | 1.20 sec: 5.26x slower                                                          |
| async_tree_memoization     | 275 ms                                                              | 1.47 sec: 5.33x slower                                                          |
| async_tree_memoization_tg  | 254 ms                                                              | 1.47 sec: 5.81x slower                                                          |
| async_tree_none_tg         | 203 ms                                                              | 1.24 sec: 6.09x slower                                                          |
| async_tree_io              | 530 ms                                                              | 4.63 sec: 8.74x slower                                                          |
| async_tree_io_tg           | 529 ms                                                              | 4.73 sec: 8.93x slower                                                          |
| Geometric mean             | (ref)                                                               | 1.28x slower                                                                    |

Benchmark hidden because not significant (3): sympy_str, pidigits, sympy_sum
Ignored benchmarks (1) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17.json: flaskblogging
Ignored benchmarks (1) of results/bm-20240320-3.13.0a5+-dcaf33a-JIT/bm-20240320-pythonperf1_win32-x86-python-dcaf33a41d5d220523d7-3.13.0a5+-dcaf33a.json: unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.13x
- 95% likely to have a slowdown of 1.12x
- 99% likely to have a slowdown of 1.10x

# Memory
- memory change: unknown