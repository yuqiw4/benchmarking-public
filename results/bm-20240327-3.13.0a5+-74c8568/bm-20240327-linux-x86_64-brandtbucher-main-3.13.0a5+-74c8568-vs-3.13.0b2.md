# Results vs. 3.13.0b2

- fork: brandtbucher
- ref: main
- machine: linux-x86_64
- commit hash: 74c8568
- commit date: 2024-03-27
- overall geometric mean: 1.02x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.97x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240327-linux-x86_64-brandtbucher-main-3.13.0a5+-74c8568 |
|----------------|:----------------------------------------------------------:|:------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 267 ms: 1.03x faster                                         |
| chameleon      | 7.22 ms                                                    | 6.82 ms: 1.06x faster                                        |
| docutils       | 2.83 sec                                                   | 2.77 sec: 1.02x faster                                       |
| html5lib       | 67.2 ms                                                    | 67.9 ms: 1.01x slower                                        |
| Geometric mean | (ref)                                                      | 1.02x faster                                                 |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240327-linux-x86_64-brandtbucher-main-3.13.0a5+-74c8568 |
|----------------------------|:----------------------------------------------------------:|:------------------------------------------------------------:|
| async_tree_memoization     | 463 ms                                                     | 440 ms: 1.05x faster                                         |
| async_tree_cpu_io_mixed    | 611 ms                                                     | 592 ms: 1.03x faster                                         |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 577 ms: 1.02x faster                                         |
| Geometric mean             | (ref)                                                      | 1.02x faster                                                 |

