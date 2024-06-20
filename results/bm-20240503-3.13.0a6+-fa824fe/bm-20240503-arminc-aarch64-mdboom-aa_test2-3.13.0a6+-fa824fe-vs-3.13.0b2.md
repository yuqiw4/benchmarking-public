# Results vs. 3.13.0b2

- fork: mdboom
- ref: aa_test2
- machine: linux-aarch64
- commit hash: fa824fe
- commit date: 2024-05-03
- overall geometric mean: 1.00x faster
- HPT reliability: 94.31%
- HPT 99th percentile: 1.00x slower
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240503-arminc-aarch64-mdboom-aa_test2-3.13.0a6+-fa824fe |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------:|
| 2to3           | 305 ms                                                       | 302 ms: 1.01x faster                                         |
| chameleon      | 8.95 ms                                                      | 9.17 ms: 1.02x slower                                        |
| Geometric mean | (ref)                                                        | 1.00x slower                                                 |

Benchmark hidden because not significant (3): docutils, html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240503-arminc-aarch64-mdboom-aa_test2-3.13.0a6+-fa824fe |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------:|
| async_tree_io_tg           | 1.27 sec                                                     | 1.21 sec: 1.05x faster                                       |
| async_tree_cpu_io_mixed_tg | 763 ms                                                       | 785 ms: 1.03x slower                                         |
| Geometric mean             | (ref)                                                        | 1.00x slower                                                 |

Benchmark hidden because not significant (6): async_tree_none_tg, async_tree_cpu_io_mixed, async_tree_none, async_tree_memoization, async_tree_io, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240503-arminc-aarch64-mdboom-aa_test2-3.13.0a6+-fa824fe |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------:|
| nbody          | 114 ms                                                       | 111 ms: 1.03x faster                                         |
| pidigits       | 234 ms                                                       | 233 ms: 1.01x faster                                         |
| float          | 91.4 ms                                                      | 91.0 ms: 1.00x faster                                        |
| Geometric mean | (ref)                                                        | 1.01x faster                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240503-arminc-aarch64-mdboom-aa_test2-3.13.0a6+-fa824fe |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------:|
| regex_dna      | 259 ms                                                       | 249 ms: 1.04x faster                                         |
| regex_effbot   | 4.98 ms                                                      | 4.88 ms: 1.02x faster                                        |
| regex_compile  | 128 ms                                                       | 128 ms: 1.00x slower                                         |
| Geometric mean | (ref)                                                        | 1.01x faster                                                 |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240503-arminc-aarch64-mdboom-aa_test2-3.13.0a6+-fa824fe |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------------:|
| unpickle_list        | 6.52 us                                                      | 6.32 us: 1.03x faster                                        |
| tomli_loads          | 2.57 sec                                                     | 2.53 sec: 1.01x faster                                       |
| unpickle_pure_python | 251 us                                                       | 248 us: 1.01x faster                                         |
| json_loads           | 32.1 us                                                      | 32.2 us: 1.00x slower                                        |
| unpickle             | 19.8 us                                                      | 19.9 us: 1.01x slower                                        |
| xml_etree_iterparse  | 147 ms                                                       | 148 ms: 1.01x slower                                         |
| pickle_list          | 5.27 us                                                      | 5.36 us: 1.02x slower                                        |
| Geometric mean       | (ref)                                                        | 1.00x faster                                                 |

Benchmark hidden because not significant (7): xml_etree_parse, xml_etree_process, pickle_dict, json_dumps, xml_etree_generate, pickle, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240503-arminc-aarch64-mdboom-aa_test2-3.13.0a6+-fa824fe |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------------:|
| python_startup         | 13.0 ms                                                      | 12.5 ms: 1.04x faster                                        |
| python_startup_no_site | 8.60 ms                                                      | 8.35 ms: 1.03x faster                                        |
| Geometric mean         | (ref)                                                        | 1.04x faster                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240503-arminc-aarch64-mdboom-aa_test2-3.13.0a6+-fa824fe |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------:|
| genshi_text    | 27.4 ms                                                      | 27.8 ms: 1.01x slower                                        |
| Geometric mean | (ref)                                                        | 1.00x slower                                                 |

