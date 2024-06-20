# Results vs. 3.13.0b2

- fork: python
- ref: 15fbd53ba96be4b6a5ab
- machine: windows-x86
- commit hash: 15fbd53
- commit date: 2024-04-20
- overall geometric mean: 1.07x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 233 ms                                                              | 253 ms: 1.08x slower                                                            |
| chameleon      | 5.71 ms                                                             | 6.02 ms: 1.05x slower                                                           |
| docutils       | 1.81 sec                                                            | 1.91 sec: 1.06x slower                                                          |
| html5lib       | 45.4 ms                                                             | 45.0 ms: 1.01x faster                                                           |
| tornado_http   | 94.3 ms                                                             | 95.0 ms: 1.01x slower                                                           |
| Geometric mean | (ref)                                                               | 1.04x slower                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 447 ms                                                              | 456 ms: 1.02x slower                                                            |
| async_tree_io_tg           | 529 ms                                                              | 542 ms: 1.02x slower                                                            |
| async_tree_cpu_io_mixed    | 471 ms                                                              | 484 ms: 1.03x slower                                                            |
| async_tree_memoization_tg  | 254 ms                                                              | 266 ms: 1.05x slower                                                            |
| async_tree_memoization     | 275 ms                                                              | 289 ms: 1.05x slower                                                            |
| async_tree_none            | 228 ms                                                              | 240 ms: 1.05x slower                                                            |
| async_tree_none_tg         | 203 ms                                                              | 215 ms: 1.06x slower                                                            |
| Geometric mean             | (ref)                                                               | 1.04x slower                                                                    |

