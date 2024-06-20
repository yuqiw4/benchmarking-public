# Results vs. 3.13.0b2

- fork: savannahostrowski
- ref: llvm_18
- machine: windows-x86
- commit hash: fe17f68
- commit date: 2024-04-26
- overall geometric mean: 1.10x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-pythonperf1_win32-x86-savannahostrowski-llvm_18-3.13.0a6+-fe17f68 |
|----------------|:-------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 233 ms                                                              | 270 ms: 1.16x slower                                                          |
| chameleon      | 5.71 ms                                                             | 6.48 ms: 1.13x slower                                                         |
| docutils       | 1.81 sec                                                            | 1.99 sec: 1.10x slower                                                        |
| html5lib       | 45.4 ms                                                             | 46.1 ms: 1.01x slower                                                         |
| tornado_http   | 94.3 ms                                                             | 107 ms: 1.13x slower                                                          |
| Geometric mean | (ref)                                                               | 1.11x slower                                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-pythonperf1_win32-x86-savannahostrowski-llvm_18-3.13.0a6+-fe17f68 |
|----------------------------|:-------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 447 ms                                                              | 469 ms: 1.05x slower                                                          |
| async_tree_io_tg           | 529 ms                                                              | 561 ms: 1.06x slower                                                          |
| async_tree_io              | 530 ms                                                              | 562 ms: 1.06x slower                                                          |
| async_tree_cpu_io_mixed    | 471 ms                                                              | 502 ms: 1.07x slower                                                          |
| async_tree_memoization_tg  | 254 ms                                                              | 276 ms: 1.09x slower                                                          |
| async_tree_none            | 228 ms                                                              | 248 ms: 1.09x slower                                                          |
| async_tree_memoization     | 275 ms                                                              | 301 ms: 1.09x slower                                                          |
| async_tree_none_tg         | 203 ms                                                              | 224 ms: 1.10x slower                                                          |
| Geometric mean             | (ref)                                                               | 1.08x slower                                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-pythonperf1_win32-x86-savannahostrowski-llvm_18-3.13.0a6+-fe17f68 |
|----------------|:-------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| float          | 52.4 ms                                                             | 53.7 ms: 1.02x slower                                                         |
| nbody          | 76.9 ms                                                             | 96.2 ms: 1.25x slower                                                         |
| Geometric mean | (ref)                                                               | 1.09x slower                                                                  |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-pythonperf1_win32-x86-savannahostrowski-llvm_18-3.13.0a6+-fe17f68 |
|----------------|:-------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_v8       | 15.7 ms                                                             | 16.1 ms: 1.03x slower                                                         |
| regex_effbot   | 1.88 ms                                                             | 2.00 ms: 1.06x slower                                                         |
| regex_dna      | 118 ms                                                              | 128 ms: 1.09x slower                                                          |
| regex_compile  | 99.9 ms                                                             | 109 ms: 1.09x slower                                                          |
| Geometric mean | (ref)                                                               | 1.07x slower                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-pythonperf1_win32-x86-savannahostrowski-llvm_18-3.13.0a6+-fe17f68 |
|----------------------|:-------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| pickle_list          | 3.57 us                                                             | 3.28 us: 1.09x faster                                                         |
| unpickle_list        | 2.93 us                                                             | 2.80 us: 1.05x faster                                                         |
| pickle_dict          | 20.8 us                                                             | 20.3 us: 1.02x faster                                                         |
| json_dumps           | 6.84 ms                                                             | 6.90 ms: 1.01x slower                                                         |
| xml_etree_iterparse  | 64.2 ms                                                             | 65.7 ms: 1.02x slower                                                         |
| unpickle             | 9.79 us                                                             | 10.2 us: 1.04x slower                                                         |
| pickle_pure_python   | 213 us                                                              | 224 us: 1.05x slower                                                          |
| xml_etree_generate   | 59.6 ms                                                             | 62.9 ms: 1.06x slower                                                         |
| tomli_loads          | 1.65 sec                                                            | 1.75 sec: 1.06x slower                                                        |
| xml_etree_process    | 42.1 ms                                                             | 45.4 ms: 1.08x slower                                                         |
| unpickle_pure_python | 147 us                                                              | 165 us: 1.12x slower                                                          |
| Geometric mean       | (ref)                                                               | 1.02x slower                                                                  |

Benchmark hidden because not significant (3): xml_etree_parse, json_loads, pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-pythonperf1_win32-x86-savannahostrowski-llvm_18-3.13.0a6+-fe17f68 |
|------------------------|:-------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup         | 22.2 ms                                                             | 24.6 ms: 1.11x slower                                                         |
| python_startup_no_site | 18.2 ms                                                             | 20.6 ms: 1.13x slower                                                         |
| Geometric mean         | (ref)                                                               | 1.12x slower                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-pythonperf1_win32-x86-savannahostrowski-llvm_18-3.13.0a6+-fe17f68 |
|-----------------|:-------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| mako            | 6.94 ms                                                             | 7.09 ms: 1.02x slower                                                         |
| django_template | 30.1 ms                                                             | 33.8 ms: 1.13x slower                                                         |
| genshi_xml      | 44.3 ms                                                             | 52.1 ms: 1.18x slower                                                         |
| genshi_text     | 20.1 ms                                                             | 24.3 ms: 1.21x slower                                                         |
| Geometric mean  | (ref)                                                               | 1.13x slower                                                                  |

