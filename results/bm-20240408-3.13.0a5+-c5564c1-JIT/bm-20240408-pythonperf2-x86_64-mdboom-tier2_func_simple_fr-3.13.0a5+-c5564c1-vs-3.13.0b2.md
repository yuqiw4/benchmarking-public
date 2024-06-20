# Results vs. 3.13.0b2

- fork: mdboom
- ref: tier2_func_simple_fr
- machine: linux-x86_64
- commit hash: c5564c1
- commit date: 2024-04-08
- overall geometric mean: 1.02x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.05x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 291 ms                                                           | 298 ms: 1.02x slower                                                         |
| chameleon      | 7.40 ms                                                          | 7.70 ms: 1.04x slower                                                        |
| docutils       | 2.98 sec                                                         | 3.09 sec: 1.04x slower                                                       |
| html5lib       | 74.7 ms                                                          | 73.7 ms: 1.01x faster                                                        |
| tornado_http   | 119 ms                                                           | 122 ms: 1.02x slower                                                         |
| Geometric mean | (ref)                                                            | 1.02x slower                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_io_tg           | 900 ms                                                           | 855 ms: 1.05x faster                                                         |
| async_tree_memoization     | 460 ms                                                           | 441 ms: 1.04x faster                                                         |
| async_tree_io              | 873 ms                                                           | 847 ms: 1.03x faster                                                         |
| async_tree_none_tg         | 340 ms                                                           | 333 ms: 1.02x faster                                                         |
| async_tree_none            | 365 ms                                                           | 375 ms: 1.03x slower                                                         |
| async_tree_cpu_io_mixed_tg | 573 ms                                                           | 590 ms: 1.03x slower                                                         |
| Geometric mean             | (ref)                                                            | 1.01x faster                                                                 |

Benchmark hidden because not significant (2): async_tree_memoization_tg, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 80.2 ms                                                          | 76.3 ms: 1.05x faster                                                        |
| pidigits       | 254 ms                                                           | 262 ms: 1.03x slower                                                         |
| nbody          | 87.8 ms                                                          | 96.2 ms: 1.10x slower                                                        |
| Geometric mean | (ref)                                                            | 1.02x slower                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_dna      | 249 ms                                                           | 238 ms: 1.05x faster                                                         |
| regex_v8       | 26.0 ms                                                          | 25.3 ms: 1.03x faster                                                        |
| regex_compile  | 144 ms                                                           | 148 ms: 1.02x slower                                                         |
| regex_effbot   | 3.40 ms                                                          | 3.58 ms: 1.05x slower                                                        |
| Geometric mean | (ref)                                                            | 1.00x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| tomli_loads          | 2.40 sec                                                         | 2.18 sec: 1.11x faster                                                       |
| unpickle             | 15.7 us                                                          | 14.6 us: 1.07x faster                                                        |
| json_dumps           | 10.8 ms                                                          | 10.5 ms: 1.02x faster                                                        |
| xml_etree_iterparse  | 103 ms                                                           | 101 ms: 1.01x faster                                                         |
| xml_etree_process    | 59.7 ms                                                          | 59.2 ms: 1.01x faster                                                        |
| xml_etree_parse      | 144 ms                                                           | 143 ms: 1.00x faster                                                         |
| pickle               | 10.6 us                                                          | 10.7 us: 1.01x slower                                                        |
| pickle_pure_python   | 307 us                                                           | 310 us: 1.01x slower                                                         |
| json_loads           | 25.0 us                                                          | 25.4 us: 1.02x slower                                                        |
| unpickle_pure_python | 224 us                                                           | 233 us: 1.04x slower                                                         |
| pickle_dict          | 32.8 us                                                          | 34.6 us: 1.05x slower                                                        |
| Geometric mean       | (ref)                                                            | 1.01x faster                                                                 |

