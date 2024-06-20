# Results vs. 3.13.0b2

- fork: mdboom
- ref: tier2_func_simple
- machine: linux-x86_64
- commit hash: 81bda60
- commit date: 2024-04-05
- overall geometric mean: 1.01x slower
- HPT reliability: 99.97%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.06x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240405-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:----------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 291 ms                                                           | 297 ms: 1.02x slower                                                      |
| chameleon      | 7.40 ms                                                          | 7.43 ms: 1.00x slower                                                     |
| docutils       | 2.98 sec                                                         | 3.08 sec: 1.03x slower                                                    |
| html5lib       | 74.7 ms                                                          | 73.0 ms: 1.02x faster                                                     |
| tornado_http   | 119 ms                                                           | 121 ms: 1.02x slower                                                      |
| Geometric mean | (ref)                                                            | 1.01x slower                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240405-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------------------|:----------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_io_tg           | 900 ms                                                           | 869 ms: 1.04x faster                                                      |
| async_tree_io              | 873 ms                                                           | 856 ms: 1.02x faster                                                      |
| async_tree_none            | 365 ms                                                           | 378 ms: 1.03x slower                                                      |
| async_tree_cpu_io_mixed_tg | 573 ms                                                           | 593 ms: 1.03x slower                                                      |
| Geometric mean             | (ref)                                                            | 1.00x faster                                                              |