Benchmark hidden because not significant (5): async_tree_io, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240327-linux-x86_64-brandtbucher-main-3.13.0a5+-74c8568 |
|----------------|:----------------------------------------------------------:|:------------------------------------------------------------:|
| float          | 78.9 ms                                                    | 76.6 ms: 1.03x faster                                        |
| pidigits       | 191 ms                                                     | 189 ms: 1.01x faster                                         |
| Geometric mean | (ref)                                                      | 1.01x faster                                                 |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240327-linux-x86_64-brandtbucher-main-3.13.0a5+-74c8568 |
|----------------|:----------------------------------------------------------:|:------------------------------------------------------------:|
| regex_compile  | 137 ms                                                     | 133 ms: 1.03x faster                                         |
| regex_v8       | 25.1 ms                                                    | 26.0 ms: 1.04x slower                                        |
| regex_effbot   | 3.67 ms                                                    | 3.81 ms: 1.04x slower                                        |
| regex_dna      | 221 ms                                                     | 230 ms: 1.04x slower                                         |
| Geometric mean | (ref)                                                      | 1.02x slower                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240327-linux-x86_64-brandtbucher-main-3.13.0a5+-74c8568 |
|----------------------|:----------------------------------------------------------:|:------------------------------------------------------------:|
| pickle_pure_python   | 305 us                                                     | 297 us: 1.03x faster                                         |
| json_dumps           | 10.7 ms                                                    | 10.4 ms: 1.03x faster                                        |
| xml_etree_process    | 61.2 ms                                                    | 59.8 ms: 1.02x faster                                        |
| xml_etree_generate   | 87.4 ms                                                    | 85.8 ms: 1.02x faster                                        |
| unpickle_pure_python | 218 us                                                     | 215 us: 1.02x faster                                         |
| unpickle_list        | 5.34 us                                                    | 5.26 us: 1.02x faster                                        |
| xml_etree_iterparse  | 107 ms                                                     | 106 ms: 1.01x faster                                         |
| json_loads           | 28.9 us                                                    | 28.6 us: 1.01x faster                                        |
| pickle_dict          | 34.8 us                                                    | 35.6 us: 1.02x slower                                        |
| tomli_loads          | 2.12 sec                                                   | 2.20 sec: 1.04x slower                                       |
| pickle               | 11.5 us                                                    | 12.0 us: 1.05x slower                                        |
| pickle_list          | 5.11 us                                                    | 5.40 us: 1.06x slower                                        |
| unpickle             | 15.1 us                                                    | 16.7 us: 1.10x slower                                        |
| Geometric mean       | (ref)                                                      | 1.01x slower                                                 |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240327-linux-x86_64-brandtbucher-main-3.13.0a5+-74c8568 |
|------------------------|:----------------------------------------------------------:|:------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 10.6 ms: 1.01x faster                                        |
| python_startup_no_site | 7.11 ms                                                    | 9.00 ms: 1.27x slower                                        |
| Geometric mean         | (ref)                                                      | 1.12x slower                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240327-linux-x86_64-brandtbucher-main-3.13.0a5+-74c8568 |
|----------------|:----------------------------------------------------------:|:------------------------------------------------------------:|
| mako           | 11.2 ms                                                    | 10.7 ms: 1.05x faster                                        |
| genshi_xml     | 51.6 ms                                                    | 50.8 ms: 1.02x faster                                        |
| genshi_text    | 23.7 ms                                                    | 24.0 ms: 1.01x slower                                        |
| Geometric mean | (ref)                                                      | 1.01x faster                                                 |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240327-linux-x86_64-brandtbucher-main-3.13.0a5+-74c8568 |
|----------------------------|:----------------------------------------------------------:|:------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 111 us: 1.49x faster                                         |
| richards                   | 50.9 ms                                                    | 45.4 ms: 1.12x faster                                        |
| richards_super             | 57.4 ms                                                    | 51.2 ms: 1.12x faster                                        |
| scimark_fft                | 392 ms                                                     | 358 ms: 1.10x faster                                         |
| create_gc_cycles           | 1.82 ms                                                    | 1.68 ms: 1.08x faster                                        |
| deepcopy_reduce            | 3.35 us                                                    | 3.10 us: 1.08x faster                                        |
| deepcopy_memo              | 39.7 us                                                    | 37.0 us: 1.07x faster                                        |
| scimark_lu                 | 122 ms                                                     | 114 ms: 1.07x faster                                         |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 4.95 ms: 1.06x faster                                        |
| deepcopy                   | 367 us                                                     | 347 us: 1.06x faster                                         |
| crypto_pyaes               | 77.5 ms                                                    | 73.1 ms: 1.06x faster                                        |
| logging_silent             | 105 ns                                                     | 98.9 ns: 1.06x faster                                        |
| chameleon                  | 7.22 ms                                                    | 6.82 ms: 1.06x faster                                        |
| spectral_norm              | 116 ms                                                     | 110 ms: 1.06x faster                                         |
| async_tree_memoization     | 463 ms                                                     | 440 ms: 1.05x faster                                         |
| mako                       | 11.2 ms                                                    | 10.7 ms: 1.05x faster                                        |
| scimark_monte_carlo        | 69.2 ms                                                    | 66.0 ms: 1.05x faster                                        |
| scimark_sor                | 127 ms                                                     | 122 ms: 1.04x faster                                         |
| pyflate                    | 484 ms                                                     | 464 ms: 1.04x faster                                         |
| sqlite_synth               | 2.99 us                                                    | 2.88 us: 1.04x faster                                        |
| sqlglot_transpile          | 1.63 ms                                                    | 1.58 ms: 1.04x faster                                        |
| sympy_str                  | 282 ms                                                     | 272 ms: 1.04x faster                                         |
| pprint_pformat             | 1.56 sec                                                   | 1.50 sec: 1.04x faster                                       |
| go                         | 145 ms                                                     | 140 ms: 1.03x faster                                         |
| async_tree_cpu_io_mixed    | 611 ms                                                     | 592 ms: 1.03x faster                                         |
| mdp                        | 2.79 sec                                                   | 2.70 sec: 1.03x faster                                       |
| sqlglot_parse              | 1.32 ms                                                    | 1.28 ms: 1.03x faster                                        |
| float                      | 78.9 ms                                                    | 76.6 ms: 1.03x faster                                        |
| regex_compile              | 137 ms                                                     | 133 ms: 1.03x faster                                         |
| fannkuch                   | 402 ms                                                     | 391 ms: 1.03x faster                                         |
| chaos                      | 61.3 ms                                                    | 59.7 ms: 1.03x faster                                        |
| pickle_pure_python         | 305 us                                                     | 297 us: 1.03x faster                                         |
| json_dumps                 | 10.7 ms                                                    | 10.4 ms: 1.03x faster                                        |
| 2to3                       | 274 ms                                                     | 267 ms: 1.03x faster                                         |
| pprint_safe_repr           | 758 ms                                                     | 740 ms: 1.03x faster                                         |
| sympy_expand               | 473 ms                                                     | 461 ms: 1.02x faster                                         |
| sympy_integrate            | 20.5 ms                                                    | 20.0 ms: 1.02x faster                                        |
| xml_etree_process          | 61.2 ms                                                    | 59.8 ms: 1.02x faster                                        |
| sympy_sum                  | 156 ms                                                     | 153 ms: 1.02x faster                                         |
| docutils                   | 2.83 sec                                                   | 2.77 sec: 1.02x faster                                       |
| xml_etree_generate         | 87.4 ms                                                    | 85.8 ms: 1.02x faster                                        |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 577 ms: 1.02x faster                                         |
| hexiom                     | 6.30 ms                                                    | 6.19 ms: 1.02x faster                                        |
| genshi_xml                 | 51.6 ms                                                    | 50.8 ms: 1.02x faster                                        |
| unpickle_pure_python       | 218 us                                                     | 215 us: 1.02x faster                                         |
| unpickle_list              | 5.34 us                                                    | 5.26 us: 1.02x faster                                        |
| sqlglot_optimize           | 55.5 ms                                                    | 54.7 ms: 1.01x faster                                        |
| asyncio_tcp                | 508 ms                                                     | 501 ms: 1.01x faster                                         |
| sqlglot_normalize          | 110 ms                                                     | 109 ms: 1.01x faster                                         |
| raytrace                   | 267 ms                                                     | 263 ms: 1.01x faster                                         |
| python_startup             | 10.8 ms                                                    | 10.6 ms: 1.01x faster                                        |
| nqueens                    | 81.4 ms                                                    | 80.5 ms: 1.01x faster                                        |
| pidigits                   | 191 ms                                                     | 189 ms: 1.01x faster                                         |
| bench_thread_pool          | 834 us                                                     | 825 us: 1.01x faster                                         |
| coroutines                 | 23.2 ms                                                    | 23.0 ms: 1.01x faster                                        |
| comprehensions             | 16.6 us                                                    | 16.5 us: 1.01x faster                                        |
| xml_etree_iterparse        | 107 ms                                                     | 106 ms: 1.01x faster                                         |
| json_loads                 | 28.9 us                                                    | 28.6 us: 1.01x faster                                        |
| meteor_contest             | 110 ms                                                     | 109 ms: 1.01x faster                                         |
| thrift                     | 823 us                                                     | 819 us: 1.00x faster                                         |
| generators                 | 29.6 ms                                                    | 29.5 ms: 1.00x faster                                        |
| asyncio_websockets         | 567 ms                                                     | 569 ms: 1.00x slower                                         |
| gc_traversal               | 3.98 ms                                                    | 4.01 ms: 1.01x slower                                        |
| html5lib                   | 67.2 ms                                                    | 67.9 ms: 1.01x slower                                        |
| json                       | 5.31 ms                                                    | 5.37 ms: 1.01x slower                                        |
| genshi_text                | 23.7 ms                                                    | 24.0 ms: 1.01x slower                                        |
| logging_format             | 6.47 us                                                    | 6.59 us: 1.02x slower                                        |
| telco                      | 8.41 ms                                                    | 8.59 ms: 1.02x slower                                        |
| logging_simple             | 5.74 us                                                    | 5.87 us: 1.02x slower                                        |
| pickle_dict                | 34.8 us                                                    | 35.6 us: 1.02x slower                                        |
| tomli_loads                | 2.12 sec                                                   | 2.20 sec: 1.04x slower                                       |
| regex_v8                   | 25.1 ms                                                    | 26.0 ms: 1.04x slower                                        |
| regex_effbot               | 3.67 ms                                                    | 3.81 ms: 1.04x slower                                        |
| regex_dna                  | 221 ms                                                     | 230 ms: 1.04x slower                                         |
| coverage                   | 93.1 ms                                                    | 97.2 ms: 1.04x slower                                        |
| pickle                     | 11.5 us                                                    | 12.0 us: 1.05x slower                                        |
| pycparser                  | 1.16 sec                                                   | 1.22 sec: 1.06x slower                                       |
| pickle_list                | 5.11 us                                                    | 5.40 us: 1.06x slower                                        |
| pathlib                    | 17.3 ms                                                    | 18.5 ms: 1.07x slower                                        |
| unpickle                   | 15.1 us                                                    | 16.7 us: 1.10x slower                                        |
| python_startup_no_site     | 7.11 ms                                                    | 9.00 ms: 1.27x slower                                        |
| Geometric mean             | (ref)                                                      | 1.02x faster                                                 |

Benchmark hidden because not significant (20): async_tree_io, async_tree_io_tg, mypy2, dask, xml_etree_parse, gunicorn, bench_mp_pool, async_generators, aiohttp, asyncio_tcp_ssl, nbody, django_template, pylint, deltablue, dulwich_log, tornado_http, async_tree_memoization_tg, async_tree_none_tg, djangocms, async_tree_none
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging
Ignored benchmarks (1) of results/bm-20240327-3.13.0a5+-74c8568/bm-20240327-linux-x86_64-brandtbucher-main-3.13.0a5+-74c8568.json: unpack_sequence

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.97x