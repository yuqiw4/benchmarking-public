# Results vs. 3.13.0b2

- fork: mdboom
- ref: tier2_func_simple_fr
- machine: windows-x86
- commit hash: c181b59
- commit date: 2024-04-10
- overall geometric mean: 1.08x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240410-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 233 ms                                                              | 255 ms: 1.09x slower                                                            |
| chameleon      | 5.71 ms                                                             | 6.27 ms: 1.10x slower                                                           |
| docutils       | 1.81 sec                                                            | 1.93 sec: 1.07x slower                                                          |
| tornado_http   | 94.3 ms                                                             | 95.5 ms: 1.01x slower                                                           |
| Geometric mean | (ref)                                                               | 1.05x slower                                                                    |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240410-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 447 ms                                                              | 461 ms: 1.03x slower                                                            |
| async_tree_io_tg           | 529 ms                                                              | 547 ms: 1.03x slower                                                            |
| async_tree_cpu_io_mixed    | 471 ms                                                              | 491 ms: 1.04x slower                                                            |
| async_tree_memoization     | 275 ms                                                              | 287 ms: 1.04x slower                                                            |
| async_tree_io              | 530 ms                                                              | 553 ms: 1.04x slower                                                            |
| async_tree_none            | 228 ms                                                              | 238 ms: 1.05x slower                                                            |
| async_tree_memoization_tg  | 254 ms                                                              | 267 ms: 1.05x slower                                                            |
| async_tree_none_tg         | 203 ms                                                              | 217 ms: 1.07x slower                                                            |
| Geometric mean             | (ref)                                                               | 1.04x slower                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240410-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| pidigits       | 199 ms                                                              | 197 ms: 1.01x faster                                                            |
| float          | 52.4 ms                                                             | 53.2 ms: 1.02x slower                                                           |
| nbody          | 76.9 ms                                                             | 96.9 ms: 1.26x slower                                                           |
| Geometric mean | (ref)                                                               | 1.08x slower                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240410-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_effbot   | 1.88 ms                                                             | 1.91 ms: 1.02x slower                                                           |
| regex_v8       | 15.7 ms                                                             | 16.1 ms: 1.03x slower                                                           |
| regex_dna      | 118 ms                                                              | 122 ms: 1.03x slower                                                            |
| regex_compile  | 99.9 ms                                                             | 110 ms: 1.11x slower                                                            |
| Geometric mean | (ref)                                                               | 1.04x slower                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240410-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| pickle_list          | 3.57 us                                                             | 3.17 us: 1.12x faster                                                           |
| pickle_dict          | 20.8 us                                                             | 19.8 us: 1.05x faster                                                           |
| unpickle_list        | 2.93 us                                                             | 2.82 us: 1.04x faster                                                           |
| json_loads           | 20.5 us                                                             | 20.1 us: 1.02x faster                                                           |
| pickle               | 8.07 us                                                             | 7.94 us: 1.02x faster                                                           |
| pickle_pure_python   | 213 us                                                              | 216 us: 1.02x slower                                                            |
| xml_etree_generate   | 59.6 ms                                                             | 60.7 ms: 1.02x slower                                                           |
| xml_etree_process    | 42.1 ms                                                             | 43.0 ms: 1.02x slower                                                           |
| xml_etree_iterparse  | 64.2 ms                                                             | 65.7 ms: 1.02x slower                                                           |
| xml_etree_parse      | 104 ms                                                              | 108 ms: 1.03x slower                                                            |
| tomli_loads          | 1.65 sec                                                            | 1.71 sec: 1.04x slower                                                          |
| unpickle             | 9.79 us                                                             | 10.2 us: 1.04x slower                                                           |
| unpickle_pure_python | 147 us                                                              | 174 us: 1.18x slower                                                            |
| Geometric mean       | (ref)                                                               | 1.01x slower                                                                    |

