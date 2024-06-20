# Results vs. 3.13.0b2

- fork: python
- ref: d610d821fd210dce63a1
- machine: linux-x86_64
- commit hash: d610d82
- commit date: 2024-03-23
- overall geometric mean: 1.01x faster
- HPT reliability: 86.14%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.97x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf2-x86_64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 291 ms                                                           | 291 ms: 1.00x faster                                                         |
| chameleon      | 7.40 ms                                                          | 7.36 ms: 1.01x faster                                                        |
| docutils       | 2.98 sec                                                         | 2.96 sec: 1.01x faster                                                       |
| html5lib       | 74.7 ms                                                          | 75.5 ms: 1.01x slower                                                        |
| tornado_http   | 119 ms                                                           | 121 ms: 1.01x slower                                                         |
| Geometric mean | (ref)                                                            | 1.00x slower                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf2-x86_64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|----------------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_memoization     | 460 ms                                                           | 438 ms: 1.05x faster                                                         |
| async_tree_io_tg           | 900 ms                                                           | 859 ms: 1.05x faster                                                         |
| async_tree_io              | 873 ms                                                           | 851 ms: 1.03x faster                                                         |
| async_tree_cpu_io_mixed_tg | 573 ms                                                           | 586 ms: 1.02x slower                                                         |
| async_tree_none            | 365 ms                                                           | 379 ms: 1.04x slower                                                         |
| Geometric mean             | (ref)                                                            | 1.00x faster                                                                 |

Benchmark hidden because not significant (3): async_tree_cpu_io_mixed, async_tree_none_tg, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf2-x86_64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 80.2 ms                                                          | 78.2 ms: 1.02x faster                                                        |
| pidigits       | 254 ms                                                           | 262 ms: 1.03x slower                                                         |
| Geometric mean | (ref)                                                            | 1.00x faster                                                                 |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf2-x86_64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_dna      | 249 ms                                                           | 233 ms: 1.07x faster                                                         |
| regex_v8       | 26.0 ms                                                          | 25.6 ms: 1.02x faster                                                        |
| regex_compile  | 144 ms                                                           | 144 ms: 1.00x faster                                                         |
| regex_effbot   | 3.40 ms                                                          | 3.70 ms: 1.09x slower                                                        |
| Geometric mean | (ref)                                                            | 1.00x faster                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf2-x86_64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|----------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| tomli_loads          | 2.40 sec                                                         | 2.21 sec: 1.09x faster                                                       |
| unpickle             | 15.7 us                                                          | 14.6 us: 1.07x faster                                                        |
| pickle_dict          | 32.8 us                                                          | 30.9 us: 1.06x faster                                                        |
| unpickle_list        | 4.70 us                                                          | 4.47 us: 1.05x faster                                                        |
| xml_etree_generate   | 85.7 ms                                                          | 82.0 ms: 1.04x faster                                                        |
| pickle               | 10.6 us                                                          | 10.2 us: 1.04x faster                                                        |
| xml_etree_process    | 59.7 ms                                                          | 57.8 ms: 1.03x faster                                                        |
| json_dumps           | 10.8 ms                                                          | 10.5 ms: 1.02x faster                                                        |
| pickle_list          | 4.44 us                                                          | 4.37 us: 1.02x faster                                                        |
| unpickle_pure_python | 224 us                                                           | 223 us: 1.00x faster                                                         |
| json_loads           | 25.0 us                                                          | 25.2 us: 1.01x slower                                                        |
| xml_etree_iterparse  | 103 ms                                                           | 105 ms: 1.03x slower                                                         |
| xml_etree_parse      | 144 ms                                                           | 150 ms: 1.04x slower                                                         |
| Geometric mean       | (ref)                                                            | 1.03x faster                                                                 |

