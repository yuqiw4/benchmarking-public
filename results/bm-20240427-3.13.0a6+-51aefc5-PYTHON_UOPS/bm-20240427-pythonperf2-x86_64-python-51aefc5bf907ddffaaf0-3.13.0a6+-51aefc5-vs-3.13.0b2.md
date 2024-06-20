# Results vs. 3.13.0b2

- fork: python
- ref: 51aefc5bf907ddffaaf0
- machine: linux-x86_64
- commit hash: 51aefc5
- commit date: 2024-04-27
- overall geometric mean: 1.12x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x slower
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 291 ms                                                           | 326 ms: 1.12x slower                                                         |
| chameleon      | 7.40 ms                                                          | 7.94 ms: 1.07x slower                                                        |
| docutils       | 2.98 sec                                                         | 3.28 sec: 1.10x slower                                                       |
| html5lib       | 74.7 ms                                                          | 80.4 ms: 1.08x slower                                                        |
| tornado_http   | 119 ms                                                           | 126 ms: 1.05x slower                                                         |
| Geometric mean | (ref)                                                            | 1.08x slower                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none_tg         | 340 ms                                                           | 349 ms: 1.02x slower                                                         |
| async_tree_memoization_tg  | 421 ms                                                           | 437 ms: 1.04x slower                                                         |
| async_tree_cpu_io_mixed    | 604 ms                                                           | 634 ms: 1.05x slower                                                         |
| async_tree_cpu_io_mixed_tg | 573 ms                                                           | 603 ms: 1.05x slower                                                         |
| async_tree_memoization     | 460 ms                                                           | 485 ms: 1.06x slower                                                         |
| async_tree_none            | 365 ms                                                           | 386 ms: 1.06x slower                                                         |
| async_tree_io              | 873 ms                                                           | 927 ms: 1.06x slower                                                         |
| Geometric mean             | (ref)                                                            | 1.04x slower                                                                 |

Benchmark hidden because not significant (1): async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pidigits       | 254 ms                                                           | 264 ms: 1.04x slower                                                         |
| float          | 80.2 ms                                                          | 92.8 ms: 1.16x slower                                                        |
| nbody          | 87.8 ms                                                          | 119 ms: 1.35x slower                                                         |
| Geometric mean | (ref)                                                            | 1.18x slower                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_v8       | 26.0 ms                                                          | 25.4 ms: 1.02x faster                                                        |
| regex_dna      | 249 ms                                                           | 245 ms: 1.02x faster                                                         |
| regex_effbot   | 3.40 ms                                                          | 3.62 ms: 1.07x slower                                                        |
| regex_compile  | 144 ms                                                           | 199 ms: 1.38x slower                                                         |
| Geometric mean | (ref)                                                            | 1.09x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| unpickle             | 15.7 us                                                          | 15.3 us: 1.02x faster                                                        |
| json_loads           | 25.0 us                                                          | 24.6 us: 1.02x faster                                                        |
| pickle_list          | 4.44 us                                                          | 4.37 us: 1.02x faster                                                        |
| unpickle_list        | 4.70 us                                                          | 4.62 us: 1.02x faster                                                        |
| json_dumps           | 10.8 ms                                                          | 10.8 ms: 1.01x slower                                                        |
| xml_etree_parse      | 144 ms                                                           | 146 ms: 1.02x slower                                                         |
| pickle_pure_python   | 307 us                                                           | 323 us: 1.05x slower                                                         |
| xml_etree_generate   | 85.7 ms                                                          | 91.6 ms: 1.07x slower                                                        |
| xml_etree_process    | 59.7 ms                                                          | 64.2 ms: 1.08x slower                                                        |
| xml_etree_iterparse  | 103 ms                                                           | 112 ms: 1.09x slower                                                         |
| tomli_loads          | 2.40 sec                                                         | 2.86 sec: 1.19x slower                                                       |
| unpickle_pure_python | 224 us                                                           | 301 us: 1.34x slower                                                         |
| Geometric mean       | (ref)                                                            | 1.05x slower                                                                 |

