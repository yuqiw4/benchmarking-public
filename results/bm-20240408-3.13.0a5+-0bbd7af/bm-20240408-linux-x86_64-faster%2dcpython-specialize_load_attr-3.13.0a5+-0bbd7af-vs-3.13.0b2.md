# Results vs. 3.13.0b2

- fork: faster-cpython
- ref: specialize_load_attr
- machine: linux-x86_64
- commit hash: 0bbd7af
- commit date: 2024-04-08
- overall geometric mean: 1.02x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-0bbd7af |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 269 ms: 1.02x faster                                                             |
| chameleon      | 7.22 ms                                                    | 6.83 ms: 1.06x faster                                                            |
| html5lib       | 67.2 ms                                                    | 67.7 ms: 1.01x slower                                                            |
| Geometric mean | (ref)                                                      | 1.01x faster                                                                     |

Benchmark hidden because not significant (2): docutils, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-0bbd7af |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none            | 378 ms                                                     | 350 ms: 1.08x faster                                                             |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 605 ms: 1.03x slower                                                             |
| Geometric mean             | (ref)                                                      | 1.01x faster                                                                     |

Benchmark hidden because not significant (6): async_tree_io, async_tree_memoization, async_tree_cpu_io_mixed, async_tree_memoization_tg, async_tree_none_tg, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-0bbd7af |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| float          | 78.9 ms                                                    | 77.6 ms: 1.02x faster                                                            |
| nbody          | 88.3 ms                                                    | 87.9 ms: 1.00x faster                                                            |
| pidigits       | 191 ms                                                     | 197 ms: 1.03x slower                                                             |
| Geometric mean | (ref)                                                      | 1.00x slower                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-0bbd7af |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 137 ms                                                     | 134 ms: 1.02x faster                                                             |
| regex_v8       | 25.1 ms                                                    | 24.8 ms: 1.01x faster                                                            |
| regex_effbot   | 3.67 ms                                                    | 3.66 ms: 1.00x faster                                                            |
| regex_dna      | 221 ms                                                     | 227 ms: 1.03x slower                                                             |
| Geometric mean | (ref)                                                      | 1.00x faster                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-0bbd7af |
|----------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| unpickle_list        | 5.34 us                                                    | 5.01 us: 1.07x faster                                                            |
| pickle_pure_python   | 305 us                                                     | 298 us: 1.02x faster                                                             |
| json_dumps           | 10.7 ms                                                    | 10.5 ms: 1.02x faster                                                            |
| xml_etree_generate   | 87.4 ms                                                    | 88.0 ms: 1.01x slower                                                            |
| unpickle_pure_python | 218 us                                                     | 220 us: 1.01x slower                                                             |
| pickle_list          | 5.11 us                                                    | 5.19 us: 1.02x slower                                                            |
| pickle_dict          | 34.8 us                                                    | 36.4 us: 1.05x slower                                                            |
| pickle               | 11.5 us                                                    | 12.1 us: 1.05x slower                                                            |
| Geometric mean       | (ref)                                                      | 1.00x faster                                                                     |

Benchmark hidden because not significant (6): xml_etree_parse, xml_etree_iterparse, xml_etree_process, json_loads, unpickle, tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-0bbd7af |
|------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 10.5 ms: 1.02x faster                                                            |
| python_startup_no_site | 7.11 ms                                                    | 8.95 ms: 1.26x slower                                                            |
| Geometric mean         | (ref)                                                      | 1.11x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-0bbd7af |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako           | 11.2 ms                                                    | 10.7 ms: 1.05x faster                                                            |
| Geometric mean | (ref)                                                      | 1.02x faster                                                                     |

