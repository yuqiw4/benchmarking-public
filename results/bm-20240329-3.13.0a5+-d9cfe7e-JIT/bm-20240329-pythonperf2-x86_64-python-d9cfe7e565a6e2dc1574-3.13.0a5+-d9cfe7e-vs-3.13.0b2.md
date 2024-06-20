# Results vs. 3.13.0b2

- fork: python
- ref: d9cfe7e565a6e2dc1574
- machine: linux-x86_64
- commit hash: d9cfe7e
- commit date: 2024-03-29
- overall geometric mean: 1.03x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.05x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e |
|----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 291 ms                                                           | 300 ms: 1.03x slower                                                         |
| chameleon      | 7.40 ms                                                          | 7.43 ms: 1.00x slower                                                        |
| docutils       | 2.98 sec                                                         | 3.07 sec: 1.03x slower                                                       |
| html5lib       | 74.7 ms                                                          | 73.4 ms: 1.02x faster                                                        |
| tornado_http   | 119 ms                                                           | 124 ms: 1.04x slower                                                         |
| Geometric mean | (ref)                                                            | 1.02x slower                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e |
|----------------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_io_tg           | 900 ms                                                           | 880 ms: 1.02x faster                                                         |
| async_tree_none            | 365 ms                                                           | 377 ms: 1.03x slower                                                         |
| async_tree_io              | 873 ms                                                           | 907 ms: 1.04x slower                                                         |
| async_tree_cpu_io_mixed_tg | 573 ms                                                           | 596 ms: 1.04x slower                                                         |
| Geometric mean             | (ref)                                                            | 1.01x slower                                                                 |

