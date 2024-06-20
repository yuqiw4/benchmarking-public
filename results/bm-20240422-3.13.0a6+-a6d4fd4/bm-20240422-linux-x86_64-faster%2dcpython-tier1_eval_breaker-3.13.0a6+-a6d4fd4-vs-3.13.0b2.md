# Results vs. 3.13.0b2

- fork: faster-cpython
- ref: tier1_eval_breaker
- machine: linux-x86_64
- commit hash: a6d4fd4
- commit date: 2024-04-22
- overall geometric mean: 1.00x faster
- HPT reliability: 92.62%
- HPT 99th percentile: 1.00x slower
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240422-linux-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:----------------------------------------------------------:|:------------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 273 ms: 1.00x faster                                                           |
| chameleon      | 7.22 ms                                                    | 7.17 ms: 1.01x faster                                                          |
| html5lib       | 67.2 ms                                                    | 66.5 ms: 1.01x faster                                                          |
| Geometric mean | (ref)                                                      | 1.00x faster                                                                   |

Benchmark hidden because not significant (2): docutils, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240422-linux-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------------------|:----------------------------------------------------------:|:------------------------------------------------------------------------------:|
| async_tree_none            | 378 ms                                                     | 356 ms: 1.06x faster                                                           |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 605 ms: 1.03x slower                                                           |
| Geometric mean             | (ref)                                                      | 1.00x faster                                                                   |

Benchmark hidden because not significant (6): async_tree_io, async_tree_memoization_tg, async_tree_cpu_io_mixed, async_tree_none_tg, async_tree_io_tg, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240422-linux-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:----------------------------------------------------------:|:------------------------------------------------------------------------------:|
| pidigits       | 191 ms                                                     | 193 ms: 1.01x slower                                                           |
| nbody          | 88.3 ms                                                    | 92.6 ms: 1.05x slower                                                          |
| Geometric mean | (ref)                                                      | 1.02x slower                                                                   |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240422-linux-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:----------------------------------------------------------:|:------------------------------------------------------------------------------:|
| regex_compile  | 137 ms                                                     | 137 ms: 1.00x slower                                                           |
| regex_v8       | 25.1 ms                                                    | 25.8 ms: 1.03x slower                                                          |
| regex_effbot   | 3.67 ms                                                    | 3.83 ms: 1.04x slower                                                          |
| regex_dna      | 221 ms                                                     | 233 ms: 1.05x slower                                                           |
| Geometric mean | (ref)                                                      | 1.03x slower                                                                   |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240422-linux-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------------|:----------------------------------------------------------:|:------------------------------------------------------------------------------:|
| json_loads           | 28.9 us                                                    | 27.5 us: 1.05x faster                                                          |
| xml_etree_parse      | 162 ms                                                     | 158 ms: 1.02x faster                                                           |
| json_dumps           | 10.7 ms                                                    | 10.5 ms: 1.02x faster                                                          |
| pickle_pure_python   | 305 us                                                     | 308 us: 1.01x slower                                                           |
| xml_etree_generate   | 87.4 ms                                                    | 88.6 ms: 1.01x slower                                                          |
| pickle_dict          | 34.8 us                                                    | 35.4 us: 1.02x slower                                                          |
| pickle_list          | 5.11 us                                                    | 5.21 us: 1.02x slower                                                          |
| unpickle_pure_python | 218 us                                                     | 224 us: 1.03x slower                                                           |
| pickle               | 11.5 us                                                    | 11.9 us: 1.03x slower                                                          |
| tomli_loads          | 2.12 sec                                                   | 2.20 sec: 1.04x slower                                                         |
| Geometric mean       | (ref)                                                      | 1.00x slower                                                                   |

