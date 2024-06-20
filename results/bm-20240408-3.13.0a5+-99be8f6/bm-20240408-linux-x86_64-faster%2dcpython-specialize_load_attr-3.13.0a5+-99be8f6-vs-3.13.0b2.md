# Results vs. 3.13.0b2

- fork: faster-cpython
- ref: specialize_load_attr
- machine: linux-x86_64
- commit hash: 99be8f6
- commit date: 2024-04-08
- overall geometric mean: 1.01x faster
- HPT reliability: 99.65%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-99be8f6 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 271 ms: 1.01x faster                                                             |
| chameleon      | 7.22 ms                                                    | 6.87 ms: 1.05x faster                                                            |
| html5lib       | 67.2 ms                                                    | 67.8 ms: 1.01x slower                                                            |
| Geometric mean | (ref)                                                      | 1.01x faster                                                                     |

Benchmark hidden because not significant (2): docutils, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-99be8f6 |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none            | 378 ms                                                     | 350 ms: 1.08x faster                                                             |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 603 ms: 1.03x slower                                                             |
| Geometric mean             | (ref)                                                      | 1.02x faster                                                                     |

Benchmark hidden because not significant (6): async_tree_io, async_tree_io_tg, async_tree_none_tg, async_tree_memoization, async_tree_cpu_io_mixed, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-99be8f6 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| float          | 78.9 ms                                                    | 77.5 ms: 1.02x faster                                                            |
| pidigits       | 191 ms                                                     | 190 ms: 1.01x faster                                                             |
| nbody          | 88.3 ms                                                    | 89.4 ms: 1.01x slower                                                            |
| Geometric mean | (ref)                                                      | 1.00x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-99be8f6 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 137 ms                                                     | 135 ms: 1.01x faster                                                             |
| regex_v8       | 25.1 ms                                                    | 25.0 ms: 1.01x faster                                                            |
| regex_dna      | 221 ms                                                     | 225 ms: 1.02x slower                                                             |
| regex_effbot   | 3.67 ms                                                    | 3.85 ms: 1.05x slower                                                            |
| Geometric mean | (ref)                                                      | 1.01x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-99be8f6 |
|----------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_pure_python   | 305 us                                                     | 300 us: 1.02x faster                                                             |
| unpickle             | 15.1 us                                                    | 14.9 us: 1.02x faster                                                            |
| unpickle_list        | 5.34 us                                                    | 5.27 us: 1.01x faster                                                            |
| json_loads           | 28.9 us                                                    | 28.6 us: 1.01x faster                                                            |
| json_dumps           | 10.7 ms                                                    | 10.6 ms: 1.01x faster                                                            |
| xml_etree_process    | 61.2 ms                                                    | 60.9 ms: 1.00x faster                                                            |
| pickle_list          | 5.11 us                                                    | 5.14 us: 1.01x slower                                                            |
| pickle_dict          | 34.8 us                                                    | 35.1 us: 1.01x slower                                                            |
| xml_etree_generate   | 87.4 ms                                                    | 88.3 ms: 1.01x slower                                                            |
| tomli_loads          | 2.12 sec                                                   | 2.17 sec: 1.02x slower                                                           |
| pickle               | 11.5 us                                                    | 11.7 us: 1.02x slower                                                            |
| unpickle_pure_python | 218 us                                                     | 225 us: 1.03x slower                                                             |
| Geometric mean       | (ref)                                                      | 1.00x slower                                                                     |

