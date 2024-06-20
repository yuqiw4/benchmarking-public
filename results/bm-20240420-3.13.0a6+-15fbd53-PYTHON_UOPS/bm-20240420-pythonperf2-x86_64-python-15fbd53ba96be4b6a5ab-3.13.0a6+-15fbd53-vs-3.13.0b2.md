# Results vs. 3.13.0b2

- fork: python
- ref: 15fbd53ba96be4b6a5ab
- machine: linux-x86_64
- commit hash: 15fbd53
- commit date: 2024-04-20
- overall geometric mean: 1.09x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x slower
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 291 ms                                                           | 314 ms: 1.08x slower                                                         |
| chameleon      | 7.40 ms                                                          | 8.34 ms: 1.13x slower                                                        |
| docutils       | 2.98 sec                                                         | 3.24 sec: 1.09x slower                                                       |
| html5lib       | 74.7 ms                                                          | 79.0 ms: 1.06x slower                                                        |
| tornado_http   | 119 ms                                                           | 127 ms: 1.06x slower                                                         |
| Geometric mean | (ref)                                                            | 1.08x slower                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none_tg         | 340 ms                                                           | 352 ms: 1.03x slower                                                         |
| async_tree_memoization     | 460 ms                                                           | 478 ms: 1.04x slower                                                         |
| async_tree_memoization_tg  | 421 ms                                                           | 438 ms: 1.04x slower                                                         |
| async_tree_cpu_io_mixed    | 604 ms                                                           | 631 ms: 1.04x slower                                                         |
| async_tree_none            | 365 ms                                                           | 384 ms: 1.05x slower                                                         |
| async_tree_io              | 873 ms                                                           | 919 ms: 1.05x slower                                                         |
| async_tree_cpu_io_mixed_tg | 573 ms                                                           | 604 ms: 1.06x slower                                                         |
| Geometric mean             | (ref)                                                            | 1.04x slower                                                                 |

