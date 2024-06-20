# Results vs. 3.13.0b2

- fork: python
- ref: 51aefc5bf907ddffaaf0
- machine: linux-x86_64
- commit hash: 51aefc5
- commit date: 2024-04-27
- overall geometric mean: 1.02x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.07x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 291 ms                                                           | 303 ms: 1.04x slower                                                         |
| chameleon      | 7.40 ms                                                          | 7.67 ms: 1.04x slower                                                        |
| docutils       | 2.98 sec                                                         | 3.09 sec: 1.04x slower                                                       |
| html5lib       | 74.7 ms                                                          | 73.8 ms: 1.01x faster                                                        |
| tornado_http   | 119 ms                                                           | 122 ms: 1.02x slower                                                         |
| Geometric mean | (ref)                                                            | 1.02x slower                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed    | 604 ms                                                           | 618 ms: 1.02x slower                                                         |
| async_tree_io              | 873 ms                                                           | 902 ms: 1.03x slower                                                         |
| async_tree_cpu_io_mixed_tg | 573 ms                                                           | 594 ms: 1.04x slower                                                         |
| Geometric mean             | (ref)                                                            | 1.01x slower                                                                 |

Benchmark hidden because not significant (5): async_tree_io_tg, async_tree_none_tg, async_tree_memoization_tg, async_tree_none, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 80.2 ms                                                          | 76.1 ms: 1.05x faster                                                        |
| pidigits       | 254 ms                                                           | 261 ms: 1.03x slower                                                         |
| nbody          | 87.8 ms                                                          | 97.1 ms: 1.11x slower                                                        |
| Geometric mean | (ref)                                                            | 1.03x slower                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_dna      | 249 ms                                                           | 241 ms: 1.03x faster                                                         |
| regex_v8       | 26.0 ms                                                          | 25.8 ms: 1.01x faster                                                        |
| regex_compile  | 144 ms                                                           | 143 ms: 1.01x faster                                                         |
| regex_effbot   | 3.40 ms                                                          | 3.53 ms: 1.04x slower                                                        |
| Geometric mean | (ref)                                                            | 1.00x faster                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| tomli_loads          | 2.40 sec                                                         | 2.11 sec: 1.14x faster                                                       |
| unpickle             | 15.7 us                                                          | 14.9 us: 1.05x faster                                                        |
| xml_etree_iterparse  | 103 ms                                                           | 100 ms: 1.02x faster                                                         |
| xml_etree_process    | 59.7 ms                                                          | 58.6 ms: 1.02x faster                                                        |
| json_loads           | 25.0 us                                                          | 24.6 us: 1.02x faster                                                        |
| json_dumps           | 10.8 ms                                                          | 10.6 ms: 1.02x faster                                                        |
| xml_etree_generate   | 85.7 ms                                                          | 84.6 ms: 1.01x faster                                                        |
| unpickle_pure_python | 224 us                                                           | 221 us: 1.01x faster                                                         |
| pickle               | 10.6 us                                                          | 10.7 us: 1.01x slower                                                        |
| unpickle_list        | 4.70 us                                                          | 4.75 us: 1.01x slower                                                        |
| xml_etree_parse      | 144 ms                                                           | 145 ms: 1.01x slower                                                         |
| pickle_dict          | 32.8 us                                                          | 33.2 us: 1.01x slower                                                        |
| pickle_pure_python   | 307 us                                                           | 320 us: 1.04x slower                                                         |
| Geometric mean       | (ref)                                                            | 1.01x faster                                                                 |

