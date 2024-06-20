# Results vs. 3.13.0b2

- fork: faster-cpython
- ref: stats_for_all_ops
- machine: linux-x86_64
- commit hash: dd7732d
- commit date: 2024-04-04
- overall geometric mean: 1.00x slower
- HPT reliability: 76.18%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-dd7732d |
|----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 268 ms: 1.02x faster                                                          |
| chameleon      | 7.22 ms                                                    | 6.98 ms: 1.03x faster                                                         |
| docutils       | 2.83 sec                                                   | 2.80 sec: 1.01x faster                                                        |
| html5lib       | 67.2 ms                                                    | 68.2 ms: 1.01x slower                                                         |
| Geometric mean | (ref)                                                      | 1.01x faster                                                                  |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-dd7732d |
|----------------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_none            | 378 ms                                                     | 351 ms: 1.08x faster                                                          |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 606 ms: 1.03x slower                                                          |
| Geometric mean             | (ref)                                                      | 1.01x faster                                                                  |

Benchmark hidden because not significant (6): async_tree_io, async_tree_none_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_cpu_io_mixed, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-dd7732d |
|----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| float          | 78.9 ms                                                    | 81.3 ms: 1.03x slower                                                         |
| pidigits       | 191 ms                                                     | 198 ms: 1.04x slower                                                          |
| nbody          | 88.3 ms                                                    | 127 ms: 1.43x slower                                                          |
| Geometric mean | (ref)                                                      | 1.15x slower                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-dd7732d |
|----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_v8       | 25.1 ms                                                    | 24.4 ms: 1.03x faster                                                         |
| regex_compile  | 137 ms                                                     | 135 ms: 1.01x faster                                                          |
| regex_dna      | 221 ms                                                     | 221 ms: 1.00x faster                                                          |
| regex_effbot   | 3.67 ms                                                    | 3.75 ms: 1.02x slower                                                         |
| Geometric mean | (ref)                                                      | 1.01x faster                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-dd7732d |
|----------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| pickle_list          | 5.11 us                                                    | 4.93 us: 1.04x faster                                                         |
| unpickle_list        | 5.34 us                                                    | 5.22 us: 1.02x faster                                                         |
| pickle_pure_python   | 305 us                                                     | 299 us: 1.02x faster                                                          |
| pickle_dict          | 34.8 us                                                    | 34.2 us: 1.02x faster                                                         |
| xml_etree_parse      | 162 ms                                                     | 159 ms: 1.02x faster                                                          |
| xml_etree_iterparse  | 107 ms                                                     | 106 ms: 1.01x faster                                                          |
| xml_etree_process    | 61.2 ms                                                    | 60.9 ms: 1.00x faster                                                         |
| unpickle_pure_python | 218 us                                                     | 219 us: 1.00x slower                                                          |
| unpickle             | 15.1 us                                                    | 15.3 us: 1.01x slower                                                         |
| xml_etree_generate   | 87.4 ms                                                    | 88.8 ms: 1.02x slower                                                         |
| pickle               | 11.5 us                                                    | 11.7 us: 1.02x slower                                                         |
| tomli_loads          | 2.12 sec                                                   | 2.26 sec: 1.07x slower                                                        |
| Geometric mean       | (ref)                                                      | 1.00x faster                                                                  |