Benchmark hidden because not significant (1): pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf2-x86_64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|------------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 13.2 ms                                                          | 12.7 ms: 1.04x faster                                                        |
| python_startup_no_site | 8.85 ms                                                          | 11.0 ms: 1.24x slower                                                        |
| Geometric mean         | (ref)                                                            | 1.09x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf2-x86_64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|-----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| genshi_xml      | 58.1 ms                                                          | 54.0 ms: 1.07x faster                                                        |
| genshi_text     | 25.9 ms                                                          | 25.2 ms: 1.03x faster                                                        |
| mako            | 10.4 ms                                                          | 10.2 ms: 1.02x faster                                                        |
| django_template | 39.0 ms                                                          | 40.9 ms: 1.05x slower                                                        |
| Geometric mean  | (ref)                                                            | 1.02x faster                                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf2-x86_64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|----------------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 171 us                                                           | 113 us: 1.51x faster                                                         |
| create_gc_cycles           | 2.00 ms                                                          | 1.52 ms: 1.32x faster                                                        |
| gc_traversal               | 4.69 ms                                                          | 4.30 ms: 1.09x faster                                                        |
| tomli_loads                | 2.40 sec                                                         | 2.21 sec: 1.09x faster                                                       |
| genshi_xml                 | 58.1 ms                                                          | 54.0 ms: 1.07x faster                                                        |
| unpickle                   | 15.7 us                                                          | 14.6 us: 1.07x faster                                                        |
| regex_dna                  | 249 ms                                                           | 233 ms: 1.07x faster                                                         |
| pickle_dict                | 32.8 us                                                          | 30.9 us: 1.06x faster                                                        |
| telco                      | 8.40 ms                                                          | 7.91 ms: 1.06x faster                                                        |
| spectral_norm              | 97.3 ms                                                          | 92.2 ms: 1.06x faster                                                        |
| scimark_fft                | 312 ms                                                           | 296 ms: 1.05x faster                                                         |
| unpickle_list              | 4.70 us                                                          | 4.47 us: 1.05x faster                                                        |
| async_tree_memoization     | 460 ms                                                           | 438 ms: 1.05x faster                                                         |
| async_tree_io_tg           | 900 ms                                                           | 859 ms: 1.05x faster                                                         |
| xml_etree_generate         | 85.7 ms                                                          | 82.0 ms: 1.04x faster                                                        |
| coverage                   | 83.5 ms                                                          | 79.9 ms: 1.04x faster                                                        |
| pickle                     | 10.6 us                                                          | 10.2 us: 1.04x faster                                                        |
| python_startup             | 13.2 ms                                                          | 12.7 ms: 1.04x faster                                                        |
| pprint_safe_repr           | 818 ms                                                           | 789 ms: 1.04x faster                                                         |
| xml_etree_process          | 59.7 ms                                                          | 57.8 ms: 1.03x faster                                                        |
| crypto_pyaes               | 73.6 ms                                                          | 71.2 ms: 1.03x faster                                                        |
| scimark_lu                 | 97.5 ms                                                          | 94.4 ms: 1.03x faster                                                        |
| pprint_pformat             | 1.66 sec                                                         | 1.61 sec: 1.03x faster                                                       |
| deepcopy_memo              | 37.3 us                                                          | 36.3 us: 1.03x faster                                                        |
| deepcopy                   | 377 us                                                           | 368 us: 1.03x faster                                                         |
| genshi_text                | 25.9 ms                                                          | 25.2 ms: 1.03x faster                                                        |
| async_tree_io              | 873 ms                                                           | 851 ms: 1.03x faster                                                         |
| asyncio_websockets         | 395 ms                                                           | 385 ms: 1.03x faster                                                         |
| deepcopy_reduce            | 3.39 us                                                          | 3.30 us: 1.03x faster                                                        |
| float                      | 80.2 ms                                                          | 78.2 ms: 1.02x faster                                                        |
| async_generators           | 363 ms                                                           | 354 ms: 1.02x faster                                                         |
| json_dumps                 | 10.8 ms                                                          | 10.5 ms: 1.02x faster                                                        |
| sqlglot_normalize          | 120 ms                                                           | 118 ms: 1.02x faster                                                         |
| sympy_sum                  | 155 ms                                                           | 152 ms: 1.02x faster                                                         |
| sqlite_synth               | 2.80 us                                                          | 2.74 us: 1.02x faster                                                        |
| mako                       | 10.4 ms                                                          | 10.2 ms: 1.02x faster                                                        |
| pickle_list                | 4.44 us                                                          | 4.37 us: 1.02x faster                                                        |
| regex_v8                   | 26.0 ms                                                          | 25.6 ms: 1.02x faster                                                        |
| asyncio_tcp                | 378 ms                                                           | 371 ms: 1.02x faster                                                         |
| sympy_str                  | 295 ms                                                           | 290 ms: 1.02x faster                                                         |
| comprehensions             | 17.0 us                                                          | 16.7 us: 1.01x faster                                                        |
| thrift                     | 880 us                                                           | 868 us: 1.01x faster                                                         |
| richards_super             | 61.2 ms                                                          | 60.4 ms: 1.01x faster                                                        |
| sympy_expand               | 501 ms                                                           | 496 ms: 1.01x faster                                                         |
| nqueens                    | 88.4 ms                                                          | 87.5 ms: 1.01x faster                                                        |
| sqlglot_parse              | 1.39 ms                                                          | 1.38 ms: 1.01x faster                                                        |
| docutils                   | 2.98 sec                                                         | 2.96 sec: 1.01x faster                                                       |
| sqlglot_optimize           | 59.5 ms                                                          | 59.2 ms: 1.01x faster                                                        |
| chameleon                  | 7.40 ms                                                          | 7.36 ms: 1.01x faster                                                        |
| sympy_integrate            | 23.2 ms                                                          | 23.1 ms: 1.00x faster                                                        |
| unpickle_pure_python       | 224 us                                                           | 223 us: 1.00x faster                                                         |
| regex_compile              | 144 ms                                                           | 144 ms: 1.00x faster                                                         |
| 2to3                       | 291 ms                                                           | 291 ms: 1.00x faster                                                         |
| asyncio_tcp_ssl            | 1.58 sec                                                         | 1.58 sec: 1.00x faster                                                       |
| meteor_contest             | 128 ms                                                           | 129 ms: 1.00x slower                                                         |
| json_loads                 | 25.0 us                                                          | 25.2 us: 1.01x slower                                                        |
| scimark_monte_carlo        | 65.5 ms                                                          | 66.0 ms: 1.01x slower                                                        |
| json                       | 5.35 ms                                                          | 5.40 ms: 1.01x slower                                                        |
| dulwich_log                | 67.3 ms                                                          | 68.0 ms: 1.01x slower                                                        |
| tornado_http               | 119 ms                                                           | 121 ms: 1.01x slower                                                         |
| mdp                        | 2.46 sec                                                         | 2.49 sec: 1.01x slower                                                       |
| html5lib                   | 74.7 ms                                                          | 75.5 ms: 1.01x slower                                                        |
| richards                   | 53.4 ms                                                          | 54.4 ms: 1.02x slower                                                        |
| raytrace                   | 260 ms                                                           | 265 ms: 1.02x slower                                                         |
| chaos                      | 59.6 ms                                                          | 60.9 ms: 1.02x slower                                                        |
| async_tree_cpu_io_mixed_tg | 573 ms                                                           | 586 ms: 1.02x slower                                                         |
| xml_etree_iterparse        | 103 ms                                                           | 105 ms: 1.03x slower                                                         |
| pycparser                  | 1.22 sec                                                         | 1.26 sec: 1.03x slower                                                       |
| logging_simple             | 6.40 us                                                          | 6.58 us: 1.03x slower                                                        |
| coroutines                 | 22.0 ms                                                          | 22.7 ms: 1.03x slower                                                        |
| pidigits                   | 254 ms                                                           | 262 ms: 1.03x slower                                                         |
| logging_format             | 7.11 us                                                          | 7.35 us: 1.03x slower                                                        |
| async_tree_none            | 365 ms                                                           | 379 ms: 1.04x slower                                                         |
| xml_etree_parse            | 144 ms                                                           | 150 ms: 1.04x slower                                                         |
| deltablue                  | 3.37 ms                                                          | 3.52 ms: 1.04x slower                                                        |
| go                         | 165 ms                                                           | 173 ms: 1.05x slower                                                         |
| django_template            | 39.0 ms                                                          | 40.9 ms: 1.05x slower                                                        |
| regex_effbot               | 3.40 ms                                                          | 3.70 ms: 1.09x slower                                                        |
| pyflate                    | 482 ms                                                           | 525 ms: 1.09x slower                                                         |
| fannkuch                   | 353 ms                                                           | 385 ms: 1.09x slower                                                         |
| pathlib                    | 17.1 ms                                                          | 19.1 ms: 1.12x slower                                                        |
| scimark_sor                | 119 ms                                                           | 140 ms: 1.18x slower                                                         |
| python_startup_no_site     | 8.85 ms                                                          | 11.0 ms: 1.24x slower                                                        |
| Geometric mean             | (ref)                                                            | 1.01x faster                                                                 |

Benchmark hidden because not significant (17): bench_mp_pool, nbody, gunicorn, bench_thread_pool, async_tree_cpu_io_mixed, aiohttp, pickle_pure_python, sqlglot_transpile, logging_silent, generators, hexiom, dask, scimark_sparse_mat_mult, async_tree_none_tg, mypy2, pylint, async_tree_memoization_tg
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging
Ignored benchmarks (1) of results/bm-20240323-3.13.0a5+-d610d82/bm-20240323-pythonperf2-x86_64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82.json: unpack_sequence

# HPT report

- Reliability score: 86.14% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.97x