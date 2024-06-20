# Results vs. 3.13.0b2

- fork: python
- ref: 3e06c7f719b99cc7f5e8
- machine: linux-x86_64
- commit hash: 3e06c7f
- commit date: 2024-04-26
- overall geometric mean: 1.02x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.07x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-pythonperf2-x86_64-python-3e06c7f719b99cc7f5e8-3.13.0a6+-3e06c7f |
|----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 291 ms                                                           | 304 ms: 1.04x slower                                                         |
| chameleon      | 7.40 ms                                                          | 7.58 ms: 1.03x slower                                                        |
| docutils       | 2.98 sec                                                         | 3.10 sec: 1.04x slower                                                       |
| html5lib       | 74.7 ms                                                          | 74.0 ms: 1.01x faster                                                        |
| tornado_http   | 119 ms                                                           | 124 ms: 1.04x slower                                                         |
| Geometric mean | (ref)                                                            | 1.03x slower                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-pythonperf2-x86_64-python-3e06c7f719b99cc7f5e8-3.13.0a6+-3e06c7f |
|----------------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none            | 365 ms                                                           | 376 ms: 1.03x slower                                                         |
| async_tree_cpu_io_mixed    | 604 ms                                                           | 622 ms: 1.03x slower                                                         |
| async_tree_cpu_io_mixed_tg | 573 ms                                                           | 595 ms: 1.04x slower                                                         |
| async_tree_io              | 873 ms                                                           | 909 ms: 1.04x slower                                                         |
| Geometric mean             | (ref)                                                            | 1.02x slower                                                                 |