Benchmark hidden because not significant (3): unpickle_list, pickle_list, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|------------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 13.2 ms                                                          | 13.4 ms: 1.02x slower                                                        |
| python_startup_no_site | 8.85 ms                                                          | 11.8 ms: 1.33x slower                                                        |
| Geometric mean         | (ref)                                                            | 1.16x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako           | 10.4 ms                                                          | 10.0 ms: 1.03x faster                                                        |
| genshi_xml     | 58.1 ms                                                          | 60.9 ms: 1.05x slower                                                        |
| genshi_text    | 25.9 ms                                                          | 27.4 ms: 1.06x slower                                                        |
| Geometric mean | (ref)                                                            | 1.02x slower                                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 171 us                                                           | 123 us: 1.38x faster                                                         |
| richards_super             | 61.2 ms                                                          | 52.1 ms: 1.17x faster                                                        |
| richards                   | 53.4 ms                                                          | 45.8 ms: 1.17x faster                                                        |
| tomli_loads                | 2.40 sec                                                         | 2.18 sec: 1.11x faster                                                       |
| unpickle                   | 15.7 us                                                          | 14.6 us: 1.07x faster                                                        |
| create_gc_cycles           | 2.00 ms                                                          | 1.87 ms: 1.07x faster                                                        |
| gc_traversal               | 4.69 ms                                                          | 4.38 ms: 1.07x faster                                                        |
| async_tree_io_tg           | 900 ms                                                           | 855 ms: 1.05x faster                                                         |
| float                      | 80.2 ms                                                          | 76.3 ms: 1.05x faster                                                        |
| regex_dna                  | 249 ms                                                           | 238 ms: 1.05x faster                                                         |
| telco                      | 8.40 ms                                                          | 8.05 ms: 1.04x faster                                                        |
| spectral_norm              | 97.3 ms                                                          | 93.3 ms: 1.04x faster                                                        |
| async_tree_memoization     | 460 ms                                                           | 441 ms: 1.04x faster                                                         |
| scimark_sparse_mat_mult    | 4.28 ms                                                          | 4.13 ms: 1.04x faster                                                        |
| mako                       | 10.4 ms                                                          | 10.0 ms: 1.03x faster                                                        |
| async_tree_io              | 873 ms                                                           | 847 ms: 1.03x faster                                                         |
| regex_v8                   | 26.0 ms                                                          | 25.3 ms: 1.03x faster                                                        |
| sqlite_synth               | 2.80 us                                                          | 2.73 us: 1.02x faster                                                        |
| json_dumps                 | 10.8 ms                                                          | 10.5 ms: 1.02x faster                                                        |
| async_tree_none_tg         | 340 ms                                                           | 333 ms: 1.02x faster                                                         |
| logging_simple             | 6.40 us                                                          | 6.30 us: 1.02x faster                                                        |
| html5lib                   | 74.7 ms                                                          | 73.7 ms: 1.01x faster                                                        |
| xml_etree_iterparse        | 103 ms                                                           | 101 ms: 1.01x faster                                                         |
| asyncio_tcp                | 378 ms                                                           | 373 ms: 1.01x faster                                                         |
| xml_etree_process          | 59.7 ms                                                          | 59.2 ms: 1.01x faster                                                        |
| generators                 | 33.5 ms                                                          | 33.2 ms: 1.01x faster                                                        |
| xml_etree_parse            | 144 ms                                                           | 143 ms: 1.00x faster                                                         |
| asyncio_tcp_ssl            | 1.58 sec                                                         | 1.58 sec: 1.00x slower                                                       |
| coverage                   | 83.5 ms                                                          | 83.9 ms: 1.01x slower                                                        |
| dulwich_log                | 67.3 ms                                                          | 67.7 ms: 1.01x slower                                                        |
| pickle                     | 10.6 us                                                          | 10.7 us: 1.01x slower                                                        |
| pickle_pure_python         | 307 us                                                           | 310 us: 1.01x slower                                                         |
| sqlglot_normalize          | 120 ms                                                           | 121 ms: 1.01x slower                                                         |
| coroutines                 | 22.0 ms                                                          | 22.2 ms: 1.01x slower                                                        |
| json_loads                 | 25.0 us                                                          | 25.4 us: 1.02x slower                                                        |
| sqlglot_parse              | 1.39 ms                                                          | 1.41 ms: 1.02x slower                                                        |
| pprint_safe_repr           | 818 ms                                                           | 831 ms: 1.02x slower                                                         |
| python_startup             | 13.2 ms                                                          | 13.4 ms: 1.02x slower                                                        |
| json                       | 5.35 ms                                                          | 5.45 ms: 1.02x slower                                                        |
| logging_silent             | 96.3 ns                                                          | 98.1 ns: 1.02x slower                                                        |
| tornado_http               | 119 ms                                                           | 122 ms: 1.02x slower                                                         |
| 2to3                       | 291 ms                                                           | 298 ms: 1.02x slower                                                         |
| regex_compile              | 144 ms                                                           | 148 ms: 1.02x slower                                                         |
| pprint_pformat             | 1.66 sec                                                         | 1.70 sec: 1.02x slower                                                       |
| scimark_fft                | 312 ms                                                           | 320 ms: 1.02x slower                                                         |
| bench_thread_pool          | 908 us                                                           | 931 us: 1.03x slower                                                         |
| meteor_contest             | 128 ms                                                           | 132 ms: 1.03x slower                                                         |
| async_tree_none            | 365 ms                                                           | 375 ms: 1.03x slower                                                         |
| sqlglot_transpile          | 1.76 ms                                                          | 1.81 ms: 1.03x slower                                                        |
| sympy_expand               | 501 ms                                                           | 515 ms: 1.03x slower                                                         |
| dask                       | 391 ms                                                           | 403 ms: 1.03x slower                                                         |
| async_tree_cpu_io_mixed_tg | 573 ms                                                           | 590 ms: 1.03x slower                                                         |
| pidigits                   | 254 ms                                                           | 262 ms: 1.03x slower                                                         |
| deepcopy_reduce            | 3.39 us                                                          | 3.50 us: 1.03x slower                                                        |
| unpickle_pure_python       | 224 us                                                           | 233 us: 1.04x slower                                                         |
| docutils                   | 2.98 sec                                                         | 3.09 sec: 1.04x slower                                                       |
| pycparser                  | 1.22 sec                                                         | 1.27 sec: 1.04x slower                                                       |
| gunicorn                   | 1.04 ms                                                          | 1.09 ms: 1.04x slower                                                        |
| chameleon                  | 7.40 ms                                                          | 7.70 ms: 1.04x slower                                                        |
| raytrace                   | 260 ms                                                           | 271 ms: 1.04x slower                                                         |
| deepcopy_memo              | 37.3 us                                                          | 38.9 us: 1.04x slower                                                        |
| sympy_str                  | 295 ms                                                           | 308 ms: 1.05x slower                                                         |
| genshi_xml                 | 58.1 ms                                                          | 60.9 ms: 1.05x slower                                                        |
| regex_effbot               | 3.40 ms                                                          | 3.58 ms: 1.05x slower                                                        |
| sqlglot_optimize           | 59.5 ms                                                          | 62.7 ms: 1.05x slower                                                        |
| pickle_dict                | 32.8 us                                                          | 34.6 us: 1.05x slower                                                        |
| async_generators           | 363 ms                                                           | 382 ms: 1.05x slower                                                         |
| deepcopy                   | 377 us                                                           | 398 us: 1.05x slower                                                         |
| aiohttp                    | 1.07 ms                                                          | 1.13 ms: 1.06x slower                                                        |
| genshi_text                | 25.9 ms                                                          | 27.4 ms: 1.06x slower                                                        |
| crypto_pyaes               | 73.6 ms                                                          | 77.8 ms: 1.06x slower                                                        |
| mdp                        | 2.46 sec                                                         | 2.61 sec: 1.06x slower                                                       |
| sympy_sum                  | 155 ms                                                           | 164 ms: 1.06x slower                                                         |
| mypy2                      | 764 ms                                                           | 818 ms: 1.07x slower                                                         |
| chaos                      | 59.6 ms                                                          | 64.2 ms: 1.08x slower                                                        |
| scimark_monte_carlo        | 65.5 ms                                                          | 70.8 ms: 1.08x slower                                                        |
| sympy_integrate            | 23.2 ms                                                          | 25.3 ms: 1.09x slower                                                        |
| go                         | 165 ms                                                           | 180 ms: 1.09x slower                                                         |
| nbody                      | 87.8 ms                                                          | 96.2 ms: 1.10x slower                                                        |
| deltablue                  | 3.37 ms                                                          | 3.76 ms: 1.11x slower                                                        |
| hexiom                     | 6.35 ms                                                          | 7.17 ms: 1.13x slower                                                        |
| nqueens                    | 88.4 ms                                                          | 99.7 ms: 1.13x slower                                                        |
| fannkuch                   | 353 ms                                                           | 398 ms: 1.13x slower                                                         |
| comprehensions             | 17.0 us                                                          | 19.2 us: 1.13x slower                                                        |
| pathlib                    | 17.1 ms                                                          | 19.5 ms: 1.14x slower                                                        |
| scimark_lu                 | 97.5 ms                                                          | 128 ms: 1.32x slower                                                         |
| scimark_sor                | 119 ms                                                           | 156 ms: 1.32x slower                                                         |
| python_startup_no_site     | 8.85 ms                                                          | 11.8 ms: 1.33x slower                                                        |
| Geometric mean             | (ref)                                                            | 1.02x slower                                                                 |

Benchmark hidden because not significant (11): bench_mp_pool, pylint, asyncio_websockets, unpickle_list, logging_format, pickle_list, pyflate, async_tree_memoization_tg, xml_etree_generate, async_tree_cpu_io_mixed, thrift
Ignored benchmarks (3) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, django_template, flaskblogging

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.05x