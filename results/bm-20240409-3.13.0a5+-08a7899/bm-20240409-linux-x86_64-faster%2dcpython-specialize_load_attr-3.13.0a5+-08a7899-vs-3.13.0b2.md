# Results vs. 3.13.0b2

- fork: faster-cpython
- ref: specialize_load_attr
- machine: linux-x86_64
- commit hash: 08a7899
- commit date: 2024-04-09
- overall geometric mean: 1.01x faster
- HPT reliability: 99.88%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240409-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-08a7899 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 270 ms: 1.01x faster                                                             |
| chameleon      | 7.22 ms                                                    | 6.81 ms: 1.06x faster                                                            |
| docutils       | 2.83 sec                                                   | 2.81 sec: 1.01x faster                                                           |
| Geometric mean | (ref)                                                      | 1.02x faster                                                                     |

Benchmark hidden because not significant (2): html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240409-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-08a7899 |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none            | 378 ms                                                     | 351 ms: 1.08x faster                                                             |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 603 ms: 1.03x slower                                                             |
| Geometric mean             | (ref)                                                      | 1.01x faster                                                                     |

Benchmark hidden because not significant (6): async_tree_io, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg, async_tree_cpu_io_mixed, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240409-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-08a7899 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pidigits       | 191 ms                                                     | 190 ms: 1.01x faster                                                             |
| float          | 78.9 ms                                                    | 78.5 ms: 1.01x faster                                                            |
| nbody          | 88.3 ms                                                    | 88.8 ms: 1.01x slower                                                            |
| Geometric mean | (ref)                                                      | 1.00x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240409-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-08a7899 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 137 ms                                                     | 134 ms: 1.02x faster                                                             |
| regex_effbot   | 3.67 ms                                                    | 3.69 ms: 1.00x slower                                                            |
| regex_dna      | 221 ms                                                     | 225 ms: 1.02x slower                                                             |
| regex_v8       | 25.1 ms                                                    | 25.9 ms: 1.03x slower                                                            |
| Geometric mean | (ref)                                                      | 1.01x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240409-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-08a7899 |
|----------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_list          | 5.11 us                                                    | 5.00 us: 1.02x faster                                                            |
| pickle_pure_python   | 305 us                                                     | 299 us: 1.02x faster                                                             |
| json_dumps           | 10.7 ms                                                    | 10.5 ms: 1.02x faster                                                            |
| xml_etree_process    | 61.2 ms                                                    | 60.8 ms: 1.01x faster                                                            |
| unpickle             | 15.1 us                                                    | 15.2 us: 1.01x slower                                                            |
| pickle_dict          | 34.8 us                                                    | 35.0 us: 1.01x slower                                                            |
| xml_etree_generate   | 87.4 ms                                                    | 88.0 ms: 1.01x slower                                                            |
| unpickle_pure_python | 218 us                                                     | 220 us: 1.01x slower                                                             |
| pickle               | 11.5 us                                                    | 11.9 us: 1.03x slower                                                            |
| Geometric mean       | (ref)                                                      | 1.00x faster                                                                     |

