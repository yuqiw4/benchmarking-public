# Results vs. 3.13.0b2

- fork: mdboom
- ref: tier2_pystats_misses
- machine: linux-x86_64
- commit hash: ee60448
- commit date: 2024-04-02
- overall geometric mean: 1.03x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.06x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-pythonperf2-x86_64-mdboom-tier2_pystats_misses-3.13.0a5+-ee60448 |
|----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 291 ms                                                           | 300 ms: 1.03x slower                                                         |
| chameleon      | 7.40 ms                                                          | 7.54 ms: 1.02x slower                                                        |
| docutils       | 2.98 sec                                                         | 3.11 sec: 1.04x slower                                                       |
| html5lib       | 74.7 ms                                                          | 72.6 ms: 1.03x faster                                                        |
| tornado_http   | 119 ms                                                           | 125 ms: 1.04x slower                                                         |
| Geometric mean | (ref)                                                            | 1.02x slower                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-pythonperf2-x86_64-mdboom-tier2_pystats_misses-3.13.0a5+-ee60448 |
|----------------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_io_tg           | 900 ms                                                           | 858 ms: 1.05x faster                                                         |
| async_tree_memoization     | 460 ms                                                           | 440 ms: 1.04x faster                                                         |
| async_tree_none_tg         | 340 ms                                                           | 333 ms: 1.02x faster                                                         |
| async_tree_cpu_io_mixed_tg | 573 ms                                                           | 588 ms: 1.03x slower                                                         |
| async_tree_none            | 365 ms                                                           | 377 ms: 1.03x slower                                                         |
| Geometric mean             | (ref)                                                            | 1.01x faster                                                                 |

Benchmark hidden because not significant (3): async_tree_io, async_tree_cpu_io_mixed, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-pythonperf2-x86_64-mdboom-tier2_pystats_misses-3.13.0a5+-ee60448 |
|----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 80.2 ms                                                          | 76.6 ms: 1.05x faster                                                        |
| pidigits       | 254 ms                                                           | 261 ms: 1.03x slower                                                         |
| nbody          | 87.8 ms                                                          | 95.6 ms: 1.09x slower                                                        |
| Geometric mean | (ref)                                                            | 1.02x slower                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-pythonperf2-x86_64-mdboom-tier2_pystats_misses-3.13.0a5+-ee60448 |
|----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_v8       | 26.0 ms                                                          | 25.9 ms: 1.01x faster                                                        |
| regex_dna      | 249 ms                                                           | 249 ms: 1.00x faster                                                         |
| regex_effbot   | 3.40 ms                                                          | 3.51 ms: 1.03x slower                                                        |
| regex_compile  | 144 ms                                                           | 150 ms: 1.04x slower                                                         |
| Geometric mean | (ref)                                                            | 1.02x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-pythonperf2-x86_64-mdboom-tier2_pystats_misses-3.13.0a5+-ee60448 |
|----------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| tomli_loads          | 2.40 sec                                                         | 2.13 sec: 1.13x faster                                                       |
| unpickle             | 15.7 us                                                          | 14.5 us: 1.08x faster                                                        |
| json_dumps           | 10.8 ms                                                          | 10.5 ms: 1.03x faster                                                        |
| xml_etree_process    | 59.7 ms                                                          | 58.8 ms: 1.02x faster                                                        |
| xml_etree_generate   | 85.7 ms                                                          | 84.9 ms: 1.01x faster                                                        |
| pickle_list          | 4.44 us                                                          | 4.40 us: 1.01x faster                                                        |
| xml_etree_iterparse  | 103 ms                                                           | 102 ms: 1.00x faster                                                         |
| pickle               | 10.6 us                                                          | 10.7 us: 1.01x slower                                                        |
| xml_etree_parse      | 144 ms                                                           | 145 ms: 1.01x slower                                                         |
| pickle_pure_python   | 307 us                                                           | 311 us: 1.01x slower                                                         |
| json_loads           | 25.0 us                                                          | 25.4 us: 1.02x slower                                                        |
| unpickle_pure_python | 224 us                                                           | 232 us: 1.03x slower                                                         |
| Geometric mean       | (ref)                                                            | 1.01x faster                                                                 |

