# Results vs. 3.13.0b2

- fork: faster-cpython
- ref: specialize_binary_op
- machine: linux-x86_64
- commit hash: 23cf5de
- commit date: 2024-04-04
- overall geometric mean: 1.00x slower
- HPT reliability: 61.53%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-23cf5de |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 268 ms: 1.02x faster                                                             |
| chameleon      | 7.22 ms                                                    | 7.00 ms: 1.03x faster                                                            |
| docutils       | 2.83 sec                                                   | 2.79 sec: 1.01x faster                                                           |
| html5lib       | 67.2 ms                                                    | 68.0 ms: 1.01x slower                                                            |
| Geometric mean | (ref)                                                      | 1.01x faster                                                                     |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-23cf5de |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none            | 378 ms                                                     | 352 ms: 1.08x faster                                                             |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 601 ms: 1.02x slower                                                             |
| Geometric mean             | (ref)                                                      | 1.01x faster                                                                     |

Benchmark hidden because not significant (6): async_tree_io, async_tree_io_tg, async_tree_none_tg, async_tree_memoization_tg, async_tree_cpu_io_mixed, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-23cf5de |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| float          | 78.9 ms                                                    | 81.7 ms: 1.04x slower                                                            |
| pidigits       | 191 ms                                                     | 199 ms: 1.04x slower                                                             |
| nbody          | 88.3 ms                                                    | 118 ms: 1.34x slower                                                             |
| Geometric mean | (ref)                                                      | 1.13x slower                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-23cf5de |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_effbot   | 3.67 ms                                                    | 3.62 ms: 1.01x faster                                                            |
| regex_v8       | 25.1 ms                                                    | 24.8 ms: 1.01x faster                                                            |
| regex_compile  | 137 ms                                                     | 135 ms: 1.01x faster                                                             |
| regex_dna      | 221 ms                                                     | 220 ms: 1.01x faster                                                             |
| Geometric mean | (ref)                                                      | 1.01x faster                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark          | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-23cf5de |
|--------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_pure_python | 305 us                                                     | 299 us: 1.02x faster                                                             |
| unpickle_list      | 5.34 us                                                    | 5.24 us: 1.02x faster                                                            |
| xml_etree_process  | 61.2 ms                                                    | 60.2 ms: 1.02x faster                                                            |
| pickle_list        | 5.11 us                                                    | 5.04 us: 1.01x faster                                                            |
| pickle_dict        | 34.8 us                                                    | 34.3 us: 1.01x faster                                                            |
| json_loads         | 28.9 us                                                    | 28.7 us: 1.01x faster                                                            |
| unpickle           | 15.1 us                                                    | 15.2 us: 1.01x slower                                                            |
| pickle             | 11.5 us                                                    | 11.6 us: 1.01x slower                                                            |
| tomli_loads        | 2.12 sec                                                   | 2.30 sec: 1.08x slower                                                           |
| Geometric mean     | (ref)                                                      | 1.00x faster                                                                     |

Benchmark hidden because not significant (5): xml_etree_parse, json_dumps, xml_etree_generate, xml_etree_iterparse, unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-23cf5de |
|------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 10.6 ms: 1.02x faster                                                            |
| python_startup_no_site | 7.11 ms                                                    | 8.99 ms: 1.27x slower                                                            |
| Geometric mean         | (ref)                                                      | 1.12x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-23cf5de |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako           | 11.2 ms                                                    | 11.0 ms: 1.02x faster                                                            |
| Geometric mean | (ref)                                                      | 1.01x faster                                                                     |