Benchmark hidden because not significant (1): async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pidigits       | 254 ms                                                           | 263 ms: 1.04x slower                                                         |
| float          | 80.2 ms                                                          | 84.7 ms: 1.06x slower                                                        |
| nbody          | 87.8 ms                                                          | 110 ms: 1.25x slower                                                         |
| Geometric mean | (ref)                                                            | 1.11x slower                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_dna      | 249 ms                                                           | 242 ms: 1.03x faster                                                         |
| regex_v8       | 26.0 ms                                                          | 25.6 ms: 1.02x faster                                                        |
| regex_effbot   | 3.40 ms                                                          | 3.63 ms: 1.07x slower                                                        |
| regex_compile  | 144 ms                                                           | 194 ms: 1.35x slower                                                         |
| Geometric mean | (ref)                                                            | 1.08x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pickle_dict          | 32.8 us                                                          | 30.6 us: 1.07x faster                                                        |
| unpickle_list        | 4.70 us                                                          | 4.58 us: 1.03x faster                                                        |
| unpickle             | 15.7 us                                                          | 15.3 us: 1.02x faster                                                        |
| json_loads           | 25.0 us                                                          | 24.5 us: 1.02x faster                                                        |
| pickle               | 10.6 us                                                          | 10.4 us: 1.02x faster                                                        |
| json_dumps           | 10.8 ms                                                          | 10.7 ms: 1.00x faster                                                        |
| pickle_list          | 4.44 us                                                          | 4.52 us: 1.02x slower                                                        |
| xml_etree_process    | 59.7 ms                                                          | 61.2 ms: 1.02x slower                                                        |
| xml_etree_generate   | 85.7 ms                                                          | 88.5 ms: 1.03x slower                                                        |
| xml_etree_parse      | 144 ms                                                           | 149 ms: 1.04x slower                                                         |
| pickle_pure_python   | 307 us                                                           | 320 us: 1.04x slower                                                         |
| xml_etree_iterparse  | 103 ms                                                           | 110 ms: 1.07x slower                                                         |
| tomli_loads          | 2.40 sec                                                         | 2.73 sec: 1.14x slower                                                       |
| unpickle_pure_python | 224 us                                                           | 283 us: 1.26x slower                                                         |
| Geometric mean       | (ref)                                                            | 1.03x slower                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|------------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 13.2 ms                                                          | 12.9 ms: 1.02x faster                                                        |
| python_startup_no_site | 8.85 ms                                                          | 8.90 ms: 1.01x slower                                                        |
| Geometric mean         | (ref)                                                            | 1.01x faster                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| genshi_xml      | 58.1 ms                                                          | 60.2 ms: 1.04x slower                                                        |
| genshi_text     | 25.9 ms                                                          | 27.5 ms: 1.06x slower                                                        |
| django_template | 39.0 ms                                                          | 41.5 ms: 1.07x slower                                                        |
| mako            | 10.4 ms                                                          | 13.0 ms: 1.25x slower                                                        |
| Geometric mean  | (ref)                                                            | 1.10x slower                                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 171 us                                                           | 126 us: 1.36x faster                                                         |
| pickle_dict                | 32.8 us                                                          | 30.6 us: 1.07x faster                                                        |
| gc_traversal               | 4.69 ms                                                          | 4.44 ms: 1.06x faster                                                        |
| create_gc_cycles           | 2.00 ms                                                          | 1.94 ms: 1.03x faster                                                        |
| regex_dna                  | 249 ms                                                           | 242 ms: 1.03x faster                                                         |
| richards_super             | 61.2 ms                                                          | 59.6 ms: 1.03x faster                                                        |
| unpickle_list              | 4.70 us                                                          | 4.58 us: 1.03x faster                                                        |
| unpickle                   | 15.7 us                                                          | 15.3 us: 1.02x faster                                                        |
| python_startup             | 13.2 ms                                                          | 12.9 ms: 1.02x faster                                                        |
| coverage                   | 83.5 ms                                                          | 81.8 ms: 1.02x faster                                                        |
| json_loads                 | 25.0 us                                                          | 24.5 us: 1.02x faster                                                        |
| regex_v8                   | 26.0 ms                                                          | 25.6 ms: 1.02x faster                                                        |
| pickle                     | 10.6 us                                                          | 10.4 us: 1.02x faster                                                        |
| asyncio_websockets         | 395 ms                                                           | 390 ms: 1.01x faster                                                         |
| json_dumps                 | 10.8 ms                                                          | 10.7 ms: 1.00x faster                                                        |
| python_startup_no_site     | 8.85 ms                                                          | 8.90 ms: 1.01x slower                                                        |
| coroutines                 | 22.0 ms                                                          | 22.2 ms: 1.01x slower                                                        |
| sqlite_synth               | 2.80 us                                                          | 2.82 us: 1.01x slower                                                        |
| asyncio_tcp_ssl            | 1.58 sec                                                         | 1.60 sec: 1.01x slower                                                       |
| generators                 | 33.5 ms                                                          | 34.0 ms: 1.01x slower                                                        |
| pickle_list                | 4.44 us                                                          | 4.52 us: 1.02x slower                                                        |
| logging_silent             | 96.3 ns                                                          | 98.1 ns: 1.02x slower                                                        |
| thrift                     | 880 us                                                           | 899 us: 1.02x slower                                                         |
| deepcopy_reduce            | 3.39 us                                                          | 3.47 us: 1.02x slower                                                        |
| xml_etree_process          | 59.7 ms                                                          | 61.2 ms: 1.02x slower                                                        |
| xml_etree_generate         | 85.7 ms                                                          | 88.5 ms: 1.03x slower                                                        |
| telco                      | 8.40 ms                                                          | 8.67 ms: 1.03x slower                                                        |
| async_tree_none_tg         | 340 ms                                                           | 352 ms: 1.03x slower                                                         |
| xml_etree_parse            | 144 ms                                                           | 149 ms: 1.04x slower                                                         |
| genshi_xml                 | 58.1 ms                                                          | 60.2 ms: 1.04x slower                                                        |
| pidigits                   | 254 ms                                                           | 263 ms: 1.04x slower                                                         |
| async_tree_memoization     | 460 ms                                                           | 478 ms: 1.04x slower                                                         |
| pickle_pure_python         | 307 us                                                           | 320 us: 1.04x slower                                                         |
| pathlib                    | 17.1 ms                                                          | 17.8 ms: 1.04x slower                                                        |
| async_tree_memoization_tg  | 421 ms                                                           | 438 ms: 1.04x slower                                                         |
| async_tree_cpu_io_mixed    | 604 ms                                                           | 631 ms: 1.04x slower                                                         |
| dask                       | 391 ms                                                           | 410 ms: 1.05x slower                                                         |
| async_tree_none            | 365 ms                                                           | 384 ms: 1.05x slower                                                         |
| async_tree_io              | 873 ms                                                           | 919 ms: 1.05x slower                                                         |
| aiohttp                    | 1.07 ms                                                          | 1.13 ms: 1.05x slower                                                        |
| async_tree_cpu_io_mixed_tg | 573 ms                                                           | 604 ms: 1.06x slower                                                         |
| sqlglot_normalize          | 120 ms                                                           | 127 ms: 1.06x slower                                                         |
| float                      | 80.2 ms                                                          | 84.7 ms: 1.06x slower                                                        |
| html5lib                   | 74.7 ms                                                          | 79.0 ms: 1.06x slower                                                        |
| genshi_text                | 25.9 ms                                                          | 27.5 ms: 1.06x slower                                                        |
| logging_format             | 7.11 us                                                          | 7.55 us: 1.06x slower                                                        |
| bench_thread_pool          | 908 us                                                           | 965 us: 1.06x slower                                                         |
| tornado_http               | 119 ms                                                           | 127 ms: 1.06x slower                                                         |
| django_template            | 39.0 ms                                                          | 41.5 ms: 1.07x slower                                                        |
| regex_effbot               | 3.40 ms                                                          | 3.63 ms: 1.07x slower                                                        |
| deepcopy                   | 377 us                                                           | 404 us: 1.07x slower                                                         |
| mdp                        | 2.46 sec                                                         | 2.63 sec: 1.07x slower                                                       |
| xml_etree_iterparse        | 103 ms                                                           | 110 ms: 1.07x slower                                                         |
| meteor_contest             | 128 ms                                                           | 137 ms: 1.07x slower                                                         |
| logging_simple             | 6.40 us                                                          | 6.86 us: 1.07x slower                                                        |
| gunicorn                   | 1.04 ms                                                          | 1.12 ms: 1.07x slower                                                        |
| 2to3                       | 291 ms                                                           | 314 ms: 1.08x slower                                                         |
| async_generators           | 363 ms                                                           | 392 ms: 1.08x slower                                                         |
| docutils                   | 2.98 sec                                                         | 3.24 sec: 1.09x slower                                                       |
| pylint                     | 339 ms                                                           | 370 ms: 1.09x slower                                                         |
| pycparser                  | 1.22 sec                                                         | 1.34 sec: 1.10x slower                                                       |
| sqlglot_transpile          | 1.76 ms                                                          | 1.95 ms: 1.10x slower                                                        |
| mypy2                      | 764 ms                                                           | 846 ms: 1.11x slower                                                         |
| deepcopy_memo              | 37.3 us                                                          | 41.4 us: 1.11x slower                                                        |
| dulwich_log                | 67.3 ms                                                          | 74.8 ms: 1.11x slower                                                        |
| sqlglot_parse              | 1.39 ms                                                          | 1.55 ms: 1.12x slower                                                        |
| sqlglot_optimize           | 59.5 ms                                                          | 66.5 ms: 1.12x slower                                                        |
| chameleon                  | 7.40 ms                                                          | 8.34 ms: 1.13x slower                                                        |
| sympy_integrate            | 23.2 ms                                                          | 26.2 ms: 1.13x slower                                                        |
| tomli_loads                | 2.40 sec                                                         | 2.73 sec: 1.14x slower                                                       |
| sympy_expand               | 501 ms                                                           | 573 ms: 1.14x slower                                                         |
| raytrace                   | 260 ms                                                           | 299 ms: 1.15x slower                                                         |
| sympy_sum                  | 155 ms                                                           | 178 ms: 1.15x slower                                                         |
| crypto_pyaes               | 73.6 ms                                                          | 85.5 ms: 1.16x slower                                                        |
| sympy_str                  | 295 ms                                                           | 343 ms: 1.16x slower                                                         |
| pprint_safe_repr           | 818 ms                                                           | 981 ms: 1.20x slower                                                         |
| pprint_pformat             | 1.66 sec                                                         | 2.01 sec: 1.21x slower                                                       |
| pyflate                    | 482 ms                                                           | 587 ms: 1.22x slower                                                         |
| deltablue                  | 3.37 ms                                                          | 4.12 ms: 1.22x slower                                                        |
| chaos                      | 59.6 ms                                                          | 73.3 ms: 1.23x slower                                                        |
| go                         | 165 ms                                                           | 204 ms: 1.24x slower                                                         |
| nbody                      | 87.8 ms                                                          | 110 ms: 1.25x slower                                                         |
| mako                       | 10.4 ms                                                          | 13.0 ms: 1.25x slower                                                        |
| unpickle_pure_python       | 224 us                                                           | 283 us: 1.26x slower                                                         |
| nqueens                    | 88.4 ms                                                          | 111 ms: 1.26x slower                                                         |
| scimark_fft                | 312 ms                                                           | 396 ms: 1.27x slower                                                         |
| fannkuch                   | 353 ms                                                           | 459 ms: 1.30x slower                                                         |
| scimark_sor                | 119 ms                                                           | 159 ms: 1.34x slower                                                         |
| regex_compile              | 144 ms                                                           | 194 ms: 1.35x slower                                                         |
| scimark_monte_carlo        | 65.5 ms                                                          | 90.3 ms: 1.38x slower                                                        |
| scimark_sparse_mat_mult    | 4.28 ms                                                          | 5.95 ms: 1.39x slower                                                        |
| comprehensions             | 17.0 us                                                          | 23.9 us: 1.41x slower                                                        |
| scimark_lu                 | 97.5 ms                                                          | 140 ms: 1.43x slower                                                         |
| spectral_norm              | 97.3 ms                                                          | 140 ms: 1.44x slower                                                         |
| hexiom                     | 6.35 ms                                                          | 9.39 ms: 1.48x slower                                                        |
| Geometric mean             | (ref)                                                            | 1.09x slower                                                                 |

Benchmark hidden because not significant (5): bench_mp_pool, richards, async_tree_io_tg, asyncio_tcp, json
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.05x

# Memory
- memory change: 0.99x