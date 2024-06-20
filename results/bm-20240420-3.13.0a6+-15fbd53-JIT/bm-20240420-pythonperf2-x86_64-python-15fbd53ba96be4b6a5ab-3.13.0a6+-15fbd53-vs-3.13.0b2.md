# Results vs. 3.13.0b2

- fork: python
- ref: 15fbd53ba96be4b6a5ab
- machine: linux-x86_64
- commit hash: 15fbd53
- commit date: 2024-04-20
- overall geometric mean: 1.01x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.06x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 291 ms                                                           | 298 ms: 1.02x slower                                                         |
| chameleon      | 7.40 ms                                                          | 7.57 ms: 1.02x slower                                                        |
| docutils       | 2.98 sec                                                         | 3.05 sec: 1.02x slower                                                       |
| tornado_http   | 119 ms                                                           | 122 ms: 1.02x slower                                                         |
| Geometric mean | (ref)                                                            | 1.02x slower                                                                 |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none            | 365 ms                                                           | 372 ms: 1.02x slower                                                         |
| async_tree_cpu_io_mixed    | 604 ms                                                           | 617 ms: 1.02x slower                                                         |
| async_tree_io              | 873 ms                                                           | 903 ms: 1.03x slower                                                         |
| async_tree_cpu_io_mixed_tg | 573 ms                                                           | 595 ms: 1.04x slower                                                         |
| Geometric mean             | (ref)                                                            | 1.02x slower                                                                 |

Benchmark hidden because not significant (4): async_tree_io_tg, async_tree_none_tg, async_tree_memoization_tg, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 80.2 ms                                                          | 75.6 ms: 1.06x faster                                                        |
| pidigits       | 254 ms                                                           | 261 ms: 1.03x slower                                                         |
| nbody          | 87.8 ms                                                          | 98.2 ms: 1.12x slower                                                        |
| Geometric mean | (ref)                                                            | 1.03x slower                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_dna      | 249 ms                                                           | 241 ms: 1.04x faster                                                         |
| regex_v8       | 26.0 ms                                                          | 26.2 ms: 1.01x slower                                                        |
| regex_compile  | 144 ms                                                           | 145 ms: 1.01x slower                                                         |
| regex_effbot   | 3.40 ms                                                          | 3.47 ms: 1.02x slower                                                        |
| Geometric mean | (ref)                                                            | 1.00x faster                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| tomli_loads          | 2.40 sec                                                         | 2.14 sec: 1.12x faster                                                       |
| xml_etree_process    | 59.7 ms                                                          | 57.6 ms: 1.04x faster                                                        |
| unpickle             | 15.7 us                                                          | 15.3 us: 1.03x faster                                                        |
| xml_etree_generate   | 85.7 ms                                                          | 83.7 ms: 1.02x faster                                                        |
| unpickle_pure_python | 224 us                                                           | 219 us: 1.02x faster                                                         |
| unpickle_list        | 4.70 us                                                          | 4.60 us: 1.02x faster                                                        |
| xml_etree_iterparse  | 103 ms                                                           | 101 ms: 1.01x faster                                                         |
| pickle_dict          | 32.8 us                                                          | 32.5 us: 1.01x faster                                                        |
| json_loads           | 25.0 us                                                          | 24.8 us: 1.01x faster                                                        |
| pickle_list          | 4.44 us                                                          | 4.41 us: 1.01x faster                                                        |
| pickle_pure_python   | 307 us                                                           | 311 us: 1.01x slower                                                         |
| pickle               | 10.6 us                                                          | 10.8 us: 1.02x slower                                                        |
| Geometric mean       | (ref)                                                            | 1.02x faster                                                                 |

Benchmark hidden because not significant (2): json_dumps, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|------------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 13.2 ms                                                          | 13.5 ms: 1.02x slower                                                        |
| python_startup_no_site | 8.85 ms                                                          | 9.45 ms: 1.07x slower                                                        |
| Geometric mean         | (ref)                                                            | 1.05x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 10.4 ms                                                          | 9.93 ms: 1.04x faster                                                        |
| django_template | 39.0 ms                                                          | 39.4 ms: 1.01x slower                                                        |
| Geometric mean  | (ref)                                                            | 1.01x faster                                                                 |