Benchmark hidden because not significant (3): django_template, mako, genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240503-arminc-aarch64-mdboom-aa_test2-3.13.0a6+-fa824fe |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------:|
| async_tree_io_tg           | 1.27 sec                                                     | 1.21 sec: 1.05x faster                                       |
| python_startup             | 13.0 ms                                                      | 12.5 ms: 1.04x faster                                        |
| scimark_lu                 | 141 ms                                                       | 136 ms: 1.04x faster                                         |
| asyncio_tcp                | 584 ms                                                       | 561 ms: 1.04x faster                                         |
| regex_dna                  | 259 ms                                                       | 249 ms: 1.04x faster                                         |
| gc_traversal               | 5.17 ms                                                      | 5.01 ms: 1.03x faster                                        |
| unpickle_list              | 6.52 us                                                      | 6.32 us: 1.03x faster                                        |
| python_startup_no_site     | 8.60 ms                                                      | 8.35 ms: 1.03x faster                                        |
| deepcopy_memo              | 50.8 us                                                      | 49.4 us: 1.03x faster                                        |
| create_gc_cycles           | 2.33 ms                                                      | 2.27 ms: 1.03x faster                                        |
| nbody                      | 114 ms                                                       | 111 ms: 1.03x faster                                         |
| dulwich_log                | 58.5 ms                                                      | 57.1 ms: 1.02x faster                                        |
| richards_super             | 62.3 ms                                                      | 61.0 ms: 1.02x faster                                        |
| thrift                     | 962 us                                                       | 942 us: 1.02x faster                                         |
| regex_effbot               | 4.98 ms                                                      | 4.88 ms: 1.02x faster                                        |
| logging_simple             | 7.21 us                                                      | 7.09 us: 1.02x faster                                        |
| crypto_pyaes               | 82.0 ms                                                      | 80.7 ms: 1.02x faster                                        |
| tomli_loads                | 2.57 sec                                                     | 2.53 sec: 1.01x faster                                       |
| unpickle_pure_python       | 251 us                                                       | 248 us: 1.01x faster                                         |
| logging_format             | 7.82 us                                                      | 7.76 us: 1.01x faster                                        |
| 2to3                       | 305 ms                                                       | 302 ms: 1.01x faster                                         |
| mdp                        | 3.33 sec                                                     | 3.31 sec: 1.01x faster                                       |
| pidigits                   | 234 ms                                                       | 233 ms: 1.01x faster                                         |
| float                      | 91.4 ms                                                      | 91.0 ms: 1.00x faster                                        |
| sqlglot_transpile          | 1.71 ms                                                      | 1.71 ms: 1.00x faster                                        |
| regex_compile              | 128 ms                                                       | 128 ms: 1.00x slower                                         |
| json_loads                 | 32.1 us                                                      | 32.2 us: 1.00x slower                                        |
| pprint_safe_repr           | 933 ms                                                       | 939 ms: 1.01x slower                                         |
| unpickle                   | 19.8 us                                                      | 19.9 us: 1.01x slower                                        |
| logging_silent             | 133 ns                                                       | 134 ns: 1.01x slower                                         |
| xml_etree_iterparse        | 147 ms                                                       | 148 ms: 1.01x slower                                         |
| sympy_integrate            | 20.9 ms                                                      | 21.1 ms: 1.01x slower                                        |
| fannkuch                   | 451 ms                                                       | 456 ms: 1.01x slower                                         |
| deepcopy_reduce            | 4.04 us                                                      | 4.08 us: 1.01x slower                                        |
| genshi_text                | 27.4 ms                                                      | 27.8 ms: 1.01x slower                                        |
| pickle_list                | 5.27 us                                                      | 5.36 us: 1.02x slower                                        |
| generators                 | 37.1 ms                                                      | 37.7 ms: 1.02x slower                                        |
| bench_mp_pool              | 7.03 ms                                                      | 7.14 ms: 1.02x slower                                        |
| chameleon                  | 8.95 ms                                                      | 9.17 ms: 1.02x slower                                        |
| async_tree_cpu_io_mixed_tg | 763 ms                                                       | 785 ms: 1.03x slower                                         |
| Geometric mean             | (ref)                                                        | 1.00x faster                                                 |

Benchmark hidden because not significant (60): sqlglot_parse, xml_etree_parse, sqlglot_normalize, sqlglot_optimize, django_template, async_generators, aiohttp, deepcopy, richards, sqlite_synth, nqueens, sympy_expand, scimark_sparse_mat_mult, xml_etree_process, dask, typing_runtime_protocols, async_tree_none_tg, go, spectral_norm, scimark_sor, pathlib, comprehensions, tornado_http, chaos, pprint_pformat, meteor_contest, html5lib, scimark_fft, sympy_str, coroutines, docutils, hexiom, pickle_dict, asyncio_tcp_ssl, json_dumps, async_tree_cpu_io_mixed, raytrace, deltablue, asyncio_websockets, regex_v8, mako, pycparser, pyflate, scimark_monte_carlo, bench_thread_pool, genshi_xml, async_tree_none, xml_etree_generate, pickle, coverage, sympy_sum, telco, flaskblogging, async_tree_memoization, async_tree_io, pickle_pure_python, json, pylint, gunicorn, async_tree_memoization_tg
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, mypy2

# HPT report

- Reliability score: 94.31% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 0.98x