Benchmark hidden because not significant (2): pickle, pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|------------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 13.2 ms                                                          | 13.0 ms: 1.02x faster                                                        |
| python_startup_no_site | 8.85 ms                                                          | 8.91 ms: 1.01x slower                                                        |
| Geometric mean         | (ref)                                                            | 1.01x faster                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|-----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| django_template | 39.0 ms                                                          | 43.0 ms: 1.10x slower                                                        |
| genshi_xml      | 58.1 ms                                                          | 65.8 ms: 1.13x slower                                                        |
| genshi_text     | 25.9 ms                                                          | 31.8 ms: 1.23x slower                                                        |
| mako            | 10.4 ms                                                          | 14.3 ms: 1.38x slower                                                        |
| Geometric mean  | (ref)                                                            | 1.21x slower                                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| coverage                   | 83.5 ms                                                          | 80.0 ms: 1.04x faster                                                        |
| unpickle                   | 15.7 us                                                          | 15.3 us: 1.02x faster                                                        |
| regex_v8                   | 26.0 ms                                                          | 25.4 ms: 1.02x faster                                                        |
| json_loads                 | 25.0 us                                                          | 24.6 us: 1.02x faster                                                        |
| python_startup             | 13.2 ms                                                          | 13.0 ms: 1.02x faster                                                        |
| pickle_list                | 4.44 us                                                          | 4.37 us: 1.02x faster                                                        |
| unpickle_list              | 4.70 us                                                          | 4.62 us: 1.02x faster                                                        |
| regex_dna                  | 249 ms                                                           | 245 ms: 1.02x faster                                                         |
| asyncio_websockets         | 395 ms                                                           | 390 ms: 1.01x faster                                                         |
| coroutines                 | 22.0 ms                                                          | 22.0 ms: 1.00x slower                                                        |
| python_startup_no_site     | 8.85 ms                                                          | 8.91 ms: 1.01x slower                                                        |
| json_dumps                 | 10.8 ms                                                          | 10.8 ms: 1.01x slower                                                        |
| generators                 | 33.5 ms                                                          | 33.8 ms: 1.01x slower                                                        |
| asyncio_tcp_ssl            | 1.58 sec                                                         | 1.60 sec: 1.01x slower                                                       |
| thrift                     | 880 us                                                           | 895 us: 1.02x slower                                                         |
| xml_etree_parse            | 144 ms                                                           | 146 ms: 1.02x slower                                                         |
| telco                      | 8.40 ms                                                          | 8.59 ms: 1.02x slower                                                        |
| richards_super             | 61.2 ms                                                          | 62.7 ms: 1.02x slower                                                        |
| async_tree_none_tg         | 340 ms                                                           | 349 ms: 1.02x slower                                                         |
| asyncio_tcp                | 378 ms                                                           | 387 ms: 1.02x slower                                                         |
| sqlite_synth               | 2.80 us                                                          | 2.87 us: 1.03x slower                                                        |
| json                       | 5.35 ms                                                          | 5.50 ms: 1.03x slower                                                        |
| create_gc_cycles           | 2.00 ms                                                          | 2.07 ms: 1.03x slower                                                        |
| logging_format             | 7.11 us                                                          | 7.36 us: 1.03x slower                                                        |
| async_tree_memoization_tg  | 421 ms                                                           | 437 ms: 1.04x slower                                                         |
| pidigits                   | 254 ms                                                           | 264 ms: 1.04x slower                                                         |
| richards                   | 53.4 ms                                                          | 55.6 ms: 1.04x slower                                                        |
| logging_silent             | 96.3 ns                                                          | 100 ns: 1.04x slower                                                         |
| gc_traversal               | 4.69 ms                                                          | 4.91 ms: 1.05x slower                                                        |
| async_tree_cpu_io_mixed    | 604 ms                                                           | 634 ms: 1.05x slower                                                         |
| pickle_pure_python         | 307 us                                                           | 323 us: 1.05x slower                                                         |
| async_tree_cpu_io_mixed_tg | 573 ms                                                           | 603 ms: 1.05x slower                                                         |
| tornado_http               | 119 ms                                                           | 126 ms: 1.05x slower                                                         |
| async_tree_memoization     | 460 ms                                                           | 485 ms: 1.06x slower                                                         |
| async_tree_none            | 365 ms                                                           | 386 ms: 1.06x slower                                                         |
| deepcopy_reduce            | 3.39 us                                                          | 3.59 us: 1.06x slower                                                        |
| async_tree_io              | 873 ms                                                           | 927 ms: 1.06x slower                                                         |
| logging_simple             | 6.40 us                                                          | 6.79 us: 1.06x slower                                                        |
| regex_effbot               | 3.40 ms                                                          | 3.62 ms: 1.07x slower                                                        |
| pathlib                    | 17.1 ms                                                          | 18.3 ms: 1.07x slower                                                        |
| dask                       | 391 ms                                                           | 417 ms: 1.07x slower                                                         |
| xml_etree_generate         | 85.7 ms                                                          | 91.6 ms: 1.07x slower                                                        |
| chameleon                  | 7.40 ms                                                          | 7.94 ms: 1.07x slower                                                        |
| aiohttp                    | 1.07 ms                                                          | 1.15 ms: 1.07x slower                                                        |
| xml_etree_process          | 59.7 ms                                                          | 64.2 ms: 1.08x slower                                                        |
| html5lib                   | 74.7 ms                                                          | 80.4 ms: 1.08x slower                                                        |
| bench_thread_pool          | 908 us                                                           | 980 us: 1.08x slower                                                         |
| gunicorn                   | 1.04 ms                                                          | 1.13 ms: 1.08x slower                                                        |
| async_generators           | 363 ms                                                           | 393 ms: 1.08x slower                                                         |
| deepcopy                   | 377 us                                                           | 410 us: 1.09x slower                                                         |
| xml_etree_iterparse        | 103 ms                                                           | 112 ms: 1.09x slower                                                         |
| docutils                   | 2.98 sec                                                         | 3.28 sec: 1.10x slower                                                       |
| pycparser                  | 1.22 sec                                                         | 1.34 sec: 1.10x slower                                                       |
| django_template            | 39.0 ms                                                          | 43.0 ms: 1.10x slower                                                        |
| sqlglot_normalize          | 120 ms                                                           | 133 ms: 1.10x slower                                                         |
| sqlglot_transpile          | 1.76 ms                                                          | 1.95 ms: 1.11x slower                                                        |
| sqlglot_parse              | 1.39 ms                                                          | 1.55 ms: 1.11x slower                                                        |
| pylint                     | 339 ms                                                           | 378 ms: 1.12x slower                                                         |
| mdp                        | 2.46 sec                                                         | 2.75 sec: 1.12x slower                                                       |
| 2to3                       | 291 ms                                                           | 326 ms: 1.12x slower                                                         |
| meteor_contest             | 128 ms                                                           | 144 ms: 1.12x slower                                                         |
| genshi_xml                 | 58.1 ms                                                          | 65.8 ms: 1.13x slower                                                        |
| mypy2                      | 764 ms                                                           | 868 ms: 1.14x slower                                                         |
| dulwich_log                | 67.3 ms                                                          | 76.8 ms: 1.14x slower                                                        |
| sympy_integrate            | 23.2 ms                                                          | 26.5 ms: 1.15x slower                                                        |
| deepcopy_memo              | 37.3 us                                                          | 42.7 us: 1.15x slower                                                        |
| sympy_sum                  | 155 ms                                                           | 178 ms: 1.15x slower                                                         |
| sympy_expand               | 501 ms                                                           | 577 ms: 1.15x slower                                                         |
| typing_runtime_protocols   | 171 us                                                           | 197 us: 1.15x slower                                                         |
| sqlglot_optimize           | 59.5 ms                                                          | 68.8 ms: 1.16x slower                                                        |
| float                      | 80.2 ms                                                          | 92.8 ms: 1.16x slower                                                        |
| raytrace                   | 260 ms                                                           | 306 ms: 1.17x slower                                                         |
| sympy_str                  | 295 ms                                                           | 346 ms: 1.17x slower                                                         |
| tomli_loads                | 2.40 sec                                                         | 2.86 sec: 1.19x slower                                                       |
| genshi_text                | 25.9 ms                                                          | 31.8 ms: 1.23x slower                                                        |
| crypto_pyaes               | 73.6 ms                                                          | 91.3 ms: 1.24x slower                                                        |
| go                         | 165 ms                                                           | 207 ms: 1.26x slower                                                         |
| pprint_safe_repr           | 818 ms                                                           | 1.04 sec: 1.27x slower                                                       |
| pprint_pformat             | 1.66 sec                                                         | 2.11 sec: 1.27x slower                                                       |
| pyflate                    | 482 ms                                                           | 621 ms: 1.29x slower                                                         |
| deltablue                  | 3.37 ms                                                          | 4.36 ms: 1.29x slower                                                        |
| chaos                      | 59.6 ms                                                          | 77.3 ms: 1.30x slower                                                        |
| unpickle_pure_python       | 224 us                                                           | 301 us: 1.34x slower                                                         |
| nqueens                    | 88.4 ms                                                          | 119 ms: 1.34x slower                                                         |
| nbody                      | 87.8 ms                                                          | 119 ms: 1.35x slower                                                         |
| scimark_sor                | 119 ms                                                           | 161 ms: 1.36x slower                                                         |
| scimark_fft                | 312 ms                                                           | 425 ms: 1.36x slower                                                         |
| fannkuch                   | 353 ms                                                           | 485 ms: 1.37x slower                                                         |
| regex_compile              | 144 ms                                                           | 199 ms: 1.38x slower                                                         |
| mako                       | 10.4 ms                                                          | 14.3 ms: 1.38x slower                                                        |
| scimark_lu                 | 97.5 ms                                                          | 141 ms: 1.45x slower                                                         |
| scimark_sparse_mat_mult    | 4.28 ms                                                          | 6.28 ms: 1.47x slower                                                        |
| spectral_norm              | 97.3 ms                                                          | 144 ms: 1.48x slower                                                         |
| scimark_monte_carlo        | 65.5 ms                                                          | 97.9 ms: 1.50x slower                                                        |
| comprehensions             | 17.0 us                                                          | 27.6 us: 1.63x slower                                                        |
| hexiom                     | 6.35 ms                                                          | 10.6 ms: 1.66x slower                                                        |
| Geometric mean             | (ref)                                                            | 1.12x slower                                                                 |

Benchmark hidden because not significant (4): bench_mp_pool, pickle, pickle_dict, async_tree_io_tg
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.09x
- 99% likely to have a slowdown of 1.08x

# Memory
- memory change: 0.99x