Benchmark hidden because not significant (2): json_loads, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-dd7732d |
|------------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 10.6 ms: 1.02x faster                                                         |
| python_startup_no_site | 7.11 ms                                                    | 8.97 ms: 1.26x slower                                                         |
| Geometric mean         | (ref)                                                      | 1.11x slower                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-dd7732d |
|----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| genshi_xml     | 51.6 ms                                                    | 51.0 ms: 1.01x faster                                                         |
| genshi_text    | 23.7 ms                                                    | 23.5 ms: 1.01x faster                                                         |
| mako           | 11.2 ms                                                    | 11.2 ms: 1.00x faster                                                         |
| Geometric mean | (ref)                                                      | 1.01x faster                                                                  |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-dd7732d |
|----------------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 114 us: 1.45x faster                                                          |
| pylint                     | 317 ms                                                     | 278 ms: 1.14x faster                                                          |
| gc_traversal               | 3.98 ms                                                    | 3.59 ms: 1.11x faster                                                         |
| richards_super             | 57.4 ms                                                    | 52.5 ms: 1.09x faster                                                         |
| richards                   | 50.9 ms                                                    | 46.8 ms: 1.09x faster                                                         |
| async_tree_none            | 378 ms                                                     | 351 ms: 1.08x faster                                                          |
| deepcopy_memo              | 39.7 us                                                    | 37.6 us: 1.06x faster                                                         |
| deepcopy_reduce            | 3.35 us                                                    | 3.20 us: 1.05x faster                                                         |
| logging_silent             | 105 ns                                                     | 100 ns: 1.05x faster                                                          |
| deepcopy                   | 367 us                                                     | 352 us: 1.04x faster                                                          |
| crypto_pyaes               | 77.5 ms                                                    | 74.3 ms: 1.04x faster                                                         |
| create_gc_cycles           | 1.82 ms                                                    | 1.75 ms: 1.04x faster                                                         |
| pickle_list                | 5.11 us                                                    | 4.93 us: 1.04x faster                                                         |
| chameleon                  | 7.22 ms                                                    | 6.98 ms: 1.03x faster                                                         |
| regex_v8                   | 25.1 ms                                                    | 24.4 ms: 1.03x faster                                                         |
| sqlglot_transpile          | 1.63 ms                                                    | 1.59 ms: 1.03x faster                                                         |
| deltablue                  | 3.25 ms                                                    | 3.17 ms: 1.02x faster                                                         |
| 2to3                       | 274 ms                                                     | 268 ms: 1.02x faster                                                          |
| unpickle_list              | 5.34 us                                                    | 5.22 us: 1.02x faster                                                         |
| sqlglot_parse              | 1.32 ms                                                    | 1.29 ms: 1.02x faster                                                         |
| pprint_pformat             | 1.56 sec                                                   | 1.52 sec: 1.02x faster                                                        |
| pprint_safe_repr           | 758 ms                                                     | 742 ms: 1.02x faster                                                          |
| pickle_pure_python         | 305 us                                                     | 299 us: 1.02x faster                                                          |
| python_startup             | 10.8 ms                                                    | 10.6 ms: 1.02x faster                                                         |
| pickle_dict                | 34.8 us                                                    | 34.2 us: 1.02x faster                                                         |
| aiohttp                    | 1.18 ms                                                    | 1.16 ms: 1.02x faster                                                         |
| thrift                     | 823 us                                                     | 809 us: 1.02x faster                                                          |
| xml_etree_parse            | 162 ms                                                     | 159 ms: 1.02x faster                                                          |
| regex_compile              | 137 ms                                                     | 135 ms: 1.01x faster                                                          |
| genshi_xml                 | 51.6 ms                                                    | 51.0 ms: 1.01x faster                                                         |
| pycparser                  | 1.16 sec                                                   | 1.15 sec: 1.01x faster                                                        |
| hexiom                     | 6.30 ms                                                    | 6.23 ms: 1.01x faster                                                         |
| gunicorn                   | 1.28 ms                                                    | 1.27 ms: 1.01x faster                                                         |
| sympy_integrate            | 20.5 ms                                                    | 20.3 ms: 1.01x faster                                                         |
| docutils                   | 2.83 sec                                                   | 2.80 sec: 1.01x faster                                                        |
| xml_etree_iterparse        | 107 ms                                                     | 106 ms: 1.01x faster                                                          |
| sqlite_synth               | 2.99 us                                                    | 2.96 us: 1.01x faster                                                         |
| sqlglot_optimize           | 55.5 ms                                                    | 55.1 ms: 1.01x faster                                                         |
| asyncio_tcp                | 508 ms                                                     | 505 ms: 1.01x faster                                                          |
| genshi_text                | 23.7 ms                                                    | 23.5 ms: 1.01x faster                                                         |
| comprehensions             | 16.6 us                                                    | 16.5 us: 1.01x faster                                                         |
| sympy_expand               | 473 ms                                                     | 470 ms: 1.01x faster                                                          |
| sympy_sum                  | 156 ms                                                     | 155 ms: 1.00x faster                                                          |
| xml_etree_process          | 61.2 ms                                                    | 60.9 ms: 1.00x faster                                                         |
| asyncio_websockets         | 567 ms                                                     | 564 ms: 1.00x faster                                                          |
| mdp                        | 2.79 sec                                                   | 2.78 sec: 1.00x faster                                                        |
| mako                       | 11.2 ms                                                    | 11.2 ms: 1.00x faster                                                         |
| regex_dna                  | 221 ms                                                     | 221 ms: 1.00x faster                                                          |
| unpickle_pure_python       | 218 us                                                     | 219 us: 1.00x slower                                                          |
| go                         | 145 ms                                                     | 145 ms: 1.00x slower                                                          |
| dulwich_log                | 67.2 ms                                                    | 67.5 ms: 1.01x slower                                                         |
| sqlglot_normalize          | 110 ms                                                     | 111 ms: 1.01x slower                                                          |
| pyflate                    | 484 ms                                                     | 490 ms: 1.01x slower                                                          |
| html5lib                   | 67.2 ms                                                    | 68.2 ms: 1.01x slower                                                         |
| unpickle                   | 15.1 us                                                    | 15.3 us: 1.01x slower                                                         |
| xml_etree_generate         | 87.4 ms                                                    | 88.8 ms: 1.02x slower                                                         |
| logging_simple             | 5.74 us                                                    | 5.85 us: 1.02x slower                                                         |
| pickle                     | 11.5 us                                                    | 11.7 us: 1.02x slower                                                         |
| logging_format             | 6.47 us                                                    | 6.59 us: 1.02x slower                                                         |
| regex_effbot               | 3.67 ms                                                    | 3.75 ms: 1.02x slower                                                         |
| nqueens                    | 81.4 ms                                                    | 83.3 ms: 1.02x slower                                                         |
| coroutines                 | 23.2 ms                                                    | 23.7 ms: 1.02x slower                                                         |
| json                       | 5.31 ms                                                    | 5.43 ms: 1.02x slower                                                         |
| float                      | 78.9 ms                                                    | 81.3 ms: 1.03x slower                                                         |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 606 ms: 1.03x slower                                                          |
| telco                      | 8.41 ms                                                    | 8.68 ms: 1.03x slower                                                         |
| pidigits                   | 191 ms                                                     | 198 ms: 1.04x slower                                                          |
| fannkuch                   | 402 ms                                                     | 419 ms: 1.04x slower                                                          |
| raytrace                   | 267 ms                                                     | 280 ms: 1.05x slower                                                          |
| coverage                   | 93.1 ms                                                    | 98.1 ms: 1.05x slower                                                         |
| scimark_monte_carlo        | 69.2 ms                                                    | 73.6 ms: 1.06x slower                                                         |
| tomli_loads                | 2.12 sec                                                   | 2.26 sec: 1.07x slower                                                        |
| scimark_sor                | 127 ms                                                     | 136 ms: 1.07x slower                                                          |
| scimark_fft                | 392 ms                                                     | 429 ms: 1.09x slower                                                          |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 5.81 ms: 1.10x slower                                                         |
| pathlib                    | 17.3 ms                                                    | 19.3 ms: 1.11x slower                                                         |
| chaos                      | 61.3 ms                                                    | 68.9 ms: 1.12x slower                                                         |
| spectral_norm              | 116 ms                                                     | 142 ms: 1.23x slower                                                          |
| python_startup_no_site     | 7.11 ms                                                    | 8.97 ms: 1.26x slower                                                         |
| nbody                      | 88.3 ms                                                    | 127 ms: 1.43x slower                                                          |
| Geometric mean             | (ref)                                                      | 1.00x slower                                                                  |

Benchmark hidden because not significant (19): async_tree_io, async_tree_none_tg, mypy2, sympy_str, async_tree_memoization, async_tree_memoization_tg, async_generators, json_loads, bench_mp_pool, dask, meteor_contest, tornado_http, bench_thread_pool, generators, asyncio_tcp_ssl, json_dumps, async_tree_cpu_io_mixed, async_tree_io_tg, scimark_lu
Ignored benchmarks (4) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, django_template, djangocms, flaskblogging

# HPT report

- Reliability score: 76.18% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.98x