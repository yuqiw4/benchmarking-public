# Results vs. 3.13.0b2

- fork: faster-cpython
- ref: stats_for_all_ops
- machine: linux-x86_64
- commit hash: 17ed8bc
- commit date: 2024-04-05
- overall geometric mean: 1.00x slower
- HPT reliability: 65.85%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240405-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-17ed8bc |
|----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 269 ms: 1.02x faster                                                          |
| chameleon      | 7.22 ms                                                    | 6.99 ms: 1.03x faster                                                         |
| docutils       | 2.83 sec                                                   | 2.81 sec: 1.01x faster                                                        |
| html5lib       | 67.2 ms                                                    | 66.6 ms: 1.01x faster                                                         |
| Geometric mean | (ref)                                                      | 1.01x faster                                                                  |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240405-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-17ed8bc |
|----------------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_none            | 378 ms                                                     | 352 ms: 1.07x faster                                                          |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 608 ms: 1.03x slower                                                          |
| Geometric mean             | (ref)                                                      | 1.01x faster                                                                  |

Benchmark hidden because not significant (6): async_tree_io, async_tree_none_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_memoization, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240405-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-17ed8bc |
|----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| pidigits       | 191 ms                                                     | 191 ms: 1.00x faster                                                          |
| float          | 78.9 ms                                                    | 81.0 ms: 1.03x slower                                                         |
| nbody          | 88.3 ms                                                    | 116 ms: 1.31x slower                                                          |
| Geometric mean | (ref)                                                      | 1.10x slower                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240405-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-17ed8bc |
|----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_compile  | 137 ms                                                     | 136 ms: 1.01x faster                                                          |
| regex_v8       | 25.1 ms                                                    | 26.1 ms: 1.04x slower                                                         |
| regex_dna      | 221 ms                                                     | 232 ms: 1.05x slower                                                          |
| regex_effbot   | 3.67 ms                                                    | 3.87 ms: 1.05x slower                                                         |
| Geometric mean | (ref)                                                      | 1.03x slower                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240405-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-17ed8bc |
|----------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| xml_etree_process    | 61.2 ms                                                    | 59.8 ms: 1.02x faster                                                         |
| pickle_pure_python   | 305 us                                                     | 299 us: 1.02x faster                                                          |
| json_dumps           | 10.7 ms                                                    | 10.5 ms: 1.02x faster                                                         |
| unpickle_list        | 5.34 us                                                    | 5.27 us: 1.01x faster                                                         |
| xml_etree_generate   | 87.4 ms                                                    | 86.4 ms: 1.01x faster                                                         |
| json_loads           | 28.9 us                                                    | 28.6 us: 1.01x faster                                                         |
| xml_etree_iterparse  | 107 ms                                                     | 106 ms: 1.01x faster                                                          |
| pickle_dict          | 34.8 us                                                    | 34.5 us: 1.01x faster                                                         |
| unpickle_pure_python | 218 us                                                     | 217 us: 1.00x faster                                                          |
| pickle_list          | 5.11 us                                                    | 5.26 us: 1.03x slower                                                         |
| pickle               | 11.5 us                                                    | 11.9 us: 1.04x slower                                                         |
| unpickle             | 15.1 us                                                    | 15.8 us: 1.04x slower                                                         |
| tomli_loads          | 2.12 sec                                                   | 2.25 sec: 1.06x slower                                                        |
| Geometric mean       | (ref)                                                      | 1.00x slower                                                                  |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240405-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-17ed8bc |
|------------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 10.6 ms: 1.01x faster                                                         |
| python_startup_no_site | 7.11 ms                                                    | 9.02 ms: 1.27x slower                                                         |
| Geometric mean         | (ref)                                                      | 1.12x slower                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240405-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-17ed8bc |
|----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| mako           | 11.2 ms                                                    | 11.0 ms: 1.02x faster                                                         |
| genshi_text    | 23.7 ms                                                    | 23.4 ms: 1.01x faster                                                         |
| Geometric mean | (ref)                                                      | 1.01x faster                                                                  |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240405-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-17ed8bc |
|----------------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 114 us: 1.44x faster                                                          |
| pylint                     | 317 ms                                                     | 279 ms: 1.14x faster                                                          |
| richards                   | 50.9 ms                                                    | 46.8 ms: 1.09x faster                                                         |
| richards_super             | 57.4 ms                                                    | 52.9 ms: 1.08x faster                                                         |
| async_tree_none            | 378 ms                                                     | 352 ms: 1.07x faster                                                          |
| crypto_pyaes               | 77.5 ms                                                    | 73.0 ms: 1.06x faster                                                         |
| deepcopy_reduce            | 3.35 us                                                    | 3.20 us: 1.05x faster                                                         |
| gc_traversal               | 3.98 ms                                                    | 3.80 ms: 1.05x faster                                                         |
| scimark_lu                 | 122 ms                                                     | 117 ms: 1.04x faster                                                          |
| deepcopy_memo              | 39.7 us                                                    | 38.1 us: 1.04x faster                                                         |
| create_gc_cycles           | 1.82 ms                                                    | 1.75 ms: 1.04x faster                                                         |
| logging_silent             | 105 ns                                                     | 101 ns: 1.03x faster                                                          |
| deepcopy                   | 367 us                                                     | 355 us: 1.03x faster                                                          |
| chameleon                  | 7.22 ms                                                    | 6.99 ms: 1.03x faster                                                         |
| pprint_pformat             | 1.56 sec                                                   | 1.51 sec: 1.03x faster                                                        |
| pprint_safe_repr           | 758 ms                                                     | 737 ms: 1.03x faster                                                          |
| mako                       | 11.2 ms                                                    | 11.0 ms: 1.02x faster                                                         |
| xml_etree_process          | 61.2 ms                                                    | 59.8 ms: 1.02x faster                                                         |
| hexiom                     | 6.30 ms                                                    | 6.15 ms: 1.02x faster                                                         |
| thrift                     | 823 us                                                     | 804 us: 1.02x faster                                                          |
| sqlglot_transpile          | 1.63 ms                                                    | 1.60 ms: 1.02x faster                                                         |
| pickle_pure_python         | 305 us                                                     | 299 us: 1.02x faster                                                          |
| sqlite_synth               | 2.99 us                                                    | 2.93 us: 1.02x faster                                                         |
| json_dumps                 | 10.7 ms                                                    | 10.5 ms: 1.02x faster                                                         |
| sqlglot_parse              | 1.32 ms                                                    | 1.30 ms: 1.02x faster                                                         |
| 2to3                       | 274 ms                                                     | 269 ms: 1.02x faster                                                          |
| unpickle_list              | 5.34 us                                                    | 5.27 us: 1.01x faster                                                         |
| deltablue                  | 3.25 ms                                                    | 3.21 ms: 1.01x faster                                                         |
| python_startup             | 10.8 ms                                                    | 10.6 ms: 1.01x faster                                                         |
| meteor_contest             | 110 ms                                                     | 109 ms: 1.01x faster                                                          |
| xml_etree_generate         | 87.4 ms                                                    | 86.4 ms: 1.01x faster                                                         |
| json_loads                 | 28.9 us                                                    | 28.6 us: 1.01x faster                                                         |
| genshi_text                | 23.7 ms                                                    | 23.4 ms: 1.01x faster                                                         |
| sqlglot_optimize           | 55.5 ms                                                    | 54.9 ms: 1.01x faster                                                         |
| xml_etree_iterparse        | 107 ms                                                     | 106 ms: 1.01x faster                                                          |
| pickle_dict                | 34.8 us                                                    | 34.5 us: 1.01x faster                                                         |
| gunicorn                   | 1.28 ms                                                    | 1.27 ms: 1.01x faster                                                         |
| html5lib                   | 67.2 ms                                                    | 66.6 ms: 1.01x faster                                                         |
| sympy_str                  | 282 ms                                                     | 280 ms: 1.01x faster                                                          |
| aiohttp                    | 1.18 ms                                                    | 1.17 ms: 1.01x faster                                                         |
| generators                 | 29.6 ms                                                    | 29.4 ms: 1.01x faster                                                         |
| regex_compile              | 137 ms                                                     | 136 ms: 1.01x faster                                                          |
| docutils                   | 2.83 sec                                                   | 2.81 sec: 1.01x faster                                                        |
| bench_thread_pool          | 834 us                                                     | 828 us: 1.01x faster                                                          |
| asyncio_websockets         | 567 ms                                                     | 563 ms: 1.01x faster                                                          |
| logging_format             | 6.47 us                                                    | 6.44 us: 1.00x faster                                                         |
| pyflate                    | 484 ms                                                     | 482 ms: 1.00x faster                                                          |
| unpickle_pure_python       | 218 us                                                     | 217 us: 1.00x faster                                                          |
| sympy_integrate            | 20.5 ms                                                    | 20.4 ms: 1.00x faster                                                         |
| pidigits                   | 191 ms                                                     | 191 ms: 1.00x faster                                                          |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.84 sec: 1.00x slower                                                        |
| comprehensions             | 16.6 us                                                    | 16.7 us: 1.00x slower                                                         |
| fannkuch                   | 402 ms                                                     | 404 ms: 1.00x slower                                                          |
| async_generators           | 442 ms                                                     | 444 ms: 1.00x slower                                                          |
| logging_simple             | 5.74 us                                                    | 5.78 us: 1.01x slower                                                         |
| dulwich_log                | 67.2 ms                                                    | 67.6 ms: 1.01x slower                                                         |
| json                       | 5.31 ms                                                    | 5.39 ms: 1.02x slower                                                         |
| nqueens                    | 81.4 ms                                                    | 83.5 ms: 1.03x slower                                                         |
| telco                      | 8.41 ms                                                    | 8.63 ms: 1.03x slower                                                         |
| float                      | 78.9 ms                                                    | 81.0 ms: 1.03x slower                                                         |
| pickle_list                | 5.11 us                                                    | 5.26 us: 1.03x slower                                                         |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 608 ms: 1.03x slower                                                          |
| coroutines                 | 23.2 ms                                                    | 24.0 ms: 1.04x slower                                                         |
| regex_v8                   | 25.1 ms                                                    | 26.1 ms: 1.04x slower                                                         |
| pycparser                  | 1.16 sec                                                   | 1.20 sec: 1.04x slower                                                        |
| pickle                     | 11.5 us                                                    | 11.9 us: 1.04x slower                                                         |
| raytrace                   | 267 ms                                                     | 278 ms: 1.04x slower                                                          |
| unpickle                   | 15.1 us                                                    | 15.8 us: 1.04x slower                                                         |
| regex_dna                  | 221 ms                                                     | 232 ms: 1.05x slower                                                          |
| scimark_sor                | 127 ms                                                     | 134 ms: 1.05x slower                                                          |
| scimark_monte_carlo        | 69.2 ms                                                    | 72.8 ms: 1.05x slower                                                         |
| regex_effbot               | 3.67 ms                                                    | 3.87 ms: 1.05x slower                                                         |
| coverage                   | 93.1 ms                                                    | 98.6 ms: 1.06x slower                                                         |
| tomli_loads                | 2.12 sec                                                   | 2.25 sec: 1.06x slower                                                        |
| scimark_fft                | 392 ms                                                     | 419 ms: 1.07x slower                                                          |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 5.74 ms: 1.09x slower                                                         |
| pathlib                    | 17.3 ms                                                    | 19.1 ms: 1.10x slower                                                         |
| chaos                      | 61.3 ms                                                    | 67.8 ms: 1.11x slower                                                         |
| spectral_norm              | 116 ms                                                     | 135 ms: 1.16x slower                                                          |
| python_startup_no_site     | 7.11 ms                                                    | 9.02 ms: 1.27x slower                                                         |
| nbody                      | 88.3 ms                                                    | 116 ms: 1.31x slower                                                          |
| Geometric mean             | (ref)                                                      | 1.00x slower                                                                  |

Benchmark hidden because not significant (18): xml_etree_parse, async_tree_io, async_tree_none_tg, async_tree_io_tg, async_tree_memoization_tg, dask, mypy2, sympy_expand, async_tree_memoization, bench_mp_pool, sqlglot_normalize, genshi_xml, tornado_http, sympy_sum, mdp, asyncio_tcp, go, async_tree_cpu_io_mixed
Ignored benchmarks (4) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, django_template, djangocms, flaskblogging

# HPT report

- Reliability score: 65.85% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.98x