Benchmark hidden because not significant (5): xml_etree_parse, json_loads, tomli_loads, unpickle_list, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240409-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-08a7899 |
|------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 10.6 ms: 1.02x faster                                                            |
| python_startup_no_site | 7.11 ms                                                    | 9.00 ms: 1.27x slower                                                            |
| Geometric mean         | (ref)                                                      | 1.11x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240409-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-08a7899 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako           | 11.2 ms                                                    | 10.8 ms: 1.04x faster                                                            |
| genshi_text    | 23.7 ms                                                    | 23.3 ms: 1.02x faster                                                            |
| Geometric mean | (ref)                                                      | 1.02x faster                                                                     |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240409-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-08a7899 |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 114 us: 1.44x faster                                                             |
| pylint                     | 317 ms                                                     | 278 ms: 1.14x faster                                                             |
| richards                   | 50.9 ms                                                    | 46.7 ms: 1.09x faster                                                            |
| richards_super             | 57.4 ms                                                    | 52.9 ms: 1.09x faster                                                            |
| async_tree_none            | 378 ms                                                     | 351 ms: 1.08x faster                                                             |
| scimark_fft                | 392 ms                                                     | 365 ms: 1.08x faster                                                             |
| deepcopy_memo              | 39.7 us                                                    | 37.2 us: 1.07x faster                                                            |
| gc_traversal               | 3.98 ms                                                    | 3.74 ms: 1.06x faster                                                            |
| chameleon                  | 7.22 ms                                                    | 6.81 ms: 1.06x faster                                                            |
| spectral_norm              | 116 ms                                                     | 110 ms: 1.06x faster                                                             |
| scimark_lu                 | 122 ms                                                     | 115 ms: 1.06x faster                                                             |
| deepcopy_reduce            | 3.35 us                                                    | 3.17 us: 1.06x faster                                                            |
| create_gc_cycles           | 1.82 ms                                                    | 1.73 ms: 1.05x faster                                                            |
| logging_silent             | 105 ns                                                     | 99.8 ns: 1.05x faster                                                            |
| mako                       | 11.2 ms                                                    | 10.8 ms: 1.04x faster                                                            |
| scimark_sor                | 127 ms                                                     | 123 ms: 1.04x faster                                                             |
| coroutines                 | 23.2 ms                                                    | 22.4 ms: 1.04x faster                                                            |
| deepcopy                   | 367 us                                                     | 355 us: 1.03x faster                                                             |
| scimark_monte_carlo        | 69.2 ms                                                    | 66.9 ms: 1.03x faster                                                            |
| logging_format             | 6.47 us                                                    | 6.28 us: 1.03x faster                                                            |
| sqlglot_transpile          | 1.63 ms                                                    | 1.59 ms: 1.03x faster                                                            |
| sqlglot_parse              | 1.32 ms                                                    | 1.28 ms: 1.03x faster                                                            |
| chaos                      | 61.3 ms                                                    | 60.0 ms: 1.02x faster                                                            |
| deltablue                  | 3.25 ms                                                    | 3.18 ms: 1.02x faster                                                            |
| pickle_list                | 5.11 us                                                    | 5.00 us: 1.02x faster                                                            |
| crypto_pyaes               | 77.5 ms                                                    | 75.9 ms: 1.02x faster                                                            |
| pickle_pure_python         | 305 us                                                     | 299 us: 1.02x faster                                                             |
| json_dumps                 | 10.7 ms                                                    | 10.5 ms: 1.02x faster                                                            |
| regex_compile              | 137 ms                                                     | 134 ms: 1.02x faster                                                             |
| python_startup             | 10.8 ms                                                    | 10.6 ms: 1.02x faster                                                            |
| logging_simple             | 5.74 us                                                    | 5.64 us: 1.02x faster                                                            |
| genshi_text                | 23.7 ms                                                    | 23.3 ms: 1.02x faster                                                            |
| go                         | 145 ms                                                     | 142 ms: 1.02x faster                                                             |
| fannkuch                   | 402 ms                                                     | 395 ms: 1.02x faster                                                             |
| sqlite_synth               | 2.99 us                                                    | 2.94 us: 1.02x faster                                                            |
| 2to3                       | 274 ms                                                     | 270 ms: 1.01x faster                                                             |
| pyflate                    | 484 ms                                                     | 477 ms: 1.01x faster                                                             |
| sympy_expand               | 473 ms                                                     | 467 ms: 1.01x faster                                                             |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 5.21 ms: 1.01x faster                                                            |
| raytrace                   | 267 ms                                                     | 264 ms: 1.01x faster                                                             |
| sympy_str                  | 282 ms                                                     | 279 ms: 1.01x faster                                                             |
| generators                 | 29.6 ms                                                    | 29.3 ms: 1.01x faster                                                            |
| pidigits                   | 191 ms                                                     | 190 ms: 1.01x faster                                                             |
| pprint_pformat             | 1.56 sec                                                   | 1.54 sec: 1.01x faster                                                           |
| gunicorn                   | 1.28 ms                                                    | 1.27 ms: 1.01x faster                                                            |
| thrift                     | 823 us                                                     | 816 us: 1.01x faster                                                             |
| aiohttp                    | 1.18 ms                                                    | 1.17 ms: 1.01x faster                                                            |
| xml_etree_process          | 61.2 ms                                                    | 60.8 ms: 1.01x faster                                                            |
| sqlglot_optimize           | 55.5 ms                                                    | 55.2 ms: 1.01x faster                                                            |
| hexiom                     | 6.30 ms                                                    | 6.26 ms: 1.01x faster                                                            |
| pprint_safe_repr           | 758 ms                                                     | 754 ms: 1.01x faster                                                             |
| float                      | 78.9 ms                                                    | 78.5 ms: 1.01x faster                                                            |
| docutils                   | 2.83 sec                                                   | 2.81 sec: 1.01x faster                                                           |
| sympy_integrate            | 20.5 ms                                                    | 20.4 ms: 1.00x faster                                                            |
| mdp                        | 2.79 sec                                                   | 2.79 sec: 1.00x slower                                                           |
| regex_effbot               | 3.67 ms                                                    | 3.69 ms: 1.00x slower                                                            |
| unpickle                   | 15.1 us                                                    | 15.2 us: 1.01x slower                                                            |
| nbody                      | 88.3 ms                                                    | 88.8 ms: 1.01x slower                                                            |
| pickle_dict                | 34.8 us                                                    | 35.0 us: 1.01x slower                                                            |
| meteor_contest             | 110 ms                                                     | 110 ms: 1.01x slower                                                             |
| sqlglot_normalize          | 110 ms                                                     | 111 ms: 1.01x slower                                                             |
| xml_etree_generate         | 87.4 ms                                                    | 88.0 ms: 1.01x slower                                                            |
| unpickle_pure_python       | 218 us                                                     | 220 us: 1.01x slower                                                             |
| async_generators           | 442 ms                                                     | 447 ms: 1.01x slower                                                             |
| telco                      | 8.41 ms                                                    | 8.52 ms: 1.01x slower                                                            |
| comprehensions             | 16.6 us                                                    | 16.8 us: 1.01x slower                                                            |
| regex_dna                  | 221 ms                                                     | 225 ms: 1.02x slower                                                             |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 603 ms: 1.03x slower                                                             |
| pycparser                  | 1.16 sec                                                   | 1.20 sec: 1.03x slower                                                           |
| regex_v8                   | 25.1 ms                                                    | 25.9 ms: 1.03x slower                                                            |
| pickle                     | 11.5 us                                                    | 11.9 us: 1.03x slower                                                            |
| coverage                   | 93.1 ms                                                    | 98.2 ms: 1.05x slower                                                            |
| pathlib                    | 17.3 ms                                                    | 18.8 ms: 1.08x slower                                                            |
| python_startup_no_site     | 7.11 ms                                                    | 9.00 ms: 1.27x slower                                                            |
| Geometric mean             | (ref)                                                      | 1.01x faster                                                                     |

Benchmark hidden because not significant (25): async_tree_io, async_tree_io_tg, xml_etree_parse, async_tree_memoization_tg, async_tree_none_tg, async_tree_cpu_io_mixed, json_loads, async_tree_memoization, dask, mypy2, tomli_loads, bench_mp_pool, asyncio_tcp, asyncio_websockets, dulwich_log, html5lib, asyncio_tcp_ssl, unpickle_list, tornado_http, bench_thread_pool, genshi_xml, nqueens, sympy_sum, xml_etree_iterparse, json
Ignored benchmarks (4) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, django_template, djangocms, flaskblogging

# HPT report

- Reliability score: 99.88% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.98x