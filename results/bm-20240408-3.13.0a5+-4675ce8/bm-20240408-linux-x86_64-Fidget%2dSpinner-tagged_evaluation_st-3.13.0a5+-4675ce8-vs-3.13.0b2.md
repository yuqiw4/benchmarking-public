# Results vs. 3.13.0b2

- fork: Fidget-Spinner
- ref: tagged_evaluation_st
- machine: linux-x86_64
- commit hash: 4675ce8
- commit date: 2024-04-08
- overall geometric mean: 1.02x faster
- HPT reliability: 99.98%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-linux-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 268 ms: 1.02x faster                                                             |
| chameleon      | 7.22 ms                                                    | 6.74 ms: 1.07x faster                                                            |
| tornado_http   | 94.6 ms                                                    | 94.2 ms: 1.00x faster                                                            |
| Geometric mean | (ref)                                                      | 1.02x faster                                                                     |

Benchmark hidden because not significant (2): docutils, html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-linux-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none            | 378 ms                                                     | 352 ms: 1.07x faster                                                             |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 608 ms: 1.03x slower                                                             |
| Geometric mean             | (ref)                                                      | 1.01x faster                                                                     |

Benchmark hidden because not significant (6): async_tree_io, async_tree_memoization_tg, async_tree_none_tg, async_tree_cpu_io_mixed, async_tree_io_tg, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-linux-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| float          | 78.9 ms                                                    | 78.1 ms: 1.01x faster                                                            |
| pidigits       | 191 ms                                                     | 211 ms: 1.10x slower                                                             |
| Geometric mean | (ref)                                                      | 1.03x slower                                                                     |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-linux-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 137 ms                                                     | 134 ms: 1.02x faster                                                             |
| regex_dna      | 221 ms                                                     | 226 ms: 1.02x slower                                                             |
| regex_effbot   | 3.67 ms                                                    | 3.77 ms: 1.03x slower                                                            |
| regex_v8       | 25.1 ms                                                    | 26.2 ms: 1.04x slower                                                            |
| Geometric mean | (ref)                                                      | 1.02x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-linux-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_list          | 5.11 us                                                    | 4.90 us: 1.04x faster                                                            |
| unpickle_list        | 5.34 us                                                    | 5.15 us: 1.04x faster                                                            |
| pickle_dict          | 34.8 us                                                    | 33.7 us: 1.03x faster                                                            |
| xml_etree_process    | 61.2 ms                                                    | 60.0 ms: 1.02x faster                                                            |
| pickle_pure_python   | 305 us                                                     | 300 us: 1.02x faster                                                             |
| json_dumps           | 10.7 ms                                                    | 10.6 ms: 1.01x faster                                                            |
| xml_etree_iterparse  | 107 ms                                                     | 106 ms: 1.01x faster                                                             |
| xml_etree_generate   | 87.4 ms                                                    | 87.2 ms: 1.00x faster                                                            |
| unpickle_pure_python | 218 us                                                     | 221 us: 1.01x slower                                                             |
| pickle               | 11.5 us                                                    | 11.6 us: 1.01x slower                                                            |
| tomli_loads          | 2.12 sec                                                   | 2.17 sec: 1.02x slower                                                           |
| Geometric mean       | (ref)                                                      | 1.01x faster                                                                     |