Benchmark hidden because not significant (1): json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240410-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|------------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup         | 22.2 ms                                                             | 23.9 ms: 1.08x slower                                                           |
| python_startup_no_site | 18.2 ms                                                             | 21.8 ms: 1.20x slower                                                           |
| Geometric mean         | (ref)                                                               | 1.14x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240410-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako           | 6.94 ms                                                             | 7.13 ms: 1.03x slower                                                           |
| genshi_text    | 20.1 ms                                                             | 20.7 ms: 1.03x slower                                                           |
| genshi_xml     | 44.3 ms                                                             | 46.6 ms: 1.05x slower                                                           |
| Geometric mean | (ref)                                                               | 1.04x slower                                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240410-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 136 us                                                              | 96.1 us: 1.41x faster                                                           |
| pickle_list                | 3.57 us                                                             | 3.17 us: 1.12x faster                                                           |
| asyncio_tcp                | 662 ms                                                              | 607 ms: 1.09x faster                                                            |
| pickle_dict                | 20.8 us                                                             | 19.8 us: 1.05x faster                                                           |
| unpickle_list              | 2.93 us                                                             | 2.82 us: 1.04x faster                                                           |
| coroutines                 | 15.5 ms                                                             | 15.1 ms: 1.03x faster                                                           |
| json_loads                 | 20.5 us                                                             | 20.1 us: 1.02x faster                                                           |
| pickle                     | 8.07 us                                                             | 7.94 us: 1.02x faster                                                           |
| create_gc_cycles           | 756 us                                                              | 749 us: 1.01x faster                                                            |
| sqlite_synth               | 1.96 us                                                             | 1.95 us: 1.01x faster                                                           |
| sympy_expand               | 375 ms                                                              | 373 ms: 1.01x faster                                                            |
| pidigits                   | 199 ms                                                              | 197 ms: 1.01x faster                                                            |
| pathlib                    | 83.9 ms                                                             | 84.6 ms: 1.01x slower                                                           |
| gc_traversal               | 1.43 ms                                                             | 1.45 ms: 1.01x slower                                                           |
| tornado_http               | 94.3 ms                                                             | 95.5 ms: 1.01x slower                                                           |
| float                      | 52.4 ms                                                             | 53.2 ms: 1.02x slower                                                           |
| pickle_pure_python         | 213 us                                                              | 216 us: 1.02x slower                                                            |
| regex_effbot               | 1.88 ms                                                             | 1.91 ms: 1.02x slower                                                           |
| xml_etree_generate         | 59.6 ms                                                             | 60.7 ms: 1.02x slower                                                           |
| xml_etree_process          | 42.1 ms                                                             | 43.0 ms: 1.02x slower                                                           |
| xml_etree_iterparse        | 64.2 ms                                                             | 65.7 ms: 1.02x slower                                                           |
| sqlglot_parse              | 964 us                                                              | 988 us: 1.02x slower                                                            |
| regex_v8                   | 15.7 ms                                                             | 16.1 ms: 1.03x slower                                                           |
| logging_silent             | 57.9 ns                                                             | 59.4 ns: 1.03x slower                                                           |
| mako                       | 6.94 ms                                                             | 7.13 ms: 1.03x slower                                                           |
| sympy_str                  | 211 ms                                                              | 217 ms: 1.03x slower                                                            |
| genshi_text                | 20.1 ms                                                             | 20.7 ms: 1.03x slower                                                           |
| async_tree_cpu_io_mixed_tg | 447 ms                                                              | 461 ms: 1.03x slower                                                            |
| xml_etree_parse            | 104 ms                                                              | 108 ms: 1.03x slower                                                            |
| async_tree_io_tg           | 529 ms                                                              | 547 ms: 1.03x slower                                                            |
| regex_dna                  | 118 ms                                                              | 122 ms: 1.03x slower                                                            |
| bench_mp_pool              | 69.4 ms                                                             | 71.8 ms: 1.03x slower                                                           |
| tomli_loads                | 1.65 sec                                                            | 1.71 sec: 1.04x slower                                                          |
| unpickle                   | 9.79 us                                                             | 10.2 us: 1.04x slower                                                           |
| deepcopy_reduce            | 2.59 us                                                             | 2.69 us: 1.04x slower                                                           |
| async_tree_cpu_io_mixed    | 471 ms                                                              | 491 ms: 1.04x slower                                                            |
| sqlglot_transpile          | 1.19 ms                                                             | 1.24 ms: 1.04x slower                                                           |
| async_tree_memoization     | 275 ms                                                              | 287 ms: 1.04x slower                                                            |
| async_tree_io              | 530 ms                                                              | 553 ms: 1.04x slower                                                            |
| spectral_norm              | 68.0 ms                                                             | 71.0 ms: 1.04x slower                                                           |
| async_tree_none            | 228 ms                                                              | 238 ms: 1.05x slower                                                            |
| sympy_sum                  | 105 ms                                                              | 110 ms: 1.05x slower                                                            |
| logging_format             | 8.13 us                                                             | 8.53 us: 1.05x slower                                                           |
| async_tree_memoization_tg  | 254 ms                                                              | 267 ms: 1.05x slower                                                            |
| deepcopy                   | 280 us                                                              | 294 us: 1.05x slower                                                            |
| genshi_xml                 | 44.3 ms                                                             | 46.6 ms: 1.05x slower                                                           |
| generators                 | 21.2 ms                                                             | 22.3 ms: 1.05x slower                                                           |
| logging_simple             | 7.47 us                                                             | 7.93 us: 1.06x slower                                                           |
| docutils                   | 1.81 sec                                                            | 1.93 sec: 1.07x slower                                                          |
| async_tree_none_tg         | 203 ms                                                              | 217 ms: 1.07x slower                                                            |
| async_generators           | 266 ms                                                              | 286 ms: 1.08x slower                                                            |
| python_startup             | 22.2 ms                                                             | 23.9 ms: 1.08x slower                                                           |
| deepcopy_memo              | 23.5 us                                                             | 25.3 us: 1.08x slower                                                           |
| mdp                        | 1.60 sec                                                            | 1.73 sec: 1.08x slower                                                          |
| pycparser                  | 777 ms                                                              | 841 ms: 1.08x slower                                                            |
| thrift                     | 9.73 ms                                                             | 10.5 ms: 1.08x slower                                                           |
| 2to3                       | 233 ms                                                              | 255 ms: 1.09x slower                                                            |
| chameleon                  | 5.71 ms                                                             | 6.27 ms: 1.10x slower                                                           |
| regex_compile              | 99.9 ms                                                             | 110 ms: 1.11x slower                                                            |
| meteor_contest             | 74.1 ms                                                             | 82.0 ms: 1.11x slower                                                           |
| richards_super             | 35.5 ms                                                             | 39.5 ms: 1.11x slower                                                           |
| richards                   | 31.2 ms                                                             | 34.8 ms: 1.11x slower                                                           |
| sympy_integrate            | 14.6 ms                                                             | 16.4 ms: 1.12x slower                                                           |
| sqlglot_normalize          | 206 ms                                                              | 232 ms: 1.12x slower                                                            |
| scimark_sparse_mat_mult    | 2.87 ms                                                             | 3.23 ms: 1.13x slower                                                           |
| telco                      | 6.03 ms                                                             | 6.84 ms: 1.13x slower                                                           |
| crypto_pyaes               | 55.8 ms                                                             | 63.5 ms: 1.14x slower                                                           |
| sqlglot_optimize           | 39.7 ms                                                             | 45.4 ms: 1.14x slower                                                           |
| raytrace                   | 189 ms                                                              | 220 ms: 1.16x slower                                                            |
| pyflate                    | 308 ms                                                              | 361 ms: 1.17x slower                                                            |
| unpickle_pure_python       | 147 us                                                              | 174 us: 1.18x slower                                                            |
| python_startup_no_site     | 18.2 ms                                                             | 21.8 ms: 1.20x slower                                                           |
| scimark_sor                | 81.0 ms                                                             | 97.4 ms: 1.20x slower                                                           |
| deltablue                  | 2.23 ms                                                             | 2.72 ms: 1.22x slower                                                           |
| fannkuch                   | 270 ms                                                              | 329 ms: 1.22x slower                                                            |
| go                         | 101 ms                                                              | 123 ms: 1.22x slower                                                            |
| pprint_safe_repr           | 607 ms                                                              | 749 ms: 1.23x slower                                                            |
| pprint_pformat             | 1.24 sec                                                            | 1.53 sec: 1.24x slower                                                          |
| scimark_fft                | 198 ms                                                              | 245 ms: 1.24x slower                                                            |
| nbody                      | 76.9 ms                                                             | 96.9 ms: 1.26x slower                                                           |
| chaos                      | 48.0 ms                                                             | 61.9 ms: 1.29x slower                                                           |
| scimark_monte_carlo        | 45.2 ms                                                             | 59.4 ms: 1.31x slower                                                           |
| comprehensions             | 11.9 us                                                             | 15.6 us: 1.32x slower                                                           |
| nqueens                    | 68.7 ms                                                             | 92.9 ms: 1.35x slower                                                           |
| hexiom                     | 4.23 ms                                                             | 6.12 ms: 1.45x slower                                                           |
| scimark_lu                 | 59.4 ms                                                             | 87.5 ms: 1.47x slower                                                           |
| coverage                   | 307 ms                                                              | 499 ms: 1.62x slower                                                            |
| Geometric mean             | (ref)                                                               | 1.08x slower                                                                    |

Benchmark hidden because not significant (6): bench_thread_pool, html5lib, json_dumps, asyncio_tcp_ssl, json, pylint
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17.json: django_template, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.05x
- 95% likely to have a slowdown of 1.04x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: unknown