Benchmark hidden because not significant (2): genshi_xml, genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-23cf5de |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 114 us: 1.45x faster                                                             |
| pylint                     | 317 ms                                                     | 278 ms: 1.14x faster                                                             |
| richards                   | 50.9 ms                                                    | 47.0 ms: 1.08x faster                                                            |
| richards_super             | 57.4 ms                                                    | 53.1 ms: 1.08x faster                                                            |
| async_tree_none            | 378 ms                                                     | 352 ms: 1.08x faster                                                             |
| gc_traversal               | 3.98 ms                                                    | 3.73 ms: 1.07x faster                                                            |
| crypto_pyaes               | 77.5 ms                                                    | 73.5 ms: 1.05x faster                                                            |
| create_gc_cycles           | 1.82 ms                                                    | 1.73 ms: 1.05x faster                                                            |
| logging_silent             | 105 ns                                                     | 100 ns: 1.05x faster                                                             |
| deepcopy_reduce            | 3.35 us                                                    | 3.21 us: 1.04x faster                                                            |
| deepcopy                   | 367 us                                                     | 353 us: 1.04x faster                                                             |
| deepcopy_memo              | 39.7 us                                                    | 38.3 us: 1.04x faster                                                            |
| pprint_safe_repr           | 758 ms                                                     | 734 ms: 1.03x faster                                                             |
| pprint_pformat             | 1.56 sec                                                   | 1.51 sec: 1.03x faster                                                           |
| chameleon                  | 7.22 ms                                                    | 7.00 ms: 1.03x faster                                                            |
| sqlglot_transpile          | 1.63 ms                                                    | 1.59 ms: 1.03x faster                                                            |
| sqlglot_parse              | 1.32 ms                                                    | 1.29 ms: 1.02x faster                                                            |
| pickle_pure_python         | 305 us                                                     | 299 us: 1.02x faster                                                             |
| 2to3                       | 274 ms                                                     | 268 ms: 1.02x faster                                                             |
| mako                       | 11.2 ms                                                    | 11.0 ms: 1.02x faster                                                            |
| unpickle_list              | 5.34 us                                                    | 5.24 us: 1.02x faster                                                            |
| sqlite_synth               | 2.99 us                                                    | 2.93 us: 1.02x faster                                                            |
| thrift                     | 823 us                                                     | 808 us: 1.02x faster                                                             |
| xml_etree_process          | 61.2 ms                                                    | 60.2 ms: 1.02x faster                                                            |
| python_startup             | 10.8 ms                                                    | 10.6 ms: 1.02x faster                                                            |
| regex_effbot               | 3.67 ms                                                    | 3.62 ms: 1.01x faster                                                            |
| regex_v8                   | 25.1 ms                                                    | 24.8 ms: 1.01x faster                                                            |
| pickle_list                | 5.11 us                                                    | 5.04 us: 1.01x faster                                                            |
| pickle_dict                | 34.8 us                                                    | 34.3 us: 1.01x faster                                                            |
| docutils                   | 2.83 sec                                                   | 2.79 sec: 1.01x faster                                                           |
| aiohttp                    | 1.18 ms                                                    | 1.17 ms: 1.01x faster                                                            |
| sqlglot_optimize           | 55.5 ms                                                    | 54.9 ms: 1.01x faster                                                            |
| gunicorn                   | 1.28 ms                                                    | 1.26 ms: 1.01x faster                                                            |
| sympy_str                  | 282 ms                                                     | 279 ms: 1.01x faster                                                             |
| regex_compile              | 137 ms                                                     | 135 ms: 1.01x faster                                                             |
| scimark_lu                 | 122 ms                                                     | 121 ms: 1.01x faster                                                             |
| sympy_integrate            | 20.5 ms                                                    | 20.3 ms: 1.01x faster                                                            |
| pyflate                    | 484 ms                                                     | 480 ms: 1.01x faster                                                             |
| comprehensions             | 16.6 us                                                    | 16.5 us: 1.01x faster                                                            |
| meteor_contest             | 110 ms                                                     | 109 ms: 1.01x faster                                                             |
| bench_thread_pool          | 834 us                                                     | 829 us: 1.01x faster                                                             |
| json_loads                 | 28.9 us                                                    | 28.7 us: 1.01x faster                                                            |
| regex_dna                  | 221 ms                                                     | 220 ms: 1.01x faster                                                             |
| asyncio_websockets         | 567 ms                                                     | 564 ms: 1.01x faster                                                             |
| asyncio_tcp                | 508 ms                                                     | 506 ms: 1.00x faster                                                             |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.84 sec: 1.00x slower                                                           |
| mdp                        | 2.79 sec                                                   | 2.80 sec: 1.01x slower                                                           |
| go                         | 145 ms                                                     | 146 ms: 1.01x slower                                                             |
| deltablue                  | 3.25 ms                                                    | 3.27 ms: 1.01x slower                                                            |
| unpickle                   | 15.1 us                                                    | 15.2 us: 1.01x slower                                                            |
| dulwich_log                | 67.2 ms                                                    | 67.8 ms: 1.01x slower                                                            |
| logging_format             | 6.47 us                                                    | 6.54 us: 1.01x slower                                                            |
| html5lib                   | 67.2 ms                                                    | 68.0 ms: 1.01x slower                                                            |
| pickle                     | 11.5 us                                                    | 11.6 us: 1.01x slower                                                            |
| hexiom                     | 6.30 ms                                                    | 6.39 ms: 1.01x slower                                                            |
| logging_simple             | 5.74 us                                                    | 5.83 us: 1.01x slower                                                            |
| telco                      | 8.41 ms                                                    | 8.56 ms: 1.02x slower                                                            |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 601 ms: 1.02x slower                                                             |
| fannkuch                   | 402 ms                                                     | 413 ms: 1.03x slower                                                             |
| coroutines                 | 23.2 ms                                                    | 23.9 ms: 1.03x slower                                                            |
| nqueens                    | 81.4 ms                                                    | 84.2 ms: 1.03x slower                                                            |
| float                      | 78.9 ms                                                    | 81.7 ms: 1.04x slower                                                            |
| pidigits                   | 191 ms                                                     | 199 ms: 1.04x slower                                                             |
| json                       | 5.31 ms                                                    | 5.51 ms: 1.04x slower                                                            |
| raytrace                   | 267 ms                                                     | 279 ms: 1.05x slower                                                             |
| coverage                   | 93.1 ms                                                    | 98.3 ms: 1.06x slower                                                            |
| scimark_monte_carlo        | 69.2 ms                                                    | 74.0 ms: 1.07x slower                                                            |
| scimark_sor                | 127 ms                                                     | 137 ms: 1.07x slower                                                             |
| tomli_loads                | 2.12 sec                                                   | 2.30 sec: 1.08x slower                                                           |
| pathlib                    | 17.3 ms                                                    | 18.8 ms: 1.09x slower                                                            |
| scimark_fft                | 392 ms                                                     | 428 ms: 1.09x slower                                                             |
| chaos                      | 61.3 ms                                                    | 68.6 ms: 1.12x slower                                                            |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 6.14 ms: 1.17x slower                                                            |
| spectral_norm              | 116 ms                                                     | 138 ms: 1.19x slower                                                             |
| python_startup_no_site     | 7.11 ms                                                    | 8.99 ms: 1.27x slower                                                            |
| nbody                      | 88.3 ms                                                    | 118 ms: 1.34x slower                                                             |
| Geometric mean             | (ref)                                                      | 1.00x slower                                                                     |

Benchmark hidden because not significant (23): async_tree_io, async_tree_io_tg, xml_etree_parse, async_tree_none_tg, async_tree_memoization_tg, sympy_expand, json_dumps, async_tree_cpu_io_mixed, async_tree_memoization, mypy2, bench_mp_pool, genshi_xml, sympy_sum, generators, async_generators, dask, pycparser, xml_etree_generate, genshi_text, sqlglot_normalize, xml_etree_iterparse, tornado_http, unpickle_pure_python
Ignored benchmarks (4) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, django_template, djangocms, flaskblogging

# HPT report

- Reliability score: 61.53% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.98x