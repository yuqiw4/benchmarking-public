# Results vs. 3.13.0b2

- fork: brandtbucher
- ref: justin_align
- machine: windows-x86
- commit hash: 0081bcd
- commit date: 2024-05-23
- overall geometric mean: 1.06x faster
- HPT reliability: 90.81%
- HPT 99th percentile: 1.00x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240523-pythonperf1_win32-x86-brandtbucher-justin_align-3.14.0a0-0081bcd |
|----------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 233 ms                                                              | 249 ms: 1.07x slower                                                         |
| chameleon      | 5.71 ms                                                             | 6.18 ms: 1.08x slower                                                        |
| docutils       | 1.81 sec                                                            | 1.90 sec: 1.05x slower                                                       |
| html5lib       | 45.4 ms                                                             | 46.0 ms: 1.01x slower                                                        |
| tornado_http   | 94.3 ms                                                             | 97.3 ms: 1.03x slower                                                        |
| Geometric mean | (ref)                                                               | 1.05x slower                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240523-pythonperf1_win32-x86-brandtbucher-justin_align-3.14.0a0-0081bcd |
|----------------------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_io_tg           | 529 ms                                                              | 536 ms: 1.01x slower                                                         |
| async_tree_cpu_io_mixed    | 471 ms                                                              | 478 ms: 1.01x slower                                                         |
| async_tree_none            | 228 ms                                                              | 232 ms: 1.02x slower                                                         |
| async_tree_cpu_io_mixed_tg | 447 ms                                                              | 456 ms: 1.02x slower                                                         |
| async_tree_io              | 530 ms                                                              | 545 ms: 1.03x slower                                                         |
| async_tree_memoization_tg  | 254 ms                                                              | 262 ms: 1.03x slower                                                         |
| async_tree_memoization     | 275 ms                                                              | 284 ms: 1.03x slower                                                         |
| Geometric mean             | (ref)                                                               | 1.02x slower                                                                 |

Benchmark hidden because not significant (1): async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240523-pythonperf1_win32-x86-brandtbucher-justin_align-3.14.0a0-0081bcd |
|----------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| nbody          | 76.9 ms                                                             | 51.8 ms: 1.48x faster                                                        |
| float          | 52.4 ms                                                             | 40.9 ms: 1.28x faster                                                        |
| Geometric mean | (ref)                                                               | 1.24x faster                                                                 |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240523-pythonperf1_win32-x86-brandtbucher-justin_align-3.14.0a0-0081bcd |
|----------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 99.9 ms                                                             | 96.3 ms: 1.04x faster                                                        |
| regex_dna      | 118 ms                                                              | 119 ms: 1.01x slower                                                         |
| Geometric mean | (ref)                                                               | 1.01x faster                                                                 |

Benchmark hidden because not significant (2): regex_v8, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240523-pythonperf1_win32-x86-brandtbucher-justin_align-3.14.0a0-0081bcd |
|----------------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| tomli_loads          | 1.65 sec                                                            | 1.37 sec: 1.21x faster                                                       |
| unpickle_pure_python | 147 us                                                              | 137 us: 1.08x faster                                                         |
| xml_etree_iterparse  | 64.2 ms                                                             | 59.9 ms: 1.07x faster                                                        |
| pickle_pure_python   | 213 us                                                              | 204 us: 1.05x faster                                                         |
| json_dumps           | 6.84 ms                                                             | 6.63 ms: 1.03x faster                                                        |
| unpickle_list        | 2.93 us                                                             | 2.85 us: 1.03x faster                                                        |
| xml_etree_generate   | 59.6 ms                                                             | 58.0 ms: 1.03x faster                                                        |
| xml_etree_parse      | 104 ms                                                              | 102 ms: 1.02x faster                                                         |
| pickle_dict          | 20.8 us                                                             | 20.7 us: 1.00x faster                                                        |
| xml_etree_process    | 42.1 ms                                                             | 42.6 ms: 1.01x slower                                                        |
| unpickle             | 9.79 us                                                             | 10.0 us: 1.02x slower                                                        |
| json_loads           | 20.5 us                                                             | 21.0 us: 1.02x slower                                                        |
| pickle               | 8.07 us                                                             | 9.05 us: 1.12x slower                                                        |
| Geometric mean       | (ref)                                                               | 1.02x faster                                                                 |