Benchmark hidden because not significant (1): async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| pidigits       | 199 ms                                                              | 198 ms: 1.00x faster                                                            |
| nbody          | 76.9 ms                                                             | 92.0 ms: 1.20x slower                                                           |
| Geometric mean | (ref)                                                               | 1.06x slower                                                                    |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_effbot   | 1.88 ms                                                             | 1.91 ms: 1.01x slower                                                           |
| regex_v8       | 15.7 ms                                                             | 16.1 ms: 1.02x slower                                                           |
| regex_dna      | 118 ms                                                              | 122 ms: 1.03x slower                                                            |
| regex_compile  | 99.9 ms                                                             | 110 ms: 1.10x slower                                                            |
| Geometric mean | (ref)                                                               | 1.04x slower                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| pickle_list          | 3.57 us                                                             | 3.19 us: 1.12x faster                                                           |
| json_loads           | 20.5 us                                                             | 19.8 us: 1.04x faster                                                           |
| pickle_dict          | 20.8 us                                                             | 20.2 us: 1.03x faster                                                           |
| unpickle_list        | 2.93 us                                                             | 2.87 us: 1.02x faster                                                           |
| pickle               | 8.07 us                                                             | 7.96 us: 1.01x faster                                                           |
| json_dumps           | 6.84 ms                                                             | 6.79 ms: 1.01x faster                                                           |
| unpickle             | 9.79 us                                                             | 10.1 us: 1.03x slower                                                           |
| xml_etree_iterparse  | 64.2 ms                                                             | 66.4 ms: 1.03x slower                                                           |
| xml_etree_process    | 42.1 ms                                                             | 43.7 ms: 1.04x slower                                                           |
| xml_etree_parse      | 104 ms                                                              | 109 ms: 1.04x slower                                                            |
| pickle_pure_python   | 213 us                                                              | 222 us: 1.04x slower                                                            |
| tomli_loads          | 1.65 sec                                                            | 1.73 sec: 1.05x slower                                                          |
| xml_etree_generate   | 59.6 ms                                                             | 62.6 ms: 1.05x slower                                                           |
| unpickle_pure_python | 147 us                                                              | 164 us: 1.11x slower                                                            |
| Geometric mean       | (ref)                                                               | 1.01x slower                                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|------------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup         | 22.2 ms                                                             | 24.4 ms: 1.10x slower                                                           |
| python_startup_no_site | 18.2 ms                                                             | 20.7 ms: 1.14x slower                                                           |
| Geometric mean         | (ref)                                                               | 1.12x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako            | 6.94 ms                                                             | 6.88 ms: 1.01x faster                                                           |
| genshi_xml      | 44.3 ms                                                             | 44.7 ms: 1.01x slower                                                           |
| genshi_text     | 20.1 ms                                                             | 20.4 ms: 1.01x slower                                                           |
| django_template | 30.1 ms                                                             | 33.3 ms: 1.11x slower                                                           |
| Geometric mean  | (ref)                                                               | 1.03x slower                                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 136 us                                                              | 95.5 us: 1.42x faster                                                           |
| pickle_list                | 3.57 us                                                             | 3.19 us: 1.12x faster                                                           |
| create_gc_cycles           | 756 us                                                              | 727 us: 1.04x faster                                                            |
| json_loads                 | 20.5 us                                                             | 19.8 us: 1.04x faster                                                           |
| pickle_dict                | 20.8 us                                                             | 20.2 us: 1.03x faster                                                           |
| unpickle_list              | 2.93 us                                                             | 2.87 us: 1.02x faster                                                           |
| sqlite_synth               | 1.96 us                                                             | 1.93 us: 1.01x faster                                                           |
| pickle                     | 8.07 us                                                             | 7.96 us: 1.01x faster                                                           |
| mako                       | 6.94 ms                                                             | 6.88 ms: 1.01x faster                                                           |
| html5lib                   | 45.4 ms                                                             | 45.0 ms: 1.01x faster                                                           |
| gc_traversal               | 1.43 ms                                                             | 1.42 ms: 1.01x faster                                                           |
| json_dumps                 | 6.84 ms                                                             | 6.79 ms: 1.01x faster                                                           |
| asyncio_tcp_ssl            | 16.9 sec                                                            | 16.8 sec: 1.01x faster                                                          |
| pidigits                   | 199 ms                                                              | 198 ms: 1.00x faster                                                            |
| sympy_expand               | 375 ms                                                              | 377 ms: 1.01x slower                                                            |
| tornado_http               | 94.3 ms                                                             | 95.0 ms: 1.01x slower                                                           |
| json                       | 4.10 ms                                                             | 4.13 ms: 1.01x slower                                                           |
| genshi_xml                 | 44.3 ms                                                             | 44.7 ms: 1.01x slower                                                           |
| coroutines                 | 15.5 ms                                                             | 15.6 ms: 1.01x slower                                                           |
| regex_effbot               | 1.88 ms                                                             | 1.91 ms: 1.01x slower                                                           |
| genshi_text                | 20.1 ms                                                             | 20.4 ms: 1.01x slower                                                           |
| async_tree_cpu_io_mixed_tg | 447 ms                                                              | 456 ms: 1.02x slower                                                            |
| regex_v8                   | 15.7 ms                                                             | 16.1 ms: 1.02x slower                                                           |
| async_tree_io_tg           | 529 ms                                                              | 542 ms: 1.02x slower                                                            |
| deepcopy_reduce            | 2.59 us                                                             | 2.65 us: 1.02x slower                                                           |
| async_tree_cpu_io_mixed    | 471 ms                                                              | 484 ms: 1.03x slower                                                            |
| unpickle                   | 9.79 us                                                             | 10.1 us: 1.03x slower                                                           |
| sqlglot_parse              | 964 us                                                              | 994 us: 1.03x slower                                                            |
| regex_dna                  | 118 ms                                                              | 122 ms: 1.03x slower                                                            |
| xml_etree_iterparse        | 64.2 ms                                                             | 66.4 ms: 1.03x slower                                                           |
| logging_silent             | 57.9 ns                                                             | 59.9 ns: 1.03x slower                                                           |
| sympy_str                  | 211 ms                                                              | 218 ms: 1.04x slower                                                            |
| xml_etree_process          | 42.1 ms                                                             | 43.7 ms: 1.04x slower                                                           |
| spectral_norm              | 68.0 ms                                                             | 70.6 ms: 1.04x slower                                                           |
| xml_etree_parse            | 104 ms                                                              | 109 ms: 1.04x slower                                                            |
| pickle_pure_python         | 213 us                                                              | 222 us: 1.04x slower                                                            |
| async_tree_memoization_tg  | 254 ms                                                              | 266 ms: 1.05x slower                                                            |
| tomli_loads                | 1.65 sec                                                            | 1.73 sec: 1.05x slower                                                          |
| async_tree_memoization     | 275 ms                                                              | 289 ms: 1.05x slower                                                            |
| sqlglot_transpile          | 1.19 ms                                                             | 1.25 ms: 1.05x slower                                                           |
| xml_etree_generate         | 59.6 ms                                                             | 62.6 ms: 1.05x slower                                                           |
| sympy_sum                  | 105 ms                                                              | 110 ms: 1.05x slower                                                            |
| async_tree_none            | 228 ms                                                              | 240 ms: 1.05x slower                                                            |
| telco                      | 6.03 ms                                                             | 6.36 ms: 1.05x slower                                                           |
| chameleon                  | 5.71 ms                                                             | 6.02 ms: 1.05x slower                                                           |
| deepcopy                   | 280 us                                                              | 295 us: 1.05x slower                                                            |
| docutils                   | 1.81 sec                                                            | 1.91 sec: 1.06x slower                                                          |
| richards_super             | 35.5 ms                                                             | 37.5 ms: 1.06x slower                                                           |
| richards                   | 31.2 ms                                                             | 33.0 ms: 1.06x slower                                                           |
| async_tree_none_tg         | 203 ms                                                              | 215 ms: 1.06x slower                                                            |
| deepcopy_memo              | 23.5 us                                                             | 24.9 us: 1.06x slower                                                           |
| logging_format             | 8.13 us                                                             | 8.66 us: 1.07x slower                                                           |
| generators                 | 21.2 ms                                                             | 22.5 ms: 1.07x slower                                                           |
| bench_mp_pool              | 69.4 ms                                                             | 74.2 ms: 1.07x slower                                                           |
| pylint                     | 217 ms                                                              | 233 ms: 1.07x slower                                                            |
| mdp                        | 1.60 sec                                                            | 1.72 sec: 1.07x slower                                                          |
| pycparser                  | 777 ms                                                              | 835 ms: 1.07x slower                                                            |
| logging_simple             | 7.47 us                                                             | 8.09 us: 1.08x slower                                                           |
| 2to3                       | 233 ms                                                              | 253 ms: 1.08x slower                                                            |
| async_generators           | 266 ms                                                              | 289 ms: 1.09x slower                                                            |
| meteor_contest             | 74.1 ms                                                             | 80.7 ms: 1.09x slower                                                           |
| thrift                     | 9.73 ms                                                             | 10.6 ms: 1.09x slower                                                           |
| python_startup             | 22.2 ms                                                             | 24.4 ms: 1.10x slower                                                           |
| regex_compile              | 99.9 ms                                                             | 110 ms: 1.10x slower                                                            |
| scimark_sparse_mat_mult    | 2.87 ms                                                             | 3.17 ms: 1.11x slower                                                           |
| django_template            | 30.1 ms                                                             | 33.3 ms: 1.11x slower                                                           |
| unpickle_pure_python       | 147 us                                                              | 164 us: 1.11x slower                                                            |
| sympy_integrate            | 14.6 ms                                                             | 16.3 ms: 1.11x slower                                                           |
| crypto_pyaes               | 55.8 ms                                                             | 63.2 ms: 1.13x slower                                                           |
| sqlglot_normalize          | 206 ms                                                              | 234 ms: 1.14x slower                                                            |
| python_startup_no_site     | 18.2 ms                                                             | 20.7 ms: 1.14x slower                                                           |
| sqlglot_optimize           | 39.7 ms                                                             | 45.7 ms: 1.15x slower                                                           |
| fannkuch                   | 270 ms                                                              | 317 ms: 1.18x slower                                                            |
| go                         | 101 ms                                                              | 119 ms: 1.18x slower                                                            |
| raytrace                   | 189 ms                                                              | 223 ms: 1.18x slower                                                            |
| pyflate                    | 308 ms                                                              | 366 ms: 1.19x slower                                                            |
| nbody                      | 76.9 ms                                                             | 92.0 ms: 1.20x slower                                                           |
| scimark_sor                | 81.0 ms                                                             | 97.3 ms: 1.20x slower                                                           |
| chaos                      | 48.0 ms                                                             | 58.0 ms: 1.21x slower                                                           |
| pprint_safe_repr           | 607 ms                                                              | 735 ms: 1.21x slower                                                            |
| pprint_pformat             | 1.24 sec                                                            | 1.50 sec: 1.21x slower                                                          |
| deltablue                  | 2.23 ms                                                             | 2.71 ms: 1.21x slower                                                           |
| scimark_fft                | 198 ms                                                              | 241 ms: 1.22x slower                                                            |
| comprehensions             | 11.9 us                                                             | 15.2 us: 1.28x slower                                                           |
| nqueens                    | 68.7 ms                                                             | 90.7 ms: 1.32x slower                                                           |
| scimark_monte_carlo        | 45.2 ms                                                             | 60.4 ms: 1.34x slower                                                           |
| hexiom                     | 4.23 ms                                                             | 5.86 ms: 1.39x slower                                                           |
| scimark_lu                 | 59.4 ms                                                             | 88.0 ms: 1.48x slower                                                           |
| coverage                   | 307 ms                                                              | 499 ms: 1.62x slower                                                            |
| Geometric mean             | (ref)                                                               | 1.07x slower                                                                    |

Benchmark hidden because not significant (5): asyncio_tcp, float, pathlib, async_tree_io, bench_thread_pool
Ignored benchmarks (1) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17.json: flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.05x
- 95% likely to have a slowdown of 1.04x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: unknown