Benchmark hidden because not significant (2): genshi_text, genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-0bbd7af |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 112 us: 1.47x faster                                                             |
| pylint                     | 317 ms                                                     | 279 ms: 1.14x faster                                                             |
| deepcopy_memo              | 39.7 us                                                    | 36.4 us: 1.09x faster                                                            |
| async_tree_none            | 378 ms                                                     | 350 ms: 1.08x faster                                                             |
| richards                   | 50.9 ms                                                    | 47.1 ms: 1.08x faster                                                            |
| richards_super             | 57.4 ms                                                    | 53.1 ms: 1.08x faster                                                            |
| mdp                        | 2.79 sec                                                   | 2.59 sec: 1.08x faster                                                           |
| spectral_norm              | 116 ms                                                     | 109 ms: 1.07x faster                                                             |
| unpickle_list              | 5.34 us                                                    | 5.01 us: 1.07x faster                                                            |
| deepcopy_reduce            | 3.35 us                                                    | 3.16 us: 1.06x faster                                                            |
| gc_traversal               | 3.98 ms                                                    | 3.75 ms: 1.06x faster                                                            |
| scimark_fft                | 392 ms                                                     | 371 ms: 1.06x faster                                                             |
| chameleon                  | 7.22 ms                                                    | 6.83 ms: 1.06x faster                                                            |
| create_gc_cycles           | 1.82 ms                                                    | 1.72 ms: 1.05x faster                                                            |
| scimark_lu                 | 122 ms                                                     | 115 ms: 1.05x faster                                                             |
| deepcopy                   | 367 us                                                     | 350 us: 1.05x faster                                                             |
| mako                       | 11.2 ms                                                    | 10.7 ms: 1.05x faster                                                            |
| fannkuch                   | 402 ms                                                     | 383 ms: 1.05x faster                                                             |
| coroutines                 | 23.2 ms                                                    | 22.1 ms: 1.05x faster                                                            |
| logging_silent             | 105 ns                                                     | 101 ns: 1.04x faster                                                             |
| scimark_monte_carlo        | 69.2 ms                                                    | 66.4 ms: 1.04x faster                                                            |
| crypto_pyaes               | 77.5 ms                                                    | 74.6 ms: 1.04x faster                                                            |
| pprint_pformat             | 1.56 sec                                                   | 1.50 sec: 1.04x faster                                                           |
| pprint_safe_repr           | 758 ms                                                     | 732 ms: 1.04x faster                                                             |
| pyflate                    | 484 ms                                                     | 467 ms: 1.04x faster                                                             |
| scimark_sor                | 127 ms                                                     | 124 ms: 1.03x faster                                                             |
| raytrace                   | 267 ms                                                     | 259 ms: 1.03x faster                                                             |
| sqlite_synth               | 2.99 us                                                    | 2.92 us: 1.03x faster                                                            |
| logging_format             | 6.47 us                                                    | 6.31 us: 1.03x faster                                                            |
| sqlglot_parse              | 1.32 ms                                                    | 1.29 ms: 1.03x faster                                                            |
| python_startup             | 10.8 ms                                                    | 10.5 ms: 1.02x faster                                                            |
| chaos                      | 61.3 ms                                                    | 59.9 ms: 1.02x faster                                                            |
| go                         | 145 ms                                                     | 141 ms: 1.02x faster                                                             |
| pickle_pure_python         | 305 us                                                     | 298 us: 1.02x faster                                                             |
| sqlglot_transpile          | 1.63 ms                                                    | 1.60 ms: 1.02x faster                                                            |
| regex_compile              | 137 ms                                                     | 134 ms: 1.02x faster                                                             |
| deltablue                  | 3.25 ms                                                    | 3.19 ms: 1.02x faster                                                            |
| thrift                     | 823 us                                                     | 807 us: 1.02x faster                                                             |
| json_dumps                 | 10.7 ms                                                    | 10.5 ms: 1.02x faster                                                            |
| 2to3                       | 274 ms                                                     | 269 ms: 1.02x faster                                                             |
| float                      | 78.9 ms                                                    | 77.6 ms: 1.02x faster                                                            |
| logging_simple             | 5.74 us                                                    | 5.66 us: 1.01x faster                                                            |
| sympy_str                  | 282 ms                                                     | 278 ms: 1.01x faster                                                             |
| regex_v8                   | 25.1 ms                                                    | 24.8 ms: 1.01x faster                                                            |
| hexiom                     | 6.30 ms                                                    | 6.23 ms: 1.01x faster                                                            |
| sympy_expand               | 473 ms                                                     | 468 ms: 1.01x faster                                                             |
| nqueens                    | 81.4 ms                                                    | 80.6 ms: 1.01x faster                                                            |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 5.22 ms: 1.01x faster                                                            |
| aiohttp                    | 1.18 ms                                                    | 1.17 ms: 1.01x faster                                                            |
| sympy_integrate            | 20.5 ms                                                    | 20.4 ms: 1.01x faster                                                            |
| asyncio_tcp                | 508 ms                                                     | 505 ms: 1.01x faster                                                             |
| gunicorn                   | 1.28 ms                                                    | 1.27 ms: 1.01x faster                                                            |
| nbody                      | 88.3 ms                                                    | 87.9 ms: 1.00x faster                                                            |
| sqlglot_optimize           | 55.5 ms                                                    | 55.3 ms: 1.00x faster                                                            |
| regex_effbot               | 3.67 ms                                                    | 3.66 ms: 1.00x faster                                                            |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.84 sec: 1.00x faster                                                           |
| sqlglot_normalize          | 110 ms                                                     | 111 ms: 1.01x slower                                                             |
| comprehensions             | 16.6 us                                                    | 16.7 us: 1.01x slower                                                            |
| html5lib                   | 67.2 ms                                                    | 67.7 ms: 1.01x slower                                                            |
| xml_etree_generate         | 87.4 ms                                                    | 88.0 ms: 1.01x slower                                                            |
| unpickle_pure_python       | 218 us                                                     | 220 us: 1.01x slower                                                             |
| meteor_contest             | 110 ms                                                     | 111 ms: 1.01x slower                                                             |
| pickle_list                | 5.11 us                                                    | 5.19 us: 1.02x slower                                                            |
| json                       | 5.31 ms                                                    | 5.43 ms: 1.02x slower                                                            |
| regex_dna                  | 221 ms                                                     | 227 ms: 1.03x slower                                                             |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 605 ms: 1.03x slower                                                             |
| pidigits                   | 191 ms                                                     | 197 ms: 1.03x slower                                                             |
| coverage                   | 93.1 ms                                                    | 96.3 ms: 1.03x slower                                                            |
| telco                      | 8.41 ms                                                    | 8.80 ms: 1.05x slower                                                            |
| pickle_dict                | 34.8 us                                                    | 36.4 us: 1.05x slower                                                            |
| pickle                     | 11.5 us                                                    | 12.1 us: 1.05x slower                                                            |
| pathlib                    | 17.3 ms                                                    | 18.5 ms: 1.07x slower                                                            |
| python_startup_no_site     | 7.11 ms                                                    | 8.95 ms: 1.26x slower                                                            |
| Geometric mean             | (ref)                                                      | 1.02x faster                                                                     |

Benchmark hidden because not significant (26): async_tree_io, async_tree_memoization, xml_etree_parse, async_tree_cpu_io_mixed, xml_etree_iterparse, async_tree_memoization_tg, dask, xml_etree_process, async_tree_none_tg, genshi_text, mypy2, pycparser, genshi_xml, json_loads, docutils, tornado_http, unpickle, asyncio_websockets, bench_thread_pool, tomli_loads, generators, dulwich_log, async_tree_io_tg, async_generators, sympy_sum, bench_mp_pool
Ignored benchmarks (4) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, django_template, djangocms, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.98x