Benchmark hidden because not significant (4): async_tree_memoization, async_tree_none_tg, async_tree_memoization_tg, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240405-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:----------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| float          | 80.2 ms                                                          | 75.2 ms: 1.07x faster                                                     |
| pidigits       | 254 ms                                                           | 262 ms: 1.03x slower                                                      |
| nbody          | 87.8 ms                                                          | 103 ms: 1.18x slower                                                      |
| Geometric mean | (ref)                                                            | 1.04x slower                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240405-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:----------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_dna      | 249 ms                                                           | 241 ms: 1.04x faster                                                      |
| regex_compile  | 144 ms                                                           | 148 ms: 1.02x slower                                                      |
| regex_effbot   | 3.40 ms                                                          | 3.54 ms: 1.04x slower                                                     |
| Geometric mean | (ref)                                                            | 1.01x slower                                                              |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240405-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------------|:----------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| tomli_loads          | 2.40 sec                                                         | 2.15 sec: 1.12x faster                                                    |
| pickle_dict          | 32.8 us                                                          | 30.8 us: 1.07x faster                                                     |
| unpickle             | 15.7 us                                                          | 14.8 us: 1.06x faster                                                     |
| xml_etree_process    | 59.7 ms                                                          | 58.0 ms: 1.03x faster                                                     |
| pickle               | 10.6 us                                                          | 10.3 us: 1.03x faster                                                     |
| xml_etree_iterparse  | 103 ms                                                           | 99.8 ms: 1.03x faster                                                     |
| xml_etree_generate   | 85.7 ms                                                          | 83.5 ms: 1.03x faster                                                     |
| pickle_list          | 4.44 us                                                          | 4.38 us: 1.01x faster                                                     |
| unpickle_list        | 4.70 us                                                          | 4.63 us: 1.01x faster                                                     |
| json_dumps           | 10.8 ms                                                          | 10.6 ms: 1.01x faster                                                     |
| xml_etree_parse      | 144 ms                                                           | 142 ms: 1.01x faster                                                      |
| json_loads           | 25.0 us                                                          | 25.4 us: 1.01x slower                                                     |
| pickle_pure_python   | 307 us                                                           | 313 us: 1.02x slower                                                      |
| unpickle_pure_python | 224 us                                                           | 230 us: 1.02x slower                                                      |
| Geometric mean       | (ref)                                                            | 1.03x faster                                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240405-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|------------------------|:----------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup         | 13.2 ms                                                          | 13.4 ms: 1.02x slower                                                     |
| python_startup_no_site | 8.85 ms                                                          | 11.8 ms: 1.33x slower                                                     |
| Geometric mean         | (ref)                                                            | 1.16x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240405-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:----------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| genshi_xml     | 58.1 ms                                                          | 56.4 ms: 1.03x faster                                                     |
| mako           | 10.4 ms                                                          | 10.1 ms: 1.02x faster                                                     |
| Geometric mean | (ref)                                                            | 1.02x faster                                                              |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240405-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------------------|:----------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| typing_runtime_protocols   | 171 us                                                           | 118 us: 1.44x faster                                                      |
| richards_super             | 61.2 ms                                                          | 52.3 ms: 1.17x faster                                                     |
| richards                   | 53.4 ms                                                          | 45.7 ms: 1.17x faster                                                     |
| tomli_loads                | 2.40 sec                                                         | 2.15 sec: 1.12x faster                                                    |
| create_gc_cycles           | 2.00 ms                                                          | 1.87 ms: 1.07x faster                                                     |
| float                      | 80.2 ms                                                          | 75.2 ms: 1.07x faster                                                     |
| pickle_dict                | 32.8 us                                                          | 30.8 us: 1.07x faster                                                     |
| unpickle                   | 15.7 us                                                          | 14.8 us: 1.06x faster                                                     |
| gc_traversal               | 4.69 ms                                                          | 4.44 ms: 1.06x faster                                                     |
| sqlite_synth               | 2.80 us                                                          | 2.68 us: 1.04x faster                                                     |
| spectral_norm              | 97.3 ms                                                          | 93.4 ms: 1.04x faster                                                     |
| regex_dna                  | 249 ms                                                           | 241 ms: 1.04x faster                                                      |
| async_tree_io_tg           | 900 ms                                                           | 869 ms: 1.04x faster                                                      |
| coverage                   | 83.5 ms                                                          | 80.7 ms: 1.03x faster                                                     |
| xml_etree_process          | 59.7 ms                                                          | 58.0 ms: 1.03x faster                                                     |
| genshi_xml                 | 58.1 ms                                                          | 56.4 ms: 1.03x faster                                                     |
| pickle                     | 10.6 us                                                          | 10.3 us: 1.03x faster                                                     |
| xml_etree_iterparse        | 103 ms                                                           | 99.8 ms: 1.03x faster                                                     |
| xml_etree_generate         | 85.7 ms                                                          | 83.5 ms: 1.03x faster                                                     |
| mako                       | 10.4 ms                                                          | 10.1 ms: 1.02x faster                                                     |
| html5lib                   | 74.7 ms                                                          | 73.0 ms: 1.02x faster                                                     |
| async_tree_io              | 873 ms                                                           | 856 ms: 1.02x faster                                                      |
| asyncio_tcp                | 378 ms                                                           | 372 ms: 1.01x faster                                                      |
| pickle_list                | 4.44 us                                                          | 4.38 us: 1.01x faster                                                     |
| unpickle_list              | 4.70 us                                                          | 4.63 us: 1.01x faster                                                     |
| json_dumps                 | 10.8 ms                                                          | 10.6 ms: 1.01x faster                                                     |
| logging_format             | 7.11 us                                                          | 7.02 us: 1.01x faster                                                     |
| xml_etree_parse            | 144 ms                                                           | 142 ms: 1.01x faster                                                      |
| scimark_sparse_mat_mult    | 4.28 ms                                                          | 4.24 ms: 1.01x faster                                                     |
| logging_simple             | 6.40 us                                                          | 6.36 us: 1.01x faster                                                     |
| generators                 | 33.5 ms                                                          | 33.4 ms: 1.00x faster                                                     |
| chameleon                  | 7.40 ms                                                          | 7.43 ms: 1.00x slower                                                     |
| deepcopy                   | 377 us                                                           | 379 us: 1.01x slower                                                      |
| dulwich_log                | 67.3 ms                                                          | 67.7 ms: 1.01x slower                                                     |
| sqlglot_parse              | 1.39 ms                                                          | 1.40 ms: 1.01x slower                                                     |
| logging_silent             | 96.3 ns                                                          | 97.2 ns: 1.01x slower                                                     |
| deepcopy_reduce            | 3.39 us                                                          | 3.43 us: 1.01x slower                                                     |
| coroutines                 | 22.0 ms                                                          | 22.3 ms: 1.01x slower                                                     |
| json_loads                 | 25.0 us                                                          | 25.4 us: 1.01x slower                                                     |
| pycparser                  | 1.22 sec                                                         | 1.24 sec: 1.02x slower                                                    |
| tornado_http               | 119 ms                                                           | 121 ms: 1.02x slower                                                      |
| pickle_pure_python         | 307 us                                                           | 313 us: 1.02x slower                                                      |
| python_startup             | 13.2 ms                                                          | 13.4 ms: 1.02x slower                                                     |
| pprint_safe_repr           | 818 ms                                                           | 833 ms: 1.02x slower                                                      |
| 2to3                       | 291 ms                                                           | 297 ms: 1.02x slower                                                      |
| sqlglot_transpile          | 1.76 ms                                                          | 1.80 ms: 1.02x slower                                                     |
| sqlglot_normalize          | 120 ms                                                           | 123 ms: 1.02x slower                                                      |
| json                       | 5.35 ms                                                          | 5.48 ms: 1.02x slower                                                     |
| unpickle_pure_python       | 224 us                                                           | 230 us: 1.02x slower                                                      |
| regex_compile              | 144 ms                                                           | 148 ms: 1.02x slower                                                      |
| pprint_pformat             | 1.66 sec                                                         | 1.70 sec: 1.03x slower                                                    |
| sympy_expand               | 501 ms                                                           | 516 ms: 1.03x slower                                                      |
| dask                       | 391 ms                                                           | 403 ms: 1.03x slower                                                      |
| pidigits                   | 254 ms                                                           | 262 ms: 1.03x slower                                                      |
| docutils                   | 2.98 sec                                                         | 3.08 sec: 1.03x slower                                                    |
| async_tree_none            | 365 ms                                                           | 378 ms: 1.03x slower                                                      |
| async_tree_cpu_io_mixed_tg | 573 ms                                                           | 593 ms: 1.03x slower                                                      |
| meteor_contest             | 128 ms                                                           | 133 ms: 1.03x slower                                                      |
| raytrace                   | 260 ms                                                           | 270 ms: 1.04x slower                                                      |
| regex_effbot               | 3.40 ms                                                          | 3.54 ms: 1.04x slower                                                     |
| gunicorn                   | 1.04 ms                                                          | 1.09 ms: 1.04x slower                                                     |
| pyflate                    | 482 ms                                                           | 504 ms: 1.05x slower                                                      |
| bench_thread_pool          | 908 us                                                           | 951 us: 1.05x slower                                                      |
| crypto_pyaes               | 73.6 ms                                                          | 77.3 ms: 1.05x slower                                                     |
| sympy_str                  | 295 ms                                                           | 310 ms: 1.05x slower                                                      |
| async_generators           | 363 ms                                                           | 383 ms: 1.05x slower                                                      |
| sqlglot_optimize           | 59.5 ms                                                          | 62.9 ms: 1.06x slower                                                     |
| aiohttp                    | 1.07 ms                                                          | 1.13 ms: 1.06x slower                                                     |
| scimark_monte_carlo        | 65.5 ms                                                          | 69.4 ms: 1.06x slower                                                     |
| sympy_sum                  | 155 ms                                                           | 165 ms: 1.07x slower                                                      |
| mdp                        | 2.46 sec                                                         | 2.63 sec: 1.07x slower                                                    |
| mypy2                      | 764 ms                                                           | 820 ms: 1.07x slower                                                      |
| go                         | 165 ms                                                           | 177 ms: 1.07x slower                                                      |
| chaos                      | 59.6 ms                                                          | 64.7 ms: 1.08x slower                                                     |
| sympy_integrate            | 23.2 ms                                                          | 25.4 ms: 1.09x slower                                                     |
| deltablue                  | 3.37 ms                                                          | 3.75 ms: 1.11x slower                                                     |
| fannkuch                   | 353 ms                                                           | 393 ms: 1.12x slower                                                      |
| hexiom                     | 6.35 ms                                                          | 7.13 ms: 1.12x slower                                                     |
| pathlib                    | 17.1 ms                                                          | 19.4 ms: 1.13x slower                                                     |
| comprehensions             | 17.0 us                                                          | 19.3 us: 1.14x slower                                                     |
| nqueens                    | 88.4 ms                                                          | 100 ms: 1.14x slower                                                      |
| nbody                      | 87.8 ms                                                          | 103 ms: 1.18x slower                                                      |
| scimark_lu                 | 97.5 ms                                                          | 118 ms: 1.21x slower                                                      |
| scimark_sor                | 119 ms                                                           | 152 ms: 1.28x slower                                                      |
| python_startup_no_site     | 8.85 ms                                                          | 11.8 ms: 1.33x slower                                                     |
| Geometric mean             | (ref)                                                            | 1.01x slower                                                              |

Benchmark hidden because not significant (14): bench_mp_pool, async_tree_memoization, async_tree_none_tg, pylint, telco, asyncio_websockets, deepcopy_memo, thrift, asyncio_tcp_ssl, genshi_text, async_tree_memoization_tg, async_tree_cpu_io_mixed, regex_v8, scimark_fft
Ignored benchmarks (3) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, django_template, flaskblogging

# HPT report

- Reliability score: 99.97% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.06x