Benchmark hidden because not significant (2): xml_etree_parse, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-99be8f6 |
|------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 10.6 ms: 1.02x faster                                                            |
| python_startup_no_site | 7.11 ms                                                    | 9.00 ms: 1.27x slower                                                            |
| Geometric mean         | (ref)                                                      | 1.12x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-99be8f6 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako           | 11.2 ms                                                    | 10.9 ms: 1.03x faster                                                            |
| genshi_xml     | 51.6 ms                                                    | 52.3 ms: 1.01x slower                                                            |
| genshi_text    | 23.7 ms                                                    | 24.2 ms: 1.02x slower                                                            |
| Geometric mean | (ref)                                                      | 1.00x slower                                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-99be8f6 |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 117 us: 1.41x faster                                                             |
| pylint                     | 317 ms                                                     | 279 ms: 1.14x faster                                                             |
| richards                   | 50.9 ms                                                    | 47.0 ms: 1.08x faster                                                            |
| richards_super             | 57.4 ms                                                    | 53.0 ms: 1.08x faster                                                            |
| async_tree_none            | 378 ms                                                     | 350 ms: 1.08x faster                                                             |
| deepcopy_memo              | 39.7 us                                                    | 36.9 us: 1.08x faster                                                            |
| scimark_lu                 | 122 ms                                                     | 116 ms: 1.05x faster                                                             |
| chameleon                  | 7.22 ms                                                    | 6.87 ms: 1.05x faster                                                            |
| deepcopy_reduce            | 3.35 us                                                    | 3.20 us: 1.05x faster                                                            |
| scimark_fft                | 392 ms                                                     | 375 ms: 1.05x faster                                                             |
| create_gc_cycles           | 1.82 ms                                                    | 1.74 ms: 1.05x faster                                                            |
| logging_silent             | 105 ns                                                     | 101 ns: 1.04x faster                                                             |
| deepcopy                   | 367 us                                                     | 353 us: 1.04x faster                                                             |
| scimark_sor                | 127 ms                                                     | 123 ms: 1.04x faster                                                             |
| crypto_pyaes               | 77.5 ms                                                    | 74.9 ms: 1.03x faster                                                            |
| mako                       | 11.2 ms                                                    | 10.9 ms: 1.03x faster                                                            |
| sqlglot_transpile          | 1.63 ms                                                    | 1.59 ms: 1.03x faster                                                            |
| logging_format             | 6.47 us                                                    | 6.29 us: 1.03x faster                                                            |
| sqlglot_parse              | 1.32 ms                                                    | 1.29 ms: 1.03x faster                                                            |
| fannkuch                   | 402 ms                                                     | 394 ms: 1.02x faster                                                             |
| sqlite_synth               | 2.99 us                                                    | 2.93 us: 1.02x faster                                                            |
| chaos                      | 61.3 ms                                                    | 60.1 ms: 1.02x faster                                                            |
| mdp                        | 2.79 sec                                                   | 2.73 sec: 1.02x faster                                                           |
| pickle_pure_python         | 305 us                                                     | 300 us: 1.02x faster                                                             |
| python_startup             | 10.8 ms                                                    | 10.6 ms: 1.02x faster                                                            |
| float                      | 78.9 ms                                                    | 77.5 ms: 1.02x faster                                                            |
| unpickle                   | 15.1 us                                                    | 14.9 us: 1.02x faster                                                            |
| unpickle_list              | 5.34 us                                                    | 5.27 us: 1.01x faster                                                            |
| regex_compile              | 137 ms                                                     | 135 ms: 1.01x faster                                                             |
| raytrace                   | 267 ms                                                     | 263 ms: 1.01x faster                                                             |
| sympy_str                  | 282 ms                                                     | 279 ms: 1.01x faster                                                             |
| pprint_pformat             | 1.56 sec                                                   | 1.54 sec: 1.01x faster                                                           |
| deltablue                  | 3.25 ms                                                    | 3.22 ms: 1.01x faster                                                            |
| pycparser                  | 1.16 sec                                                   | 1.15 sec: 1.01x faster                                                           |
| json_loads                 | 28.9 us                                                    | 28.6 us: 1.01x faster                                                            |
| asyncio_tcp                | 508 ms                                                     | 503 ms: 1.01x faster                                                             |
| gunicorn                   | 1.28 ms                                                    | 1.27 ms: 1.01x faster                                                            |
| 2to3                       | 274 ms                                                     | 271 ms: 1.01x faster                                                             |
| scimark_monte_carlo        | 69.2 ms                                                    | 68.5 ms: 1.01x faster                                                            |
| sympy_integrate            | 20.5 ms                                                    | 20.3 ms: 1.01x faster                                                            |
| pprint_safe_repr           | 758 ms                                                     | 751 ms: 1.01x faster                                                             |
| pidigits                   | 191 ms                                                     | 190 ms: 1.01x faster                                                             |
| json_dumps                 | 10.7 ms                                                    | 10.6 ms: 1.01x faster                                                            |
| spectral_norm              | 116 ms                                                     | 115 ms: 1.01x faster                                                             |
| pyflate                    | 484 ms                                                     | 480 ms: 1.01x faster                                                             |
| regex_v8                   | 25.1 ms                                                    | 25.0 ms: 1.01x faster                                                            |
| sympy_expand               | 473 ms                                                     | 471 ms: 1.00x faster                                                             |
| sqlglot_optimize           | 55.5 ms                                                    | 55.3 ms: 1.00x faster                                                            |
| xml_etree_process          | 61.2 ms                                                    | 60.9 ms: 1.00x faster                                                            |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.84 sec: 1.00x faster                                                           |
| sympy_sum                  | 156 ms                                                     | 156 ms: 1.00x slower                                                             |
| gc_traversal               | 3.98 ms                                                    | 4.00 ms: 1.01x slower                                                            |
| pickle_list                | 5.11 us                                                    | 5.14 us: 1.01x slower                                                            |
| sqlglot_normalize          | 110 ms                                                     | 111 ms: 1.01x slower                                                             |
| pickle_dict                | 34.8 us                                                    | 35.1 us: 1.01x slower                                                            |
| html5lib                   | 67.2 ms                                                    | 67.8 ms: 1.01x slower                                                            |
| dulwich_log                | 67.2 ms                                                    | 67.8 ms: 1.01x slower                                                            |
| nqueens                    | 81.4 ms                                                    | 82.2 ms: 1.01x slower                                                            |
| xml_etree_generate         | 87.4 ms                                                    | 88.3 ms: 1.01x slower                                                            |
| hexiom                     | 6.30 ms                                                    | 6.36 ms: 1.01x slower                                                            |
| go                         | 145 ms                                                     | 146 ms: 1.01x slower                                                             |
| nbody                      | 88.3 ms                                                    | 89.4 ms: 1.01x slower                                                            |
| json                       | 5.31 ms                                                    | 5.38 ms: 1.01x slower                                                            |
| genshi_xml                 | 51.6 ms                                                    | 52.3 ms: 1.01x slower                                                            |
| regex_dna                  | 221 ms                                                     | 225 ms: 1.02x slower                                                             |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 5.36 ms: 1.02x slower                                                            |
| tomli_loads                | 2.12 sec                                                   | 2.17 sec: 1.02x slower                                                           |
| pickle                     | 11.5 us                                                    | 11.7 us: 1.02x slower                                                            |
| comprehensions             | 16.6 us                                                    | 17.0 us: 1.02x slower                                                            |
| telco                      | 8.41 ms                                                    | 8.61 ms: 1.02x slower                                                            |
| genshi_text                | 23.7 ms                                                    | 24.2 ms: 1.02x slower                                                            |
| meteor_contest             | 110 ms                                                     | 113 ms: 1.03x slower                                                             |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 603 ms: 1.03x slower                                                             |
| unpickle_pure_python       | 218 us                                                     | 225 us: 1.03x slower                                                             |
| coroutines                 | 23.2 ms                                                    | 24.1 ms: 1.04x slower                                                            |
| regex_effbot               | 3.67 ms                                                    | 3.85 ms: 1.05x slower                                                            |
| coverage                   | 93.1 ms                                                    | 99.5 ms: 1.07x slower                                                            |
| pathlib                    | 17.3 ms                                                    | 18.6 ms: 1.08x slower                                                            |
| python_startup_no_site     | 7.11 ms                                                    | 9.00 ms: 1.27x slower                                                            |
| Geometric mean             | (ref)                                                      | 1.01x faster                                                                     |

Benchmark hidden because not significant (20): async_tree_io, async_tree_io_tg, async_tree_none_tg, async_tree_memoization, xml_etree_parse, async_tree_cpu_io_mixed, dask, aiohttp, xml_etree_iterparse, async_tree_memoization_tg, mypy2, logging_simple, bench_mp_pool, tornado_http, asyncio_websockets, thrift, docutils, bench_thread_pool, generators, async_generators
Ignored benchmarks (4) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, django_template, djangocms, flaskblogging

# HPT report

- Reliability score: 99.65% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.98x