Benchmark hidden because not significant (4): async_tree_io_tg, async_tree_none_tg, async_tree_memoization_tg, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-pythonperf2-x86_64-python-3e06c7f719b99cc7f5e8-3.13.0a6+-3e06c7f |
|----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 80.2 ms                                                          | 76.2 ms: 1.05x faster                                                        |
| pidigits       | 254 ms                                                           | 261 ms: 1.03x slower                                                         |
| nbody          | 87.8 ms                                                          | 99.1 ms: 1.13x slower                                                        |
| Geometric mean | (ref)                                                            | 1.03x slower                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-pythonperf2-x86_64-python-3e06c7f719b99cc7f5e8-3.13.0a6+-3e06c7f |
|----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_v8       | 26.0 ms                                                          | 24.9 ms: 1.04x faster                                                        |
| regex_dna      | 249 ms                                                           | 240 ms: 1.04x faster                                                         |
| regex_compile  | 144 ms                                                           | 143 ms: 1.01x faster                                                         |
| regex_effbot   | 3.40 ms                                                          | 3.44 ms: 1.01x slower                                                        |
| Geometric mean | (ref)                                                            | 1.02x faster                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-pythonperf2-x86_64-python-3e06c7f719b99cc7f5e8-3.13.0a6+-3e06c7f |
|----------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| tomli_loads          | 2.40 sec                                                         | 2.12 sec: 1.13x faster                                                       |
| pickle_dict          | 32.8 us                                                          | 30.8 us: 1.07x faster                                                        |
| unpickle             | 15.7 us                                                          | 15.1 us: 1.04x faster                                                        |
| pickle               | 10.6 us                                                          | 10.3 us: 1.03x faster                                                        |
| xml_etree_generate   | 85.7 ms                                                          | 83.6 ms: 1.03x faster                                                        |
| xml_etree_process    | 59.7 ms                                                          | 58.6 ms: 1.02x faster                                                        |
| json_dumps           | 10.8 ms                                                          | 10.6 ms: 1.02x faster                                                        |
| unpickle_list        | 4.70 us                                                          | 4.64 us: 1.01x faster                                                        |
| xml_etree_iterparse  | 103 ms                                                           | 101 ms: 1.01x faster                                                         |
| unpickle_pure_python | 224 us                                                           | 223 us: 1.01x faster                                                         |
| xml_etree_parse      | 144 ms                                                           | 143 ms: 1.00x faster                                                         |
| json_loads           | 25.0 us                                                          | 24.9 us: 1.00x faster                                                        |
| pickle_list          | 4.44 us                                                          | 4.50 us: 1.01x slower                                                        |
| pickle_pure_python   | 307 us                                                           | 312 us: 1.02x slower                                                         |
| Geometric mean       | (ref)                                                            | 1.02x faster                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-pythonperf2-x86_64-python-3e06c7f719b99cc7f5e8-3.13.0a6+-3e06c7f |
|------------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 13.2 ms                                                          | 13.5 ms: 1.02x slower                                                        |
| python_startup_no_site | 8.85 ms                                                          | 9.44 ms: 1.07x slower                                                        |
| Geometric mean         | (ref)                                                            | 1.04x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-pythonperf2-x86_64-python-3e06c7f719b99cc7f5e8-3.13.0a6+-3e06c7f |
|-----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 10.4 ms                                                          | 9.84 ms: 1.05x faster                                                        |
| django_template | 39.0 ms                                                          | 41.4 ms: 1.06x slower                                                        |
| genshi_xml      | 58.1 ms                                                          | 63.1 ms: 1.09x slower                                                        |
| genshi_text     | 25.9 ms                                                          | 29.7 ms: 1.15x slower                                                        |
| Geometric mean  | (ref)                                                            | 1.06x slower                                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-pythonperf2-x86_64-python-3e06c7f719b99cc7f5e8-3.13.0a6+-3e06c7f |
|----------------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| richards_super             | 61.2 ms                                                          | 52.8 ms: 1.16x faster                                                        |
| richards                   | 53.4 ms                                                          | 46.6 ms: 1.15x faster                                                        |
| tomli_loads                | 2.40 sec                                                         | 2.12 sec: 1.13x faster                                                       |
| gc_traversal               | 4.69 ms                                                          | 4.34 ms: 1.08x faster                                                        |
| coverage                   | 83.5 ms                                                          | 78.0 ms: 1.07x faster                                                        |
| pickle_dict                | 32.8 us                                                          | 30.8 us: 1.07x faster                                                        |
| mako                       | 10.4 ms                                                          | 9.84 ms: 1.05x faster                                                        |
| float                      | 80.2 ms                                                          | 76.2 ms: 1.05x faster                                                        |
| create_gc_cycles           | 2.00 ms                                                          | 1.90 ms: 1.05x faster                                                        |
| scimark_sparse_mat_mult    | 4.28 ms                                                          | 4.08 ms: 1.05x faster                                                        |
| telco                      | 8.40 ms                                                          | 8.00 ms: 1.05x faster                                                        |
| sqlite_synth               | 2.80 us                                                          | 2.67 us: 1.05x faster                                                        |
| spectral_norm              | 97.3 ms                                                          | 92.8 ms: 1.05x faster                                                        |
| regex_v8                   | 26.0 ms                                                          | 24.9 ms: 1.04x faster                                                        |
| regex_dna                  | 249 ms                                                           | 240 ms: 1.04x faster                                                         |
| unpickle                   | 15.7 us                                                          | 15.1 us: 1.04x faster                                                        |
| pickle                     | 10.6 us                                                          | 10.3 us: 1.03x faster                                                        |
| xml_etree_generate         | 85.7 ms                                                          | 83.6 ms: 1.03x faster                                                        |
| xml_etree_process          | 59.7 ms                                                          | 58.6 ms: 1.02x faster                                                        |
| json_dumps                 | 10.8 ms                                                          | 10.6 ms: 1.02x faster                                                        |
| logging_silent             | 96.3 ns                                                          | 94.8 ns: 1.02x faster                                                        |
| logging_format             | 7.11 us                                                          | 7.00 us: 1.02x faster                                                        |
| unpickle_list              | 4.70 us                                                          | 4.64 us: 1.01x faster                                                        |
| xml_etree_iterparse        | 103 ms                                                           | 101 ms: 1.01x faster                                                         |
| regex_compile              | 144 ms                                                           | 143 ms: 1.01x faster                                                         |
| html5lib                   | 74.7 ms                                                          | 74.0 ms: 1.01x faster                                                        |
| unpickle_pure_python       | 224 us                                                           | 223 us: 1.01x faster                                                         |
| pyflate                    | 482 ms                                                           | 479 ms: 1.01x faster                                                         |
| asyncio_tcp                | 378 ms                                                           | 376 ms: 1.01x faster                                                         |
| coroutines                 | 22.0 ms                                                          | 21.9 ms: 1.01x faster                                                        |
| xml_etree_parse            | 144 ms                                                           | 143 ms: 1.00x faster                                                         |
| json_loads                 | 25.0 us                                                          | 24.9 us: 1.00x faster                                                        |
| dulwich_log                | 67.3 ms                                                          | 67.0 ms: 1.00x faster                                                        |
| regex_effbot               | 3.40 ms                                                          | 3.44 ms: 1.01x slower                                                        |
| pickle_list                | 4.44 us                                                          | 4.50 us: 1.01x slower                                                        |
| pickle_pure_python         | 307 us                                                           | 312 us: 1.02x slower                                                         |
| pprint_safe_repr           | 818 ms                                                           | 830 ms: 1.02x slower                                                         |
| sqlglot_parse              | 1.39 ms                                                          | 1.42 ms: 1.02x slower                                                        |
| python_startup             | 13.2 ms                                                          | 13.5 ms: 1.02x slower                                                        |
| pathlib                    | 17.1 ms                                                          | 17.5 ms: 1.02x slower                                                        |
| generators                 | 33.5 ms                                                          | 34.3 ms: 1.02x slower                                                        |
| chameleon                  | 7.40 ms                                                          | 7.58 ms: 1.03x slower                                                        |
| pprint_pformat             | 1.66 sec                                                         | 1.70 sec: 1.03x slower                                                       |
| deepcopy_reduce            | 3.39 us                                                          | 3.48 us: 1.03x slower                                                        |
| async_tree_none            | 365 ms                                                           | 376 ms: 1.03x slower                                                         |
| async_tree_cpu_io_mixed    | 604 ms                                                           | 622 ms: 1.03x slower                                                         |
| pidigits                   | 254 ms                                                           | 261 ms: 1.03x slower                                                         |
| sqlglot_transpile          | 1.76 ms                                                          | 1.82 ms: 1.03x slower                                                        |
| deepcopy_memo              | 37.3 us                                                          | 38.6 us: 1.03x slower                                                        |
| tornado_http               | 119 ms                                                           | 124 ms: 1.04x slower                                                         |
| docutils                   | 2.98 sec                                                         | 3.10 sec: 1.04x slower                                                       |
| dask                       | 391 ms                                                           | 406 ms: 1.04x slower                                                         |
| async_tree_cpu_io_mixed_tg | 573 ms                                                           | 595 ms: 1.04x slower                                                         |
| async_tree_io              | 873 ms                                                           | 909 ms: 1.04x slower                                                         |
| 2to3                       | 291 ms                                                           | 304 ms: 1.04x slower                                                         |
| thrift                     | 880 us                                                           | 918 us: 1.04x slower                                                         |
| meteor_contest             | 128 ms                                                           | 134 ms: 1.05x slower                                                         |
| pycparser                  | 1.22 sec                                                         | 1.28 sec: 1.05x slower                                                       |
| mdp                        | 2.46 sec                                                         | 2.58 sec: 1.05x slower                                                       |
| bench_thread_pool          | 908 us                                                           | 955 us: 1.05x slower                                                         |
| async_generators           | 363 ms                                                           | 382 ms: 1.05x slower                                                         |
| go                         | 165 ms                                                           | 174 ms: 1.05x slower                                                         |
| raytrace                   | 260 ms                                                           | 275 ms: 1.06x slower                                                         |
| crypto_pyaes               | 73.6 ms                                                          | 77.8 ms: 1.06x slower                                                        |
| aiohttp                    | 1.07 ms                                                          | 1.13 ms: 1.06x slower                                                        |
| sympy_expand               | 501 ms                                                           | 531 ms: 1.06x slower                                                         |
| sympy_str                  | 295 ms                                                           | 313 ms: 1.06x slower                                                         |
| django_template            | 39.0 ms                                                          | 41.4 ms: 1.06x slower                                                        |
| sqlglot_normalize          | 120 ms                                                           | 128 ms: 1.06x slower                                                         |
| gunicorn                   | 1.04 ms                                                          | 1.11 ms: 1.06x slower                                                        |
| python_startup_no_site     | 8.85 ms                                                          | 9.44 ms: 1.07x slower                                                        |
| sympy_sum                  | 155 ms                                                           | 165 ms: 1.07x slower                                                         |
| fannkuch                   | 353 ms                                                           | 377 ms: 1.07x slower                                                         |
| scimark_monte_carlo        | 65.5 ms                                                          | 70.5 ms: 1.08x slower                                                        |
| deepcopy                   | 377 us                                                           | 408 us: 1.08x slower                                                         |
| genshi_xml                 | 58.1 ms                                                          | 63.1 ms: 1.09x slower                                                        |
| sqlglot_optimize           | 59.5 ms                                                          | 64.7 ms: 1.09x slower                                                        |
| typing_runtime_protocols   | 171 us                                                           | 186 us: 1.09x slower                                                         |
| chaos                      | 59.6 ms                                                          | 65.5 ms: 1.10x slower                                                        |
| pylint                     | 339 ms                                                           | 373 ms: 1.10x slower                                                         |
| sympy_integrate            | 23.2 ms                                                          | 25.7 ms: 1.11x slower                                                        |
| mypy2                      | 764 ms                                                           | 855 ms: 1.12x slower                                                         |
| nbody                      | 87.8 ms                                                          | 99.1 ms: 1.13x slower                                                        |
| deltablue                  | 3.37 ms                                                          | 3.83 ms: 1.14x slower                                                        |
| nqueens                    | 88.4 ms                                                          | 101 ms: 1.14x slower                                                         |
| genshi_text                | 25.9 ms                                                          | 29.7 ms: 1.15x slower                                                        |
| hexiom                     | 6.35 ms                                                          | 7.31 ms: 1.15x slower                                                        |
| comprehensions             | 17.0 us                                                          | 19.6 us: 1.16x slower                                                        |
| scimark_lu                 | 97.5 ms                                                          | 113 ms: 1.16x slower                                                         |
| scimark_sor                | 119 ms                                                           | 151 ms: 1.27x slower                                                         |
| Geometric mean             | (ref)                                                            | 1.02x slower                                                                 |

Benchmark hidden because not significant (10): async_tree_io_tg, scimark_fft, bench_mp_pool, asyncio_tcp_ssl, json, logging_simple, async_tree_none_tg, async_tree_memoization_tg, asyncio_websockets, async_tree_memoization
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.07x