Benchmark hidden because not significant (2): genshi_text, genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 171 us                                                           | 121 us: 1.41x faster                                                         |
| richards_super             | 61.2 ms                                                          | 52.2 ms: 1.17x faster                                                        |
| richards                   | 53.4 ms                                                          | 46.2 ms: 1.16x faster                                                        |
| tomli_loads                | 2.40 sec                                                         | 2.14 sec: 1.12x faster                                                       |
| gc_traversal               | 4.69 ms                                                          | 4.40 ms: 1.07x faster                                                        |
| create_gc_cycles           | 2.00 ms                                                          | 1.88 ms: 1.06x faster                                                        |
| float                      | 80.2 ms                                                          | 75.6 ms: 1.06x faster                                                        |
| bench_mp_pool              | 4.91 ms                                                          | 4.65 ms: 1.06x faster                                                        |
| coverage                   | 83.5 ms                                                          | 79.5 ms: 1.05x faster                                                        |
| spectral_norm              | 97.3 ms                                                          | 92.7 ms: 1.05x faster                                                        |
| mako                       | 10.4 ms                                                          | 9.93 ms: 1.04x faster                                                        |
| sqlite_synth               | 2.80 us                                                          | 2.68 us: 1.04x faster                                                        |
| telco                      | 8.40 ms                                                          | 8.06 ms: 1.04x faster                                                        |
| xml_etree_process          | 59.7 ms                                                          | 57.6 ms: 1.04x faster                                                        |
| regex_dna                  | 249 ms                                                           | 241 ms: 1.04x faster                                                         |
| logging_format             | 7.11 us                                                          | 6.89 us: 1.03x faster                                                        |
| unpickle                   | 15.7 us                                                          | 15.3 us: 1.03x faster                                                        |
| xml_etree_generate         | 85.7 ms                                                          | 83.7 ms: 1.02x faster                                                        |
| logging_simple             | 6.40 us                                                          | 6.25 us: 1.02x faster                                                        |
| unpickle_pure_python       | 224 us                                                           | 219 us: 1.02x faster                                                         |
| unpickle_list              | 4.70 us                                                          | 4.60 us: 1.02x faster                                                        |
| scimark_sparse_mat_mult    | 4.28 ms                                                          | 4.20 ms: 1.02x faster                                                        |
| logging_silent             | 96.3 ns                                                          | 94.7 ns: 1.02x faster                                                        |
| asyncio_websockets         | 395 ms                                                           | 390 ms: 1.01x faster                                                         |
| xml_etree_iterparse        | 103 ms                                                           | 101 ms: 1.01x faster                                                         |
| pickle_dict                | 32.8 us                                                          | 32.5 us: 1.01x faster                                                        |
| json_loads                 | 25.0 us                                                          | 24.8 us: 1.01x faster                                                        |
| dulwich_log                | 67.3 ms                                                          | 66.6 ms: 1.01x faster                                                        |
| asyncio_tcp                | 378 ms                                                           | 374 ms: 1.01x faster                                                         |
| pickle_list                | 4.44 us                                                          | 4.41 us: 1.01x faster                                                        |
| pyflate                    | 482 ms                                                           | 483 ms: 1.00x slower                                                         |
| regex_v8                   | 26.0 ms                                                          | 26.2 ms: 1.01x slower                                                        |
| coroutines                 | 22.0 ms                                                          | 22.1 ms: 1.01x slower                                                        |
| regex_compile              | 144 ms                                                           | 145 ms: 1.01x slower                                                         |
| django_template            | 39.0 ms                                                          | 39.4 ms: 1.01x slower                                                        |
| pickle_pure_python         | 307 us                                                           | 311 us: 1.01x slower                                                         |
| deepcopy                   | 377 us                                                           | 382 us: 1.01x slower                                                         |
| thrift                     | 880 us                                                           | 893 us: 1.02x slower                                                         |
| pprint_safe_repr           | 818 ms                                                           | 831 ms: 1.02x slower                                                         |
| pickle                     | 10.6 us                                                          | 10.8 us: 1.02x slower                                                        |
| sympy_expand               | 501 ms                                                           | 510 ms: 1.02x slower                                                         |
| async_tree_none            | 365 ms                                                           | 372 ms: 1.02x slower                                                         |
| pathlib                    | 17.1 ms                                                          | 17.5 ms: 1.02x slower                                                        |
| dask                       | 391 ms                                                           | 399 ms: 1.02x slower                                                         |
| regex_effbot               | 3.40 ms                                                          | 3.47 ms: 1.02x slower                                                        |
| 2to3                       | 291 ms                                                           | 298 ms: 1.02x slower                                                         |
| async_tree_cpu_io_mixed    | 604 ms                                                           | 617 ms: 1.02x slower                                                         |
| docutils                   | 2.98 sec                                                         | 3.05 sec: 1.02x slower                                                       |
| sqlglot_normalize          | 120 ms                                                           | 123 ms: 1.02x slower                                                         |
| chameleon                  | 7.40 ms                                                          | 7.57 ms: 1.02x slower                                                        |
| python_startup             | 13.2 ms                                                          | 13.5 ms: 1.02x slower                                                        |
| meteor_contest             | 128 ms                                                           | 131 ms: 1.02x slower                                                         |
| tornado_http               | 119 ms                                                           | 122 ms: 1.02x slower                                                         |
| pidigits                   | 254 ms                                                           | 261 ms: 1.03x slower                                                         |
| pprint_pformat             | 1.66 sec                                                         | 1.71 sec: 1.03x slower                                                       |
| sqlglot_parse              | 1.39 ms                                                          | 1.44 ms: 1.03x slower                                                        |
| async_tree_io              | 873 ms                                                           | 903 ms: 1.03x slower                                                         |
| sympy_str                  | 295 ms                                                           | 306 ms: 1.04x slower                                                         |
| async_tree_cpu_io_mixed_tg | 573 ms                                                           | 595 ms: 1.04x slower                                                         |
| sqlglot_transpile          | 1.76 ms                                                          | 1.84 ms: 1.04x slower                                                        |
| raytrace                   | 260 ms                                                           | 271 ms: 1.04x slower                                                         |
| gunicorn                   | 1.04 ms                                                          | 1.10 ms: 1.05x slower                                                        |
| sympy_sum                  | 155 ms                                                           | 162 ms: 1.05x slower                                                         |
| aiohttp                    | 1.07 ms                                                          | 1.13 ms: 1.05x slower                                                        |
| crypto_pyaes               | 73.6 ms                                                          | 77.3 ms: 1.05x slower                                                        |
| sqlglot_optimize           | 59.5 ms                                                          | 62.6 ms: 1.05x slower                                                        |
| mdp                        | 2.46 sec                                                         | 2.59 sec: 1.05x slower                                                       |
| fannkuch                   | 353 ms                                                           | 374 ms: 1.06x slower                                                         |
| pylint                     | 339 ms                                                           | 362 ms: 1.07x slower                                                         |
| python_startup_no_site     | 8.85 ms                                                          | 9.45 ms: 1.07x slower                                                        |
| async_generators           | 363 ms                                                           | 388 ms: 1.07x slower                                                         |
| mypy2                      | 764 ms                                                           | 820 ms: 1.07x slower                                                         |
| sympy_integrate            | 23.2 ms                                                          | 25.0 ms: 1.08x slower                                                        |
| go                         | 165 ms                                                           | 178 ms: 1.08x slower                                                         |
| chaos                      | 59.6 ms                                                          | 65.6 ms: 1.10x slower                                                        |
| scimark_monte_carlo        | 65.5 ms                                                          | 72.6 ms: 1.11x slower                                                        |
| nbody                      | 87.8 ms                                                          | 98.2 ms: 1.12x slower                                                        |
| hexiom                     | 6.35 ms                                                          | 7.15 ms: 1.13x slower                                                        |
| comprehensions             | 17.0 us                                                          | 19.2 us: 1.13x slower                                                        |
| deltablue                  | 3.37 ms                                                          | 3.83 ms: 1.13x slower                                                        |
| nqueens                    | 88.4 ms                                                          | 100 ms: 1.13x slower                                                         |
| scimark_sor                | 119 ms                                                           | 152 ms: 1.28x slower                                                         |
| scimark_lu                 | 97.5 ms                                                          | 125 ms: 1.29x slower                                                         |
| Geometric mean             | (ref)                                                            | 1.01x slower                                                                 |

Benchmark hidden because not significant (17): async_tree_io_tg, generators, json, deepcopy_memo, html5lib, async_tree_none_tg, json_dumps, asyncio_tcp_ssl, genshi_text, xml_etree_parse, genshi_xml, deepcopy_reduce, pycparser, scimark_fft, async_tree_memoization_tg, async_tree_memoization, bench_thread_pool
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.06x