Benchmark hidden because not significant (1): pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|------------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 13.2 ms                                                          | 13.5 ms: 1.02x slower                                                        |
| python_startup_no_site | 8.85 ms                                                          | 9.41 ms: 1.06x slower                                                        |
| Geometric mean         | (ref)                                                            | 1.04x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|-----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 10.4 ms                                                          | 9.86 ms: 1.05x faster                                                        |
| django_template | 39.0 ms                                                          | 40.3 ms: 1.03x slower                                                        |
| genshi_xml      | 58.1 ms                                                          | 62.8 ms: 1.08x slower                                                        |
| genshi_text     | 25.9 ms                                                          | 29.1 ms: 1.12x slower                                                        |
| Geometric mean  | (ref)                                                            | 1.05x slower                                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| richards_super             | 61.2 ms                                                          | 52.2 ms: 1.17x faster                                                        |
| richards                   | 53.4 ms                                                          | 46.2 ms: 1.16x faster                                                        |
| tomli_loads                | 2.40 sec                                                         | 2.11 sec: 1.14x faster                                                       |
| coverage                   | 83.5 ms                                                          | 76.6 ms: 1.09x faster                                                        |
| spectral_norm              | 97.3 ms                                                          | 91.3 ms: 1.07x faster                                                        |
| create_gc_cycles           | 2.00 ms                                                          | 1.88 ms: 1.07x faster                                                        |
| gc_traversal               | 4.69 ms                                                          | 4.42 ms: 1.06x faster                                                        |
| telco                      | 8.40 ms                                                          | 7.97 ms: 1.05x faster                                                        |
| unpickle                   | 15.7 us                                                          | 14.9 us: 1.05x faster                                                        |
| float                      | 80.2 ms                                                          | 76.1 ms: 1.05x faster                                                        |
| mako                       | 10.4 ms                                                          | 9.86 ms: 1.05x faster                                                        |
| scimark_sparse_mat_mult    | 4.28 ms                                                          | 4.07 ms: 1.05x faster                                                        |
| sqlite_synth               | 2.80 us                                                          | 2.66 us: 1.05x faster                                                        |
| regex_dna                  | 249 ms                                                           | 241 ms: 1.03x faster                                                         |
| xml_etree_iterparse        | 103 ms                                                           | 100 ms: 1.02x faster                                                         |
| coroutines                 | 22.0 ms                                                          | 21.6 ms: 1.02x faster                                                        |
| xml_etree_process          | 59.7 ms                                                          | 58.6 ms: 1.02x faster                                                        |
| json_loads                 | 25.0 us                                                          | 24.6 us: 1.02x faster                                                        |
| json_dumps                 | 10.8 ms                                                          | 10.6 ms: 1.02x faster                                                        |
| xml_etree_generate         | 85.7 ms                                                          | 84.6 ms: 1.01x faster                                                        |
| unpickle_pure_python       | 224 us                                                           | 221 us: 1.01x faster                                                         |
| html5lib                   | 74.7 ms                                                          | 73.8 ms: 1.01x faster                                                        |
| asyncio_websockets         | 395 ms                                                           | 390 ms: 1.01x faster                                                         |
| asyncio_tcp                | 378 ms                                                           | 374 ms: 1.01x faster                                                         |
| regex_v8                   | 26.0 ms                                                          | 25.8 ms: 1.01x faster                                                        |
| regex_compile              | 144 ms                                                           | 143 ms: 1.01x faster                                                         |
| pyflate                    | 482 ms                                                           | 478 ms: 1.01x faster                                                         |
| dulwich_log                | 67.3 ms                                                          | 66.8 ms: 1.01x faster                                                        |
| logging_format             | 7.11 us                                                          | 7.17 us: 1.01x slower                                                        |
| pickle                     | 10.6 us                                                          | 10.7 us: 1.01x slower                                                        |
| deepcopy_memo              | 37.3 us                                                          | 37.6 us: 1.01x slower                                                        |
| deepcopy_reduce            | 3.39 us                                                          | 3.42 us: 1.01x slower                                                        |
| unpickle_list              | 4.70 us                                                          | 4.75 us: 1.01x slower                                                        |
| logging_silent             | 96.3 ns                                                          | 97.2 ns: 1.01x slower                                                        |
| pycparser                  | 1.22 sec                                                         | 1.24 sec: 1.01x slower                                                       |
| xml_etree_parse            | 144 ms                                                           | 145 ms: 1.01x slower                                                         |
| pickle_dict                | 32.8 us                                                          | 33.2 us: 1.01x slower                                                        |
| thrift                     | 880 us                                                           | 892 us: 1.01x slower                                                         |
| python_startup             | 13.2 ms                                                          | 13.5 ms: 1.02x slower                                                        |
| tornado_http               | 119 ms                                                           | 122 ms: 1.02x slower                                                         |
| async_tree_cpu_io_mixed    | 604 ms                                                           | 618 ms: 1.02x slower                                                         |
| pathlib                    | 17.1 ms                                                          | 17.5 ms: 1.02x slower                                                        |
| dask                       | 391 ms                                                           | 400 ms: 1.02x slower                                                         |
| logging_simple             | 6.40 us                                                          | 6.57 us: 1.03x slower                                                        |
| sqlglot_parse              | 1.39 ms                                                          | 1.43 ms: 1.03x slower                                                        |
| pidigits                   | 254 ms                                                           | 261 ms: 1.03x slower                                                         |
| generators                 | 33.5 ms                                                          | 34.6 ms: 1.03x slower                                                        |
| sympy_expand               | 501 ms                                                           | 517 ms: 1.03x slower                                                         |
| async_tree_io              | 873 ms                                                           | 902 ms: 1.03x slower                                                         |
| django_template            | 39.0 ms                                                          | 40.3 ms: 1.03x slower                                                        |
| docutils                   | 2.98 sec                                                         | 3.09 sec: 1.04x slower                                                       |
| go                         | 165 ms                                                           | 171 ms: 1.04x slower                                                         |
| async_tree_cpu_io_mixed_tg | 573 ms                                                           | 594 ms: 1.04x slower                                                         |
| chameleon                  | 7.40 ms                                                          | 7.67 ms: 1.04x slower                                                        |
| regex_effbot               | 3.40 ms                                                          | 3.53 ms: 1.04x slower                                                        |
| 2to3                       | 291 ms                                                           | 303 ms: 1.04x slower                                                         |
| sqlglot_normalize          | 120 ms                                                           | 125 ms: 1.04x slower                                                         |
| pickle_pure_python         | 307 us                                                           | 320 us: 1.04x slower                                                         |
| sqlglot_transpile          | 1.76 ms                                                          | 1.84 ms: 1.04x slower                                                        |
| pprint_safe_repr           | 818 ms                                                           | 856 ms: 1.05x slower                                                         |
| meteor_contest             | 128 ms                                                           | 134 ms: 1.05x slower                                                         |
| mdp                        | 2.46 sec                                                         | 2.58 sec: 1.05x slower                                                       |
| deepcopy                   | 377 us                                                           | 396 us: 1.05x slower                                                         |
| pprint_pformat             | 1.66 sec                                                         | 1.74 sec: 1.05x slower                                                       |
| async_generators           | 363 ms                                                           | 381 ms: 1.05x slower                                                         |
| sympy_str                  | 295 ms                                                           | 311 ms: 1.05x slower                                                         |
| crypto_pyaes               | 73.6 ms                                                          | 77.7 ms: 1.06x slower                                                        |
| sympy_sum                  | 155 ms                                                           | 164 ms: 1.06x slower                                                         |
| aiohttp                    | 1.07 ms                                                          | 1.13 ms: 1.06x slower                                                        |
| bench_thread_pool          | 908 us                                                           | 964 us: 1.06x slower                                                         |
| python_startup_no_site     | 8.85 ms                                                          | 9.41 ms: 1.06x slower                                                        |
| raytrace                   | 260 ms                                                           | 277 ms: 1.07x slower                                                         |
| gunicorn                   | 1.04 ms                                                          | 1.12 ms: 1.07x slower                                                        |
| scimark_monte_carlo        | 65.5 ms                                                          | 70.3 ms: 1.07x slower                                                        |
| sqlglot_optimize           | 59.5 ms                                                          | 64.1 ms: 1.08x slower                                                        |
| typing_runtime_protocols   | 171 us                                                           | 184 us: 1.08x slower                                                         |
| genshi_xml                 | 58.1 ms                                                          | 62.8 ms: 1.08x slower                                                        |
| pylint                     | 339 ms                                                           | 370 ms: 1.09x slower                                                         |
| fannkuch                   | 353 ms                                                           | 385 ms: 1.09x slower                                                         |
| sympy_integrate            | 23.2 ms                                                          | 25.5 ms: 1.10x slower                                                        |
| chaos                      | 59.6 ms                                                          | 65.8 ms: 1.10x slower                                                        |
| nbody                      | 87.8 ms                                                          | 97.1 ms: 1.11x slower                                                        |
| mypy2                      | 764 ms                                                           | 846 ms: 1.11x slower                                                         |
| genshi_text                | 25.9 ms                                                          | 29.1 ms: 1.12x slower                                                        |
| deltablue                  | 3.37 ms                                                          | 3.80 ms: 1.13x slower                                                        |
| comprehensions             | 17.0 us                                                          | 19.4 us: 1.15x slower                                                        |
| hexiom                     | 6.35 ms                                                          | 7.30 ms: 1.15x slower                                                        |
| nqueens                    | 88.4 ms                                                          | 102 ms: 1.15x slower                                                         |
| scimark_lu                 | 97.5 ms                                                          | 117 ms: 1.20x slower                                                         |
| scimark_sor                | 119 ms                                                           | 154 ms: 1.30x slower                                                         |
| Geometric mean             | (ref)                                                            | 1.02x slower                                                                 |

Benchmark hidden because not significant (10): bench_mp_pool, async_tree_io_tg, async_tree_none_tg, json, scimark_fft, asyncio_tcp_ssl, pickle_list, async_tree_memoization_tg, async_tree_none, async_tree_memoization
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.07x