All benchmarks:
===============

| Benchmark                  | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-pythonperf1_win32-x86-savannahostrowski-llvm_18-3.13.0a6+-fe17f68 |
|----------------------------|:-------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| sqlglot_normalize          | 206 ms                                                              | 101 ms: 2.03x faster                                                          |
| pickle_list                | 3.57 us                                                             | 3.28 us: 1.09x faster                                                         |
| unpickle_list              | 2.93 us                                                             | 2.80 us: 1.05x faster                                                         |
| create_gc_cycles           | 756 us                                                              | 737 us: 1.03x faster                                                          |
| pickle_dict                | 20.8 us                                                             | 20.3 us: 1.02x faster                                                         |
| json_dumps                 | 6.84 ms                                                             | 6.90 ms: 1.01x slower                                                         |
| sqlite_synth               | 1.96 us                                                             | 1.98 us: 1.01x slower                                                         |
| html5lib                   | 45.4 ms                                                             | 46.1 ms: 1.01x slower                                                         |
| asyncio_tcp_ssl            | 16.9 sec                                                            | 17.1 sec: 1.01x slower                                                        |
| deepcopy_reduce            | 2.59 us                                                             | 2.64 us: 1.02x slower                                                         |
| mako                       | 6.94 ms                                                             | 7.09 ms: 1.02x slower                                                         |
| xml_etree_iterparse        | 64.2 ms                                                             | 65.7 ms: 1.02x slower                                                         |
| gc_traversal               | 1.43 ms                                                             | 1.47 ms: 1.02x slower                                                         |
| float                      | 52.4 ms                                                             | 53.7 ms: 1.02x slower                                                         |
| regex_v8                   | 15.7 ms                                                             | 16.1 ms: 1.03x slower                                                         |
| sympy_expand               | 375 ms                                                              | 385 ms: 1.03x slower                                                          |
| json                       | 4.10 ms                                                             | 4.22 ms: 1.03x slower                                                         |
| bench_thread_pool          | 985 us                                                              | 1.02 ms: 1.04x slower                                                         |
| unpickle                   | 9.79 us                                                             | 10.2 us: 1.04x slower                                                         |
| async_tree_cpu_io_mixed_tg | 447 ms                                                              | 469 ms: 1.05x slower                                                          |
| logging_silent             | 57.9 ns                                                             | 60.8 ns: 1.05x slower                                                         |
| pickle_pure_python         | 213 us                                                              | 224 us: 1.05x slower                                                          |
| sympy_str                  | 211 ms                                                              | 223 ms: 1.06x slower                                                          |
| xml_etree_generate         | 59.6 ms                                                             | 62.9 ms: 1.06x slower                                                         |
| coroutines                 | 15.5 ms                                                             | 16.4 ms: 1.06x slower                                                         |
| pathlib                    | 83.9 ms                                                             | 88.8 ms: 1.06x slower                                                         |
| async_tree_io_tg           | 529 ms                                                              | 561 ms: 1.06x slower                                                          |
| async_tree_io              | 530 ms                                                              | 562 ms: 1.06x slower                                                          |
| regex_effbot               | 1.88 ms                                                             | 2.00 ms: 1.06x slower                                                         |
| telco                      | 6.03 ms                                                             | 6.41 ms: 1.06x slower                                                         |
| tomli_loads                | 1.65 sec                                                            | 1.75 sec: 1.06x slower                                                        |
| async_tree_cpu_io_mixed    | 471 ms                                                              | 502 ms: 1.07x slower                                                          |
| bench_mp_pool              | 69.4 ms                                                             | 74.1 ms: 1.07x slower                                                         |
| deepcopy_memo              | 23.5 us                                                             | 25.1 us: 1.07x slower                                                         |
| sqlglot_parse              | 964 us                                                              | 1.03 ms: 1.07x slower                                                         |
| logging_format             | 8.13 us                                                             | 8.72 us: 1.07x slower                                                         |
| sympy_sum                  | 105 ms                                                              | 113 ms: 1.08x slower                                                          |
| xml_etree_process          | 42.1 ms                                                             | 45.4 ms: 1.08x slower                                                         |
| logging_simple             | 7.47 us                                                             | 8.11 us: 1.09x slower                                                         |
| generators                 | 21.2 ms                                                             | 23.0 ms: 1.09x slower                                                         |
| async_tree_memoization_tg  | 254 ms                                                              | 276 ms: 1.09x slower                                                          |
| regex_dna                  | 118 ms                                                              | 128 ms: 1.09x slower                                                          |
| sqlglot_transpile          | 1.19 ms                                                             | 1.30 ms: 1.09x slower                                                         |
| richards                   | 31.2 ms                                                             | 34.0 ms: 1.09x slower                                                         |
| async_tree_none            | 228 ms                                                              | 248 ms: 1.09x slower                                                          |
| deepcopy                   | 280 us                                                              | 305 us: 1.09x slower                                                          |
| regex_compile              | 99.9 ms                                                             | 109 ms: 1.09x slower                                                          |
| async_tree_memoization     | 275 ms                                                              | 301 ms: 1.09x slower                                                          |
| pycparser                  | 777 ms                                                              | 851 ms: 1.09x slower                                                          |
| richards_super             | 35.5 ms                                                             | 38.9 ms: 1.10x slower                                                         |
| docutils                   | 1.81 sec                                                            | 1.99 sec: 1.10x slower                                                        |
| async_tree_none_tg         | 203 ms                                                              | 224 ms: 1.10x slower                                                          |
| scimark_sparse_mat_mult    | 2.87 ms                                                             | 3.17 ms: 1.10x slower                                                         |
| python_startup             | 22.2 ms                                                             | 24.6 ms: 1.11x slower                                                         |
| thrift                     | 9.73 ms                                                             | 10.8 ms: 1.11x slower                                                         |
| crypto_pyaes               | 55.8 ms                                                             | 62.2 ms: 1.11x slower                                                         |
| unpickle_pure_python       | 147 us                                                              | 165 us: 1.12x slower                                                          |
| pylint                     | 217 ms                                                              | 243 ms: 1.12x slower                                                          |
| django_template            | 30.1 ms                                                             | 33.8 ms: 1.13x slower                                                         |
| python_startup_no_site     | 18.2 ms                                                             | 20.6 ms: 1.13x slower                                                         |
| chameleon                  | 5.71 ms                                                             | 6.48 ms: 1.13x slower                                                         |
| tornado_http               | 94.3 ms                                                             | 107 ms: 1.13x slower                                                          |
| typing_runtime_protocols   | 136 us                                                              | 154 us: 1.14x slower                                                          |
| async_generators           | 266 ms                                                              | 302 ms: 1.14x slower                                                          |
| mdp                        | 1.60 sec                                                            | 1.83 sec: 1.14x slower                                                        |
| sympy_integrate            | 14.6 ms                                                             | 16.7 ms: 1.14x slower                                                         |
| asyncio_tcp                | 662 ms                                                              | 764 ms: 1.15x slower                                                          |
| 2to3                       | 233 ms                                                              | 270 ms: 1.16x slower                                                          |
| meteor_contest             | 74.1 ms                                                             | 86.0 ms: 1.16x slower                                                         |
| fannkuch                   | 270 ms                                                              | 314 ms: 1.16x slower                                                          |
| pyflate                    | 308 ms                                                              | 362 ms: 1.17x slower                                                          |
| genshi_xml                 | 44.3 ms                                                             | 52.1 ms: 1.18x slower                                                         |
| raytrace                   | 189 ms                                                              | 223 ms: 1.18x slower                                                          |
| scimark_fft                | 198 ms                                                              | 235 ms: 1.18x slower                                                          |
| pprint_safe_repr           | 607 ms                                                              | 727 ms: 1.20x slower                                                          |
| pprint_pformat             | 1.24 sec                                                            | 1.49 sec: 1.20x slower                                                        |
| genshi_text                | 20.1 ms                                                             | 24.3 ms: 1.21x slower                                                         |
| sqlglot_optimize           | 39.7 ms                                                             | 48.2 ms: 1.21x slower                                                         |
| scimark_sor                | 81.0 ms                                                             | 99.3 ms: 1.23x slower                                                         |
| go                         | 101 ms                                                              | 124 ms: 1.24x slower                                                          |
| deltablue                  | 2.23 ms                                                             | 2.79 ms: 1.25x slower                                                         |
| nbody                      | 76.9 ms                                                             | 96.2 ms: 1.25x slower                                                         |
| chaos                      | 48.0 ms                                                             | 60.9 ms: 1.27x slower                                                         |
| scimark_monte_carlo        | 45.2 ms                                                             | 59.3 ms: 1.31x slower                                                         |
| nqueens                    | 68.7 ms                                                             | 93.2 ms: 1.36x slower                                                         |
| comprehensions             | 11.9 us                                                             | 16.1 us: 1.36x slower                                                         |
| coverage                   | 307 ms                                                              | 420 ms: 1.37x slower                                                          |
| hexiom                     | 4.23 ms                                                             | 6.30 ms: 1.49x slower                                                         |
| scimark_lu                 | 59.4 ms                                                             | 90.3 ms: 1.52x slower                                                         |
| Geometric mean             | (ref)                                                               | 1.10x slower                                                                  |

Benchmark hidden because not significant (5): xml_etree_parse, spectral_norm, json_loads, pidigits, pickle
Ignored benchmarks (1) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17.json: flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.08x
- 95% likely to have a slowdown of 1.08x
- 99% likely to have a slowdown of 1.07x

# Memory
- memory change: unknown