Benchmark hidden because not significant (1): pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240523-pythonperf1_win32-x86-brandtbucher-justin_align-3.14.0a0-0081bcd |
|------------------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 22.2 ms                                                             | 24.3 ms: 1.09x slower                                                        |
| python_startup_no_site | 18.2 ms                                                             | 20.5 ms: 1.13x slower                                                        |
| Geometric mean         | (ref)                                                               | 1.11x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240523-pythonperf1_win32-x86-brandtbucher-justin_align-3.14.0a0-0081bcd |
|-----------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 6.94 ms                                                             | 5.38 ms: 1.29x faster                                                        |
| django_template | 30.1 ms                                                             | 31.7 ms: 1.05x slower                                                        |
| genshi_text     | 20.1 ms                                                             | 21.4 ms: 1.07x slower                                                        |
| genshi_xml      | 44.3 ms                                                             | 50.5 ms: 1.14x slower                                                        |
| Geometric mean  | (ref)                                                               | 1.00x faster                                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240523-pythonperf1_win32-x86-brandtbucher-justin_align-3.14.0a0-0081bcd |
|----------------------------|:-------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| thrift                     | 9.73 ms                                                             | 714 us: 13.63x faster                                                        |
| coverage                   | 307 ms                                                              | 50.3 ms: 6.11x faster                                                        |
| nbody                      | 76.9 ms                                                             | 51.8 ms: 1.48x faster                                                        |
| spectral_norm              | 68.0 ms                                                             | 47.9 ms: 1.42x faster                                                        |
| mako                       | 6.94 ms                                                             | 5.38 ms: 1.29x faster                                                        |
| float                      | 52.4 ms                                                             | 40.9 ms: 1.28x faster                                                        |
| fannkuch                   | 270 ms                                                              | 215 ms: 1.25x faster                                                         |
| scimark_sparse_mat_mult    | 2.87 ms                                                             | 2.37 ms: 1.21x faster                                                        |
| tomli_loads                | 1.65 sec                                                            | 1.37 sec: 1.21x faster                                                       |
| scimark_fft                | 198 ms                                                              | 167 ms: 1.19x faster                                                         |
| deepcopy_memo              | 23.5 us                                                             | 20.6 us: 1.14x faster                                                        |
| crypto_pyaes               | 55.8 ms                                                             | 49.6 ms: 1.12x faster                                                        |
| pprint_safe_repr           | 607 ms                                                              | 542 ms: 1.12x faster                                                         |
| pyflate                    | 308 ms                                                              | 278 ms: 1.11x faster                                                         |
| pprint_pformat             | 1.24 sec                                                            | 1.13 sec: 1.10x faster                                                       |
| scimark_monte_carlo        | 45.2 ms                                                             | 41.2 ms: 1.10x faster                                                        |
| unpickle_pure_python       | 147 us                                                              | 137 us: 1.08x faster                                                         |
| comprehensions             | 11.9 us                                                             | 11.0 us: 1.08x faster                                                        |
| xml_etree_iterparse        | 64.2 ms                                                             | 59.9 ms: 1.07x faster                                                        |
| telco                      | 6.03 ms                                                             | 5.63 ms: 1.07x faster                                                        |
| sqlite_synth               | 1.96 us                                                             | 1.85 us: 1.06x faster                                                        |
| logging_silent             | 57.9 ns                                                             | 55.0 ns: 1.05x faster                                                        |
| pickle_pure_python         | 213 us                                                              | 204 us: 1.05x faster                                                         |
| sqlglot_parse              | 964 us                                                              | 922 us: 1.05x faster                                                         |
| asyncio_tcp                | 662 ms                                                              | 634 ms: 1.04x faster                                                         |
| regex_compile              | 99.9 ms                                                             | 96.3 ms: 1.04x faster                                                        |
| json_dumps                 | 6.84 ms                                                             | 6.63 ms: 1.03x faster                                                        |
| unpickle_list              | 2.93 us                                                             | 2.85 us: 1.03x faster                                                        |
| xml_etree_generate         | 59.6 ms                                                             | 58.0 ms: 1.03x faster                                                        |
| xml_etree_parse            | 104 ms                                                              | 102 ms: 1.02x faster                                                         |
| nqueens                    | 68.7 ms                                                             | 67.5 ms: 1.02x faster                                                        |
| richards                   | 31.2 ms                                                             | 30.7 ms: 1.02x faster                                                        |
| meteor_contest             | 74.1 ms                                                             | 73.5 ms: 1.01x faster                                                        |
| logging_format             | 8.13 us                                                             | 8.07 us: 1.01x faster                                                        |
| pickle_dict                | 20.8 us                                                             | 20.7 us: 1.00x faster                                                        |
| flaskblogging              | 2.03 sec                                                            | 2.03 sec: 1.00x faster                                                       |
| mdp                        | 1.60 sec                                                            | 1.60 sec: 1.00x faster                                                       |
| sympy_expand               | 375 ms                                                              | 376 ms: 1.00x slower                                                         |
| typing_runtime_protocols   | 136 us                                                              | 137 us: 1.01x slower                                                         |
| regex_dna                  | 118 ms                                                              | 119 ms: 1.01x slower                                                         |
| logging_simple             | 7.47 us                                                             | 7.54 us: 1.01x slower                                                        |
| create_gc_cycles           | 756 us                                                              | 764 us: 1.01x slower                                                         |
| gc_traversal               | 1.43 ms                                                             | 1.45 ms: 1.01x slower                                                        |
| xml_etree_process          | 42.1 ms                                                             | 42.6 ms: 1.01x slower                                                        |
| html5lib                   | 45.4 ms                                                             | 46.0 ms: 1.01x slower                                                        |
| async_tree_io_tg           | 529 ms                                                              | 536 ms: 1.01x slower                                                         |
| async_tree_cpu_io_mixed    | 471 ms                                                              | 478 ms: 1.01x slower                                                         |
| async_tree_none            | 228 ms                                                              | 232 ms: 1.02x slower                                                         |
| async_tree_cpu_io_mixed_tg | 447 ms                                                              | 456 ms: 1.02x slower                                                         |
| unpickle                   | 9.79 us                                                             | 10.0 us: 1.02x slower                                                        |
| json_loads                 | 20.5 us                                                             | 21.0 us: 1.02x slower                                                        |
| async_tree_io              | 530 ms                                                              | 545 ms: 1.03x slower                                                         |
| async_tree_memoization_tg  | 254 ms                                                              | 262 ms: 1.03x slower                                                         |
| pathlib                    | 83.9 ms                                                             | 86.4 ms: 1.03x slower                                                        |
| async_tree_memoization     | 275 ms                                                              | 284 ms: 1.03x slower                                                         |
| sympy_sum                  | 105 ms                                                              | 108 ms: 1.03x slower                                                         |
| tornado_http               | 94.3 ms                                                             | 97.3 ms: 1.03x slower                                                        |
| pycparser                  | 777 ms                                                              | 804 ms: 1.03x slower                                                         |
| chaos                      | 48.0 ms                                                             | 49.8 ms: 1.04x slower                                                        |
| coroutines                 | 15.5 ms                                                             | 16.2 ms: 1.05x slower                                                        |
| json                       | 4.10 ms                                                             | 4.30 ms: 1.05x slower                                                        |
| docutils                   | 1.81 sec                                                            | 1.90 sec: 1.05x slower                                                       |
| hexiom                     | 4.23 ms                                                             | 4.45 ms: 1.05x slower                                                        |
| django_template            | 30.1 ms                                                             | 31.7 ms: 1.05x slower                                                        |
| deepcopy_reduce            | 2.59 us                                                             | 2.75 us: 1.06x slower                                                        |
| sqlglot_optimize           | 39.7 ms                                                             | 42.3 ms: 1.06x slower                                                        |
| genshi_text                | 20.1 ms                                                             | 21.4 ms: 1.07x slower                                                        |
| sympy_integrate            | 14.6 ms                                                             | 15.7 ms: 1.07x slower                                                        |
| 2to3                       | 233 ms                                                              | 249 ms: 1.07x slower                                                         |
| sqlglot_normalize          | 206 ms                                                              | 221 ms: 1.07x slower                                                         |
| raytrace                   | 189 ms                                                              | 202 ms: 1.07x slower                                                         |
| deepcopy                   | 280 us                                                              | 300 us: 1.07x slower                                                         |
| go                         | 101 ms                                                              | 108 ms: 1.08x slower                                                         |
| bench_mp_pool              | 69.4 ms                                                             | 74.8 ms: 1.08x slower                                                        |
| chameleon                  | 5.71 ms                                                             | 6.18 ms: 1.08x slower                                                        |
| python_startup             | 22.2 ms                                                             | 24.3 ms: 1.09x slower                                                        |
| async_generators           | 266 ms                                                              | 291 ms: 1.10x slower                                                         |
| scimark_sor                | 81.0 ms                                                             | 89.4 ms: 1.10x slower                                                        |
| generators                 | 21.2 ms                                                             | 23.4 ms: 1.10x slower                                                        |
| pylint                     | 217 ms                                                              | 241 ms: 1.11x slower                                                         |
| pickle                     | 8.07 us                                                             | 9.05 us: 1.12x slower                                                        |
| python_startup_no_site     | 18.2 ms                                                             | 20.5 ms: 1.13x slower                                                        |
| genshi_xml                 | 44.3 ms                                                             | 50.5 ms: 1.14x slower                                                        |
| deltablue                  | 2.23 ms                                                             | 2.55 ms: 1.14x slower                                                        |
| scimark_lu                 | 59.4 ms                                                             | 70.6 ms: 1.19x slower                                                        |
| Geometric mean             | (ref)                                                               | 1.06x faster                                                                 |

Benchmark hidden because not significant (10): regex_v8, sqlglot_transpile, regex_effbot, pidigits, richards_super, sympy_str, asyncio_tcp_ssl, pickle_list, async_tree_none_tg, bench_thread_pool

# HPT report

- Reliability score: 90.81% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: unknown