Benchmark hidden because not significant (3): xml_etree_parse, json_loads, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-linux-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 10.5 ms: 1.02x faster                                                            |
| python_startup_no_site | 7.11 ms                                                    | 8.97 ms: 1.26x slower                                                            |
| Geometric mean         | (ref)                                                      | 1.11x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-linux-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako           | 11.2 ms                                                    | 10.8 ms: 1.04x faster                                                            |
| genshi_text    | 23.7 ms                                                    | 23.8 ms: 1.01x slower                                                            |
| genshi_xml     | 51.6 ms                                                    | 52.1 ms: 1.01x slower                                                            |
| Geometric mean | (ref)                                                      | 1.01x faster                                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-linux-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 115 us: 1.43x faster                                                             |
| pylint                     | 317 ms                                                     | 278 ms: 1.14x faster                                                             |
| richards                   | 50.9 ms                                                    | 46.7 ms: 1.09x faster                                                            |
| richards_super             | 57.4 ms                                                    | 52.7 ms: 1.09x faster                                                            |
| deepcopy_memo              | 39.7 us                                                    | 36.7 us: 1.08x faster                                                            |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 4.89 ms: 1.08x faster                                                            |
| async_tree_none            | 378 ms                                                     | 352 ms: 1.07x faster                                                             |
| scimark_lu                 | 122 ms                                                     | 113 ms: 1.07x faster                                                             |
| pyflate                    | 484 ms                                                     | 451 ms: 1.07x faster                                                             |
| scimark_fft                | 392 ms                                                     | 366 ms: 1.07x faster                                                             |
| chameleon                  | 7.22 ms                                                    | 6.74 ms: 1.07x faster                                                            |
| crypto_pyaes               | 77.5 ms                                                    | 73.1 ms: 1.06x faster                                                            |
| deepcopy_reduce            | 3.35 us                                                    | 3.18 us: 1.05x faster                                                            |
| gc_traversal               | 3.98 ms                                                    | 3.78 ms: 1.05x faster                                                            |
| create_gc_cycles           | 1.82 ms                                                    | 1.73 ms: 1.05x faster                                                            |
| spectral_norm              | 116 ms                                                     | 111 ms: 1.05x faster                                                             |
| scimark_sor                | 127 ms                                                     | 122 ms: 1.05x faster                                                             |
| mako                       | 11.2 ms                                                    | 10.8 ms: 1.04x faster                                                            |
| pickle_list                | 5.11 us                                                    | 4.90 us: 1.04x faster                                                            |
| go                         | 145 ms                                                     | 139 ms: 1.04x faster                                                             |
| deltablue                  | 3.25 ms                                                    | 3.13 ms: 1.04x faster                                                            |
| unpickle_list              | 5.34 us                                                    | 5.15 us: 1.04x faster                                                            |
| logging_silent             | 105 ns                                                     | 101 ns: 1.04x faster                                                             |
| deepcopy                   | 367 us                                                     | 354 us: 1.04x faster                                                             |
| sqlglot_transpile          | 1.63 ms                                                    | 1.58 ms: 1.04x faster                                                            |
| sqlglot_parse              | 1.32 ms                                                    | 1.28 ms: 1.04x faster                                                            |
| chaos                      | 61.3 ms                                                    | 59.3 ms: 1.03x faster                                                            |
| pickle_dict                | 34.8 us                                                    | 33.7 us: 1.03x faster                                                            |
| fannkuch                   | 402 ms                                                     | 389 ms: 1.03x faster                                                             |
| raytrace                   | 267 ms                                                     | 259 ms: 1.03x faster                                                             |
| scimark_monte_carlo        | 69.2 ms                                                    | 67.6 ms: 1.02x faster                                                            |
| coroutines                 | 23.2 ms                                                    | 22.7 ms: 1.02x faster                                                            |
| pprint_pformat             | 1.56 sec                                                   | 1.52 sec: 1.02x faster                                                           |
| 2to3                       | 274 ms                                                     | 268 ms: 1.02x faster                                                             |
| python_startup             | 10.8 ms                                                    | 10.5 ms: 1.02x faster                                                            |
| regex_compile              | 137 ms                                                     | 134 ms: 1.02x faster                                                             |
| logging_format             | 6.47 us                                                    | 6.34 us: 1.02x faster                                                            |
| xml_etree_process          | 61.2 ms                                                    | 60.0 ms: 1.02x faster                                                            |
| pprint_safe_repr           | 758 ms                                                     | 745 ms: 1.02x faster                                                             |
| pickle_pure_python         | 305 us                                                     | 300 us: 1.02x faster                                                             |
| sympy_str                  | 282 ms                                                     | 278 ms: 1.02x faster                                                             |
| sqlite_synth               | 2.99 us                                                    | 2.94 us: 1.02x faster                                                            |
| nqueens                    | 81.4 ms                                                    | 80.2 ms: 1.01x faster                                                            |
| aiohttp                    | 1.18 ms                                                    | 1.16 ms: 1.01x faster                                                            |
| sympy_integrate            | 20.5 ms                                                    | 20.2 ms: 1.01x faster                                                            |
| meteor_contest             | 110 ms                                                     | 108 ms: 1.01x faster                                                             |
| generators                 | 29.6 ms                                                    | 29.3 ms: 1.01x faster                                                            |
| comprehensions             | 16.6 us                                                    | 16.4 us: 1.01x faster                                                            |
| float                      | 78.9 ms                                                    | 78.1 ms: 1.01x faster                                                            |
| gunicorn                   | 1.28 ms                                                    | 1.27 ms: 1.01x faster                                                            |
| json_dumps                 | 10.7 ms                                                    | 10.6 ms: 1.01x faster                                                            |
| hexiom                     | 6.30 ms                                                    | 6.23 ms: 1.01x faster                                                            |
| xml_etree_iterparse        | 107 ms                                                     | 106 ms: 1.01x faster                                                             |
| mdp                        | 2.79 sec                                                   | 2.76 sec: 1.01x faster                                                           |
| sympy_expand               | 473 ms                                                     | 469 ms: 1.01x faster                                                             |
| logging_simple             | 5.74 us                                                    | 5.70 us: 1.01x faster                                                            |
| sqlglot_optimize           | 55.5 ms                                                    | 55.1 ms: 1.01x faster                                                            |
| bench_thread_pool          | 834 us                                                     | 829 us: 1.01x faster                                                             |
| tornado_http               | 94.6 ms                                                    | 94.2 ms: 1.00x faster                                                            |
| xml_etree_generate         | 87.4 ms                                                    | 87.2 ms: 1.00x faster                                                            |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.84 sec: 1.00x faster                                                           |
| asyncio_tcp                | 508 ms                                                     | 510 ms: 1.00x slower                                                             |
| genshi_text                | 23.7 ms                                                    | 23.8 ms: 1.01x slower                                                            |
| thrift                     | 823 us                                                     | 829 us: 1.01x slower                                                             |
| async_generators           | 442 ms                                                     | 446 ms: 1.01x slower                                                             |
| genshi_xml                 | 51.6 ms                                                    | 52.1 ms: 1.01x slower                                                            |
| unpickle_pure_python       | 218 us                                                     | 221 us: 1.01x slower                                                             |
| pickle                     | 11.5 us                                                    | 11.6 us: 1.01x slower                                                            |
| regex_dna                  | 221 ms                                                     | 226 ms: 1.02x slower                                                             |
| tomli_loads                | 2.12 sec                                                   | 2.17 sec: 1.02x slower                                                           |
| regex_effbot               | 3.67 ms                                                    | 3.77 ms: 1.03x slower                                                            |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 608 ms: 1.03x slower                                                             |
| pycparser                  | 1.16 sec                                                   | 1.20 sec: 1.04x slower                                                           |
| regex_v8                   | 25.1 ms                                                    | 26.2 ms: 1.04x slower                                                            |
| coverage                   | 93.1 ms                                                    | 98.5 ms: 1.06x slower                                                            |
| pathlib                    | 17.3 ms                                                    | 18.7 ms: 1.08x slower                                                            |
| pidigits                   | 191 ms                                                     | 211 ms: 1.10x slower                                                             |
| python_startup_no_site     | 7.11 ms                                                    | 8.97 ms: 1.26x slower                                                            |
| Geometric mean             | (ref)                                                      | 1.02x faster                                                                     |

Benchmark hidden because not significant (21): xml_etree_parse, async_tree_io, async_tree_memoization_tg, html5lib, mypy2, sympy_sum, dask, dulwich_log, asyncio_websockets, async_tree_none_tg, sqlglot_normalize, async_tree_cpu_io_mixed, bench_mp_pool, docutils, async_tree_io_tg, json_loads, unpickle, json, nbody, telco, async_tree_memoization
Ignored benchmarks (4) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, django_template, djangocms, flaskblogging

# HPT report

- Reliability score: 99.98% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.98x