Benchmark hidden because not significant (4): xml_etree_iterparse, unpickle, xml_etree_process, unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240422-linux-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:----------------------------------------------------------:|:------------------------------------------------------------------------------:|
| python_startup | 10.8 ms                                                    | 10.5 ms: 1.02x faster                                                          |
| Geometric mean | (ref)                                                      | 1.01x faster                                                                   |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240422-linux-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|-----------------|:----------------------------------------------------------:|:------------------------------------------------------------------------------:|
| genshi_xml      | 51.6 ms                                                    | 52.2 ms: 1.01x slower                                                          |
| genshi_text     | 23.7 ms                                                    | 24.0 ms: 1.02x slower                                                          |
| django_template | 34.8 ms                                                    | 35.6 ms: 1.02x slower                                                          |
| Geometric mean  | (ref)                                                      | 1.01x slower                                                                   |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240422-linux-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------------------|:----------------------------------------------------------:|:------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 116 us: 1.42x faster                                                           |
| richards                   | 50.9 ms                                                    | 46.9 ms: 1.09x faster                                                          |
| richards_super             | 57.4 ms                                                    | 53.3 ms: 1.08x faster                                                          |
| async_tree_none            | 378 ms                                                     | 356 ms: 1.06x faster                                                           |
| deepcopy_reduce            | 3.35 us                                                    | 3.18 us: 1.05x faster                                                          |
| json_loads                 | 28.9 us                                                    | 27.5 us: 1.05x faster                                                          |
| scimark_lu                 | 122 ms                                                     | 117 ms: 1.04x faster                                                           |
| scimark_sor                | 127 ms                                                     | 123 ms: 1.04x faster                                                           |
| scimark_fft                | 392 ms                                                     | 379 ms: 1.03x faster                                                           |
| coroutines                 | 23.2 ms                                                    | 22.5 ms: 1.03x faster                                                          |
| logging_silent             | 105 ns                                                     | 102 ns: 1.03x faster                                                           |
| thrift                     | 823 us                                                     | 804 us: 1.02x faster                                                           |
| xml_etree_parse            | 162 ms                                                     | 158 ms: 1.02x faster                                                           |
| create_gc_cycles           | 1.82 ms                                                    | 1.77 ms: 1.02x faster                                                          |
| python_startup             | 10.8 ms                                                    | 10.5 ms: 1.02x faster                                                          |
| json                       | 5.31 ms                                                    | 5.20 ms: 1.02x faster                                                          |
| sqlglot_parse              | 1.32 ms                                                    | 1.29 ms: 1.02x faster                                                          |
| sqlglot_transpile          | 1.63 ms                                                    | 1.60 ms: 1.02x faster                                                          |
| json_dumps                 | 10.7 ms                                                    | 10.5 ms: 1.02x faster                                                          |
| deepcopy                   | 367 us                                                     | 360 us: 1.02x faster                                                           |
| raytrace                   | 267 ms                                                     | 263 ms: 1.02x faster                                                           |
| crypto_pyaes               | 77.5 ms                                                    | 76.3 ms: 1.01x faster                                                          |
| html5lib                   | 67.2 ms                                                    | 66.5 ms: 1.01x faster                                                          |
| go                         | 145 ms                                                     | 143 ms: 1.01x faster                                                           |
| deepcopy_memo              | 39.7 us                                                    | 39.4 us: 1.01x faster                                                          |
| asyncio_websockets         | 567 ms                                                     | 563 ms: 1.01x faster                                                           |
| chameleon                  | 7.22 ms                                                    | 7.17 ms: 1.01x faster                                                          |
| gunicorn                   | 1.28 ms                                                    | 1.27 ms: 1.01x faster                                                          |
| sympy_integrate            | 20.5 ms                                                    | 20.4 ms: 1.01x faster                                                          |
| chaos                      | 61.3 ms                                                    | 61.0 ms: 1.01x faster                                                          |
| dulwich_log                | 67.2 ms                                                    | 66.8 ms: 1.00x faster                                                          |
| 2to3                       | 274 ms                                                     | 273 ms: 1.00x faster                                                           |
| regex_compile              | 137 ms                                                     | 137 ms: 1.00x slower                                                           |
| bench_thread_pool          | 834 us                                                     | 836 us: 1.00x slower                                                           |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.85 sec: 1.00x slower                                                         |
| sympy_sum                  | 156 ms                                                     | 156 ms: 1.00x slower                                                           |
| asyncio_tcp                | 508 ms                                                     | 511 ms: 1.01x slower                                                           |
| nqueens                    | 81.4 ms                                                    | 81.9 ms: 1.01x slower                                                          |
| pickle_pure_python         | 305 us                                                     | 308 us: 1.01x slower                                                           |
| pidigits                   | 191 ms                                                     | 193 ms: 1.01x slower                                                           |
| spectral_norm              | 116 ms                                                     | 117 ms: 1.01x slower                                                           |
| sympy_expand               | 473 ms                                                     | 477 ms: 1.01x slower                                                           |
| genshi_xml                 | 51.6 ms                                                    | 52.2 ms: 1.01x slower                                                          |
| fannkuch                   | 402 ms                                                     | 406 ms: 1.01x slower                                                           |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 5.33 ms: 1.01x slower                                                          |
| xml_etree_generate         | 87.4 ms                                                    | 88.6 ms: 1.01x slower                                                          |
| genshi_text                | 23.7 ms                                                    | 24.0 ms: 1.02x slower                                                          |
| logging_simple             | 5.74 us                                                    | 5.84 us: 1.02x slower                                                          |
| pickle_dict                | 34.8 us                                                    | 35.4 us: 1.02x slower                                                          |
| async_generators           | 442 ms                                                     | 451 ms: 1.02x slower                                                           |
| meteor_contest             | 110 ms                                                     | 112 ms: 1.02x slower                                                           |
| pickle_list                | 5.11 us                                                    | 5.21 us: 1.02x slower                                                          |
| pyflate                    | 484 ms                                                     | 495 ms: 1.02x slower                                                           |
| generators                 | 29.6 ms                                                    | 30.3 ms: 1.02x slower                                                          |
| django_template            | 34.8 ms                                                    | 35.6 ms: 1.02x slower                                                          |
| hexiom                     | 6.30 ms                                                    | 6.45 ms: 1.02x slower                                                          |
| unpickle_pure_python       | 218 us                                                     | 224 us: 1.03x slower                                                           |
| deltablue                  | 3.25 ms                                                    | 3.34 ms: 1.03x slower                                                          |
| pathlib                    | 17.3 ms                                                    | 17.8 ms: 1.03x slower                                                          |
| telco                      | 8.41 ms                                                    | 8.65 ms: 1.03x slower                                                          |
| regex_v8                   | 25.1 ms                                                    | 25.8 ms: 1.03x slower                                                          |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 605 ms: 1.03x slower                                                           |
| pickle                     | 11.5 us                                                    | 11.9 us: 1.03x slower                                                          |
| tomli_loads                | 2.12 sec                                                   | 2.20 sec: 1.04x slower                                                         |
| comprehensions             | 16.6 us                                                    | 17.3 us: 1.04x slower                                                          |
| regex_effbot               | 3.67 ms                                                    | 3.83 ms: 1.04x slower                                                          |
| nbody                      | 88.3 ms                                                    | 92.6 ms: 1.05x slower                                                          |
| pycparser                  | 1.16 sec                                                   | 1.22 sec: 1.05x slower                                                         |
| regex_dna                  | 221 ms                                                     | 233 ms: 1.05x slower                                                           |
| coverage                   | 93.1 ms                                                    | 98.8 ms: 1.06x slower                                                          |
| Geometric mean             | (ref)                                                      | 1.00x faster                                                                   |

Benchmark hidden because not significant (31): async_tree_io, async_tree_memoization_tg, sqlite_synth, aiohttp, scimark_monte_carlo, async_tree_cpu_io_mixed, xml_etree_iterparse, async_tree_none_tg, bench_mp_pool, docutils, mypy2, unpickle, float, xml_etree_process, gc_traversal, python_startup_no_site, tornado_http, sqlglot_normalize, sqlglot_optimize, mdp, unpickle_list, pprint_safe_repr, sympy_str, logging_format, mako, pprint_pformat, dask, djangocms, pylint, async_tree_io_tg, async_tree_memoization
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 92.62% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 0.98x