Benchmark hidden because not significant (2): pickle_dict, unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-pythonperf2-x86_64-mdboom-tier2_pystats_misses-3.13.0a5+-ee60448 |
|------------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 13.2 ms                                                          | 13.7 ms: 1.03x slower                                                        |
| python_startup_no_site | 8.85 ms                                                          | 11.9 ms: 1.34x slower                                                        |
| Geometric mean         | (ref)                                                            | 1.18x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-pythonperf2-x86_64-mdboom-tier2_pystats_misses-3.13.0a5+-ee60448 |
|----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako           | 10.4 ms                                                          | 9.96 ms: 1.04x faster                                                        |
| genshi_xml     | 58.1 ms                                                          | 61.8 ms: 1.06x slower                                                        |
| genshi_text    | 25.9 ms                                                          | 28.5 ms: 1.10x slower                                                        |
| Geometric mean | (ref)                                                            | 1.04x slower                                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-pythonperf2-x86_64-mdboom-tier2_pystats_misses-3.13.0a5+-ee60448 |
|----------------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 171 us                                                           | 124 us: 1.38x faster                                                         |
| tomli_loads                | 2.40 sec                                                         | 2.13 sec: 1.13x faster                                                       |
| unpickle                   | 15.7 us                                                          | 14.5 us: 1.08x faster                                                        |
| create_gc_cycles           | 2.00 ms                                                          | 1.88 ms: 1.07x faster                                                        |
| richards                   | 53.4 ms                                                          | 50.6 ms: 1.06x faster                                                        |
| spectral_norm              | 97.3 ms                                                          | 92.6 ms: 1.05x faster                                                        |
| richards_super             | 61.2 ms                                                          | 58.3 ms: 1.05x faster                                                        |
| async_tree_io_tg           | 900 ms                                                           | 858 ms: 1.05x faster                                                         |
| telco                      | 8.40 ms                                                          | 8.01 ms: 1.05x faster                                                        |
| float                      | 80.2 ms                                                          | 76.6 ms: 1.05x faster                                                        |
| sqlite_synth               | 2.80 us                                                          | 2.68 us: 1.05x faster                                                        |
| async_tree_memoization     | 460 ms                                                           | 440 ms: 1.04x faster                                                         |
| scimark_sparse_mat_mult    | 4.28 ms                                                          | 4.11 ms: 1.04x faster                                                        |
| mako                       | 10.4 ms                                                          | 9.96 ms: 1.04x faster                                                        |
| html5lib                   | 74.7 ms                                                          | 72.6 ms: 1.03x faster                                                        |
| json_dumps                 | 10.8 ms                                                          | 10.5 ms: 1.03x faster                                                        |
| async_tree_none_tg         | 340 ms                                                           | 333 ms: 1.02x faster                                                         |
| xml_etree_process          | 59.7 ms                                                          | 58.8 ms: 1.02x faster                                                        |
| thrift                     | 880 us                                                           | 871 us: 1.01x faster                                                         |
| xml_etree_generate         | 85.7 ms                                                          | 84.9 ms: 1.01x faster                                                        |
| pickle_list                | 4.44 us                                                          | 4.40 us: 1.01x faster                                                        |
| generators                 | 33.5 ms                                                          | 33.2 ms: 1.01x faster                                                        |
| coverage                   | 83.5 ms                                                          | 82.9 ms: 1.01x faster                                                        |
| regex_v8                   | 26.0 ms                                                          | 25.9 ms: 1.01x faster                                                        |
| logging_silent             | 96.3 ns                                                          | 95.7 ns: 1.01x faster                                                        |
| asyncio_tcp                | 378 ms                                                           | 376 ms: 1.01x faster                                                         |
| xml_etree_iterparse        | 103 ms                                                           | 102 ms: 1.00x faster                                                         |
| regex_dna                  | 249 ms                                                           | 249 ms: 1.00x faster                                                         |
| coroutines                 | 22.0 ms                                                          | 22.1 ms: 1.00x slower                                                        |
| logging_simple             | 6.40 us                                                          | 6.43 us: 1.00x slower                                                        |
| pyflate                    | 482 ms                                                           | 485 ms: 1.01x slower                                                         |
| pickle                     | 10.6 us                                                          | 10.7 us: 1.01x slower                                                        |
| xml_etree_parse            | 144 ms                                                           | 145 ms: 1.01x slower                                                         |
| sqlglot_normalize          | 120 ms                                                           | 122 ms: 1.01x slower                                                         |
| pickle_pure_python         | 307 us                                                           | 311 us: 1.01x slower                                                         |
| json_loads                 | 25.0 us                                                          | 25.4 us: 1.02x slower                                                        |
| chameleon                  | 7.40 ms                                                          | 7.54 ms: 1.02x slower                                                        |
| json                       | 5.35 ms                                                          | 5.48 ms: 1.02x slower                                                        |
| sqlglot_parse              | 1.39 ms                                                          | 1.43 ms: 1.03x slower                                                        |
| async_tree_cpu_io_mixed_tg | 573 ms                                                           | 588 ms: 1.03x slower                                                         |
| 2to3                       | 291 ms                                                           | 300 ms: 1.03x slower                                                         |
| pidigits                   | 254 ms                                                           | 261 ms: 1.03x slower                                                         |
| async_tree_none            | 365 ms                                                           | 377 ms: 1.03x slower                                                         |
| regex_effbot               | 3.40 ms                                                          | 3.51 ms: 1.03x slower                                                        |
| unpickle_pure_python       | 224 us                                                           | 232 us: 1.03x slower                                                         |
| gc_traversal               | 4.69 ms                                                          | 4.84 ms: 1.03x slower                                                        |
| python_startup             | 13.2 ms                                                          | 13.7 ms: 1.03x slower                                                        |
| sympy_expand               | 501 ms                                                           | 518 ms: 1.03x slower                                                         |
| deepcopy_reduce            | 3.39 us                                                          | 3.51 us: 1.04x slower                                                        |
| dask                       | 391 ms                                                           | 405 ms: 1.04x slower                                                         |
| regex_compile              | 144 ms                                                           | 150 ms: 1.04x slower                                                         |
| sqlglot_transpile          | 1.76 ms                                                          | 1.84 ms: 1.04x slower                                                        |
| docutils                   | 2.98 sec                                                         | 3.11 sec: 1.04x slower                                                       |
| pprint_safe_repr           | 818 ms                                                           | 852 ms: 1.04x slower                                                         |
| tornado_http               | 119 ms                                                           | 125 ms: 1.04x slower                                                         |
| pycparser                  | 1.22 sec                                                         | 1.28 sec: 1.04x slower                                                       |
| crypto_pyaes               | 73.6 ms                                                          | 76.9 ms: 1.05x slower                                                        |
| deepcopy                   | 377 us                                                           | 395 us: 1.05x slower                                                         |
| sqlglot_optimize           | 59.5 ms                                                          | 62.4 ms: 1.05x slower                                                        |
| meteor_contest             | 128 ms                                                           | 134 ms: 1.05x slower                                                         |
| deepcopy_memo              | 37.3 us                                                          | 39.4 us: 1.06x slower                                                        |
| mdp                        | 2.46 sec                                                         | 2.60 sec: 1.06x slower                                                       |
| sympy_str                  | 295 ms                                                           | 312 ms: 1.06x slower                                                         |
| pprint_pformat             | 1.66 sec                                                         | 1.76 sec: 1.06x slower                                                       |
| deltablue                  | 3.37 ms                                                          | 3.58 ms: 1.06x slower                                                        |
| aiohttp                    | 1.07 ms                                                          | 1.14 ms: 1.06x slower                                                        |
| genshi_xml                 | 58.1 ms                                                          | 61.8 ms: 1.06x slower                                                        |
| dulwich_log                | 67.3 ms                                                          | 71.7 ms: 1.07x slower                                                        |
| gunicorn                   | 1.04 ms                                                          | 1.12 ms: 1.07x slower                                                        |
| go                         | 165 ms                                                           | 177 ms: 1.07x slower                                                         |
| chaos                      | 59.6 ms                                                          | 64.1 ms: 1.07x slower                                                        |
| scimark_monte_carlo        | 65.5 ms                                                          | 70.6 ms: 1.08x slower                                                        |
| sympy_sum                  | 155 ms                                                           | 167 ms: 1.08x slower                                                         |
| async_generators           | 363 ms                                                           | 393 ms: 1.08x slower                                                         |
| nbody                      | 87.8 ms                                                          | 95.6 ms: 1.09x slower                                                        |
| mypy2                      | 764 ms                                                           | 834 ms: 1.09x slower                                                         |
| fannkuch                   | 353 ms                                                           | 386 ms: 1.09x slower                                                         |
| genshi_text                | 25.9 ms                                                          | 28.5 ms: 1.10x slower                                                        |
| raytrace                   | 260 ms                                                           | 287 ms: 1.10x slower                                                         |
| sympy_integrate            | 23.2 ms                                                          | 25.9 ms: 1.12x slower                                                        |
| comprehensions             | 17.0 us                                                          | 19.2 us: 1.13x slower                                                        |
| pathlib                    | 17.1 ms                                                          | 19.7 ms: 1.15x slower                                                        |
| hexiom                     | 6.35 ms                                                          | 7.33 ms: 1.15x slower                                                        |
| nqueens                    | 88.4 ms                                                          | 105 ms: 1.19x slower                                                         |
| bench_thread_pool          | 908 us                                                           | 1.11 ms: 1.23x slower                                                        |
| scimark_sor                | 119 ms                                                           | 152 ms: 1.28x slower                                                         |
| scimark_lu                 | 97.5 ms                                                          | 126 ms: 1.29x slower                                                         |
| python_startup_no_site     | 8.85 ms                                                          | 11.9 ms: 1.34x slower                                                        |
| Geometric mean             | (ref)                                                            | 1.03x slower                                                                 |

Benchmark hidden because not significant (11): async_tree_io, async_tree_cpu_io_mixed, logging_format, pickle_dict, unpickle_list, asyncio_tcp_ssl, asyncio_websockets, pylint, scimark_fft, async_tree_memoization_tg, bench_mp_pool
Ignored benchmarks (3) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, django_template, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.06x