Benchmark hidden because not significant (4): async_tree_memoization, async_tree_cpu_io_mixed, async_tree_none_tg, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e |
|----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 80.2 ms                                                          | 79.5 ms: 1.01x faster                                                        |
| pidigits       | 254 ms                                                           | 261 ms: 1.03x slower                                                         |
| nbody          | 87.8 ms                                                          | 98.3 ms: 1.12x slower                                                        |
| Geometric mean | (ref)                                                            | 1.05x slower                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e |
|----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_dna      | 249 ms                                                           | 244 ms: 1.02x faster                                                         |
| regex_v8       | 26.0 ms                                                          | 26.1 ms: 1.00x slower                                                        |
| regex_effbot   | 3.40 ms                                                          | 3.42 ms: 1.01x slower                                                        |
| regex_compile  | 144 ms                                                           | 148 ms: 1.03x slower                                                         |
| Geometric mean | (ref)                                                            | 1.00x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e |
|----------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| tomli_loads          | 2.40 sec                                                         | 2.16 sec: 1.11x faster                                                       |
| json_dumps           | 10.8 ms                                                          | 10.5 ms: 1.03x faster                                                        |
| xml_etree_process    | 59.7 ms                                                          | 58.5 ms: 1.02x faster                                                        |
| xml_etree_generate   | 85.7 ms                                                          | 83.9 ms: 1.02x faster                                                        |
| unpickle_list        | 4.70 us                                                          | 4.62 us: 1.02x faster                                                        |
| pickle_list          | 4.44 us                                                          | 4.38 us: 1.01x faster                                                        |
| unpickle             | 15.7 us                                                          | 15.5 us: 1.01x faster                                                        |
| pickle_dict          | 32.8 us                                                          | 33.0 us: 1.01x slower                                                        |
| xml_etree_iterparse  | 103 ms                                                           | 104 ms: 1.01x slower                                                         |
| pickle               | 10.6 us                                                          | 10.9 us: 1.02x slower                                                        |
| pickle_pure_python   | 307 us                                                           | 316 us: 1.03x slower                                                         |
| json_loads           | 25.0 us                                                          | 25.8 us: 1.03x slower                                                        |
| unpickle_pure_python | 224 us                                                           | 235 us: 1.05x slower                                                         |
| Geometric mean       | (ref)                                                            | 1.01x faster                                                                 |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e |
|------------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 13.2 ms                                                          | 13.5 ms: 1.02x slower                                                        |
| python_startup_no_site | 8.85 ms                                                          | 11.8 ms: 1.33x slower                                                        |
| Geometric mean         | (ref)                                                            | 1.17x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e |
|-----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 10.4 ms                                                          | 10.0 ms: 1.04x faster                                                        |
| genshi_xml      | 58.1 ms                                                          | 59.1 ms: 1.02x slower                                                        |
| genshi_text     | 25.9 ms                                                          | 26.8 ms: 1.03x slower                                                        |
| django_template | 39.0 ms                                                          | 41.2 ms: 1.06x slower                                                        |
| Geometric mean  | (ref)                                                            | 1.02x slower                                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e |
|----------------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 171 us                                                           | 122 us: 1.40x faster                                                         |
| create_gc_cycles           | 2.00 ms                                                          | 1.79 ms: 1.12x faster                                                        |
| tomli_loads                | 2.40 sec                                                         | 2.16 sec: 1.11x faster                                                       |
| gc_traversal               | 4.69 ms                                                          | 4.38 ms: 1.07x faster                                                        |
| richards_super             | 61.2 ms                                                          | 58.0 ms: 1.06x faster                                                        |
| telco                      | 8.40 ms                                                          | 7.97 ms: 1.05x faster                                                        |
| spectral_norm              | 97.3 ms                                                          | 93.2 ms: 1.04x faster                                                        |
| mako                       | 10.4 ms                                                          | 10.0 ms: 1.04x faster                                                        |
| scimark_sparse_mat_mult    | 4.28 ms                                                          | 4.15 ms: 1.03x faster                                                        |
| sqlite_synth               | 2.80 us                                                          | 2.71 us: 1.03x faster                                                        |
| richards                   | 53.4 ms                                                          | 51.9 ms: 1.03x faster                                                        |
| json_dumps                 | 10.8 ms                                                          | 10.5 ms: 1.03x faster                                                        |
| regex_dna                  | 249 ms                                                           | 244 ms: 1.02x faster                                                         |
| async_tree_io_tg           | 900 ms                                                           | 880 ms: 1.02x faster                                                         |
| xml_etree_process          | 59.7 ms                                                          | 58.5 ms: 1.02x faster                                                        |
| xml_etree_generate         | 85.7 ms                                                          | 83.9 ms: 1.02x faster                                                        |
| asyncio_websockets         | 395 ms                                                           | 387 ms: 1.02x faster                                                         |
| unpickle_list              | 4.70 us                                                          | 4.62 us: 1.02x faster                                                        |
| html5lib                   | 74.7 ms                                                          | 73.4 ms: 1.02x faster                                                        |
| asyncio_tcp                | 378 ms                                                           | 372 ms: 1.02x faster                                                         |
| pickle_list                | 4.44 us                                                          | 4.38 us: 1.01x faster                                                        |
| unpickle                   | 15.7 us                                                          | 15.5 us: 1.01x faster                                                        |
| float                      | 80.2 ms                                                          | 79.5 ms: 1.01x faster                                                        |
| coverage                   | 83.5 ms                                                          | 83.0 ms: 1.01x faster                                                        |
| asyncio_tcp_ssl            | 1.58 sec                                                         | 1.58 sec: 1.00x faster                                                       |
| regex_v8                   | 26.0 ms                                                          | 26.1 ms: 1.00x slower                                                        |
| chameleon                  | 7.40 ms                                                          | 7.43 ms: 1.00x slower                                                        |
| pickle_dict                | 32.8 us                                                          | 33.0 us: 1.01x slower                                                        |
| regex_effbot               | 3.40 ms                                                          | 3.42 ms: 1.01x slower                                                        |
| logging_silent             | 96.3 ns                                                          | 97.2 ns: 1.01x slower                                                        |
| json                       | 5.35 ms                                                          | 5.41 ms: 1.01x slower                                                        |
| xml_etree_iterparse        | 103 ms                                                           | 104 ms: 1.01x slower                                                         |
| genshi_xml                 | 58.1 ms                                                          | 59.1 ms: 1.02x slower                                                        |
| meteor_contest             | 128 ms                                                           | 131 ms: 1.02x slower                                                         |
| python_startup             | 13.2 ms                                                          | 13.5 ms: 1.02x slower                                                        |
| pickle                     | 10.6 us                                                          | 10.9 us: 1.02x slower                                                        |
| coroutines                 | 22.0 ms                                                          | 22.5 ms: 1.02x slower                                                        |
| sympy_expand               | 501 ms                                                           | 512 ms: 1.02x slower                                                         |
| pickle_pure_python         | 307 us                                                           | 316 us: 1.03x slower                                                         |
| deepcopy_memo              | 37.3 us                                                          | 38.3 us: 1.03x slower                                                        |
| regex_compile              | 144 ms                                                           | 148 ms: 1.03x slower                                                         |
| json_loads                 | 25.0 us                                                          | 25.8 us: 1.03x slower                                                        |
| pprint_safe_repr           | 818 ms                                                           | 841 ms: 1.03x slower                                                         |
| 2to3                       | 291 ms                                                           | 300 ms: 1.03x slower                                                         |
| deepcopy                   | 377 us                                                           | 388 us: 1.03x slower                                                         |
| pidigits                   | 254 ms                                                           | 261 ms: 1.03x slower                                                         |
| sympy_str                  | 295 ms                                                           | 304 ms: 1.03x slower                                                         |
| docutils                   | 2.98 sec                                                         | 3.07 sec: 1.03x slower                                                       |
| logging_format             | 7.11 us                                                          | 7.33 us: 1.03x slower                                                        |
| async_tree_none            | 365 ms                                                           | 377 ms: 1.03x slower                                                         |
| generators                 | 33.5 ms                                                          | 34.6 ms: 1.03x slower                                                        |
| genshi_text                | 25.9 ms                                                          | 26.8 ms: 1.03x slower                                                        |
| sqlglot_normalize          | 120 ms                                                           | 125 ms: 1.04x slower                                                         |
| dulwich_log                | 67.3 ms                                                          | 69.8 ms: 1.04x slower                                                        |
| pprint_pformat             | 1.66 sec                                                         | 1.72 sec: 1.04x slower                                                       |
| async_tree_io              | 873 ms                                                           | 907 ms: 1.04x slower                                                         |
| sqlglot_parse              | 1.39 ms                                                          | 1.45 ms: 1.04x slower                                                        |
| async_tree_cpu_io_mixed_tg | 573 ms                                                           | 596 ms: 1.04x slower                                                         |
| tornado_http               | 119 ms                                                           | 124 ms: 1.04x slower                                                         |
| dask                       | 391 ms                                                           | 408 ms: 1.05x slower                                                         |
| sqlglot_transpile          | 1.76 ms                                                          | 1.84 ms: 1.05x slower                                                        |
| aiohttp                    | 1.07 ms                                                          | 1.12 ms: 1.05x slower                                                        |
| unpickle_pure_python       | 224 us                                                           | 235 us: 1.05x slower                                                         |
| sympy_sum                  | 155 ms                                                           | 163 ms: 1.05x slower                                                         |
| gunicorn                   | 1.04 ms                                                          | 1.10 ms: 1.05x slower                                                        |
| crypto_pyaes               | 73.6 ms                                                          | 77.5 ms: 1.05x slower                                                        |
| pycparser                  | 1.22 sec                                                         | 1.29 sec: 1.06x slower                                                       |
| django_template            | 39.0 ms                                                          | 41.2 ms: 1.06x slower                                                        |
| logging_simple             | 6.40 us                                                          | 6.80 us: 1.06x slower                                                        |
| mdp                        | 2.46 sec                                                         | 2.62 sec: 1.06x slower                                                       |
| sqlglot_optimize           | 59.5 ms                                                          | 63.6 ms: 1.07x slower                                                        |
| pylint                     | 339 ms                                                           | 364 ms: 1.07x slower                                                         |
| fannkuch                   | 353 ms                                                           | 379 ms: 1.07x slower                                                         |
| async_generators           | 363 ms                                                           | 390 ms: 1.08x slower                                                         |
| pyflate                    | 482 ms                                                           | 519 ms: 1.08x slower                                                         |
| mypy2                      | 764 ms                                                           | 833 ms: 1.09x slower                                                         |
| sympy_integrate            | 23.2 ms                                                          | 25.3 ms: 1.09x slower                                                        |
| go                         | 165 ms                                                           | 180 ms: 1.09x slower                                                         |
| scimark_monte_carlo        | 65.5 ms                                                          | 72.9 ms: 1.11x slower                                                        |
| nbody                      | 87.8 ms                                                          | 98.3 ms: 1.12x slower                                                        |
| chaos                      | 59.6 ms                                                          | 67.5 ms: 1.13x slower                                                        |
| pathlib                    | 17.1 ms                                                          | 19.4 ms: 1.14x slower                                                        |
| deltablue                  | 3.37 ms                                                          | 3.85 ms: 1.14x slower                                                        |
| comprehensions             | 17.0 us                                                          | 19.7 us: 1.16x slower                                                        |
| nqueens                    | 88.4 ms                                                          | 103 ms: 1.17x slower                                                         |
| raytrace                   | 260 ms                                                           | 308 ms: 1.18x slower                                                         |
| hexiom                     | 6.35 ms                                                          | 7.57 ms: 1.19x slower                                                        |
| scimark_lu                 | 97.5 ms                                                          | 120 ms: 1.23x slower                                                         |
| bench_thread_pool          | 908 us                                                           | 1.12 ms: 1.24x slower                                                        |
| scimark_sor                | 119 ms                                                           | 154 ms: 1.30x slower                                                         |
| python_startup_no_site     | 8.85 ms                                                          | 11.8 ms: 1.33x slower                                                        |
| Geometric mean             | (ref)                                                            | 1.03x slower                                                                 |

Benchmark hidden because not significant (9): async_tree_memoization, async_tree_cpu_io_mixed, scimark_fft, xml_etree_parse, deepcopy_reduce, async_tree_none_tg, thrift, async_tree_memoization_tg, bench_mp_pool
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging
Ignored benchmarks (1) of results/bm-20240329-3.13.0a5+-d9cfe7e-JIT/bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e.json: unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.05x