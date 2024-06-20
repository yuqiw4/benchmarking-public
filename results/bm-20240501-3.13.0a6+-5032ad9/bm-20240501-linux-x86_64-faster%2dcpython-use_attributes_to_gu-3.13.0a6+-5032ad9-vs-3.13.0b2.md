# Results vs. 3.13.0b2

- fork: faster-cpython
- ref: use_attributes_to_gu
- machine: linux-x86_64
- commit hash: 5032ad9
- commit date: 2024-05-01
- overall geometric mean: 1.01x faster
- HPT reliability: 98.75%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-5032ad9 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 272 ms: 1.01x faster                                                             |
| chameleon      | 7.22 ms                                                    | 7.26 ms: 1.01x slower                                                            |
| html5lib       | 67.2 ms                                                    | 68.6 ms: 1.02x slower                                                            |
| tornado_http   | 94.6 ms                                                    | 93.6 ms: 1.01x faster                                                            |
| Geometric mean | (ref)                                                      | 1.00x slower                                                                     |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-5032ad9 |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none            | 378 ms                                                     | 356 ms: 1.06x faster                                                             |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 610 ms: 1.04x slower                                                             |
| Geometric mean             | (ref)                                                      | 1.01x faster                                                                     |

Benchmark hidden because not significant (6): async_tree_io, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg, async_tree_cpu_io_mixed, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-5032ad9 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| float          | 78.9 ms                                                    | 77.9 ms: 1.01x faster                                                            |
| pidigits       | 191 ms                                                     | 191 ms: 1.00x faster                                                             |
| Geometric mean | (ref)                                                      | 1.01x faster                                                                     |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-5032ad9 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 137 ms                                                     | 134 ms: 1.02x faster                                                             |
| regex_v8       | 25.1 ms                                                    | 25.8 ms: 1.03x slower                                                            |
| regex_dna      | 221 ms                                                     | 230 ms: 1.04x slower                                                             |
| regex_effbot   | 3.67 ms                                                    | 3.89 ms: 1.06x slower                                                            |
| Geometric mean | (ref)                                                      | 1.03x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-5032ad9 |
|----------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| xml_etree_parse      | 162 ms                                                     | 158 ms: 1.02x faster                                                             |
| json_loads           | 28.9 us                                                    | 28.4 us: 1.02x faster                                                            |
| json_dumps           | 10.7 ms                                                    | 10.5 ms: 1.02x faster                                                            |
| unpickle_list        | 5.34 us                                                    | 5.28 us: 1.01x faster                                                            |
| pickle_list          | 5.11 us                                                    | 5.05 us: 1.01x faster                                                            |
| unpickle_pure_python | 218 us                                                     | 217 us: 1.01x faster                                                             |
| pickle_dict          | 34.8 us                                                    | 34.7 us: 1.00x faster                                                            |
| xml_etree_process    | 61.2 ms                                                    | 61.8 ms: 1.01x slower                                                            |
| unpickle             | 15.1 us                                                    | 15.3 us: 1.01x slower                                                            |
| pickle_pure_python   | 305 us                                                     | 311 us: 1.02x slower                                                             |
| xml_etree_generate   | 87.4 ms                                                    | 89.0 ms: 1.02x slower                                                            |
| tomli_loads          | 2.12 sec                                                   | 2.17 sec: 1.02x slower                                                           |
| pickle               | 11.5 us                                                    | 12.0 us: 1.04x slower                                                            |
| Geometric mean       | (ref)                                                      | 1.00x slower                                                                     |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-5032ad9 |
|------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 10.5 ms: 1.02x faster                                                            |
| python_startup_no_site | 7.11 ms                                                    | 7.09 ms: 1.00x faster                                                            |
| Geometric mean         | (ref)                                                      | 1.01x faster                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-5032ad9 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_text    | 23.7 ms                                                    | 23.0 ms: 1.03x faster                                                            |
| mako           | 11.2 ms                                                    | 11.5 ms: 1.02x slower                                                            |
| Geometric mean | (ref)                                                      | 1.00x faster                                                                     |

Benchmark hidden because not significant (2): django_template, genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-5032ad9 |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| logging_silent             | 105 ns                                                     | 98.1 ns: 1.07x faster                                                            |
| async_tree_none            | 378 ms                                                     | 356 ms: 1.06x faster                                                             |
| spectral_norm              | 116 ms                                                     | 110 ms: 1.06x faster                                                             |
| richards                   | 50.9 ms                                                    | 48.3 ms: 1.05x faster                                                            |
| coroutines                 | 23.2 ms                                                    | 22.0 ms: 1.05x faster                                                            |
| richards_super             | 57.4 ms                                                    | 54.6 ms: 1.05x faster                                                            |
| deepcopy_memo              | 39.7 us                                                    | 38.0 us: 1.04x faster                                                            |
| scimark_fft                | 392 ms                                                     | 377 ms: 1.04x faster                                                             |
| deepcopy_reduce            | 3.35 us                                                    | 3.22 us: 1.04x faster                                                            |
| create_gc_cycles           | 1.82 ms                                                    | 1.75 ms: 1.04x faster                                                            |
| scimark_lu                 | 122 ms                                                     | 118 ms: 1.04x faster                                                             |
| genshi_text                | 23.7 ms                                                    | 23.0 ms: 1.03x faster                                                            |
| crypto_pyaes               | 77.5 ms                                                    | 75.6 ms: 1.02x faster                                                            |
| mdp                        | 2.79 sec                                                   | 2.72 sec: 1.02x faster                                                           |
| dulwich_log                | 67.2 ms                                                    | 65.6 ms: 1.02x faster                                                            |
| xml_etree_parse            | 162 ms                                                     | 158 ms: 1.02x faster                                                             |
| sqlglot_transpile          | 1.63 ms                                                    | 1.60 ms: 1.02x faster                                                            |
| nqueens                    | 81.4 ms                                                    | 79.6 ms: 1.02x faster                                                            |
| hexiom                     | 6.30 ms                                                    | 6.16 ms: 1.02x faster                                                            |
| python_startup             | 10.8 ms                                                    | 10.5 ms: 1.02x faster                                                            |
| sqlglot_parse              | 1.32 ms                                                    | 1.29 ms: 1.02x faster                                                            |
| json_loads                 | 28.9 us                                                    | 28.4 us: 1.02x faster                                                            |
| regex_compile              | 137 ms                                                     | 134 ms: 1.02x faster                                                             |
| generators                 | 29.6 ms                                                    | 29.1 ms: 1.02x faster                                                            |
| json_dumps                 | 10.7 ms                                                    | 10.5 ms: 1.02x faster                                                            |
| deepcopy                   | 367 us                                                     | 361 us: 1.02x faster                                                             |
| sympy_str                  | 282 ms                                                     | 278 ms: 1.02x faster                                                             |
| sqlite_synth               | 2.99 us                                                    | 2.95 us: 1.01x faster                                                            |
| unpickle_list              | 5.34 us                                                    | 5.28 us: 1.01x faster                                                            |
| bench_thread_pool          | 834 us                                                     | 824 us: 1.01x faster                                                             |
| comprehensions             | 16.6 us                                                    | 16.4 us: 1.01x faster                                                            |
| float                      | 78.9 ms                                                    | 77.9 ms: 1.01x faster                                                            |
| logging_format             | 6.47 us                                                    | 6.39 us: 1.01x faster                                                            |
| chaos                      | 61.3 ms                                                    | 60.6 ms: 1.01x faster                                                            |
| tornado_http               | 94.6 ms                                                    | 93.6 ms: 1.01x faster                                                            |
| deltablue                  | 3.25 ms                                                    | 3.22 ms: 1.01x faster                                                            |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 5.21 ms: 1.01x faster                                                            |
| thrift                     | 823 us                                                     | 814 us: 1.01x faster                                                             |
| sqlglot_optimize           | 55.5 ms                                                    | 54.9 ms: 1.01x faster                                                            |
| aiohttp                    | 1.18 ms                                                    | 1.17 ms: 1.01x faster                                                            |
| pickle_list                | 5.11 us                                                    | 5.05 us: 1.01x faster                                                            |
| 2to3                       | 274 ms                                                     | 272 ms: 1.01x faster                                                             |
| sympy_integrate            | 20.5 ms                                                    | 20.3 ms: 1.01x faster                                                            |
| pyflate                    | 484 ms                                                     | 480 ms: 1.01x faster                                                             |
| sympy_sum                  | 156 ms                                                     | 155 ms: 1.01x faster                                                             |
| asyncio_websockets         | 567 ms                                                     | 563 ms: 1.01x faster                                                             |
| unpickle_pure_python       | 218 us                                                     | 217 us: 1.01x faster                                                             |
| sympy_expand               | 473 ms                                                     | 470 ms: 1.01x faster                                                             |
| pidigits                   | 191 ms                                                     | 191 ms: 1.00x faster                                                             |
| pickle_dict                | 34.8 us                                                    | 34.7 us: 1.00x faster                                                            |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.84 sec: 1.00x faster                                                           |
| sqlglot_normalize          | 110 ms                                                     | 110 ms: 1.00x faster                                                             |
| python_startup_no_site     | 7.11 ms                                                    | 7.09 ms: 1.00x faster                                                            |
| gc_traversal               | 3.98 ms                                                    | 3.98 ms: 1.00x slower                                                            |
| fannkuch                   | 402 ms                                                     | 403 ms: 1.00x slower                                                             |
| chameleon                  | 7.22 ms                                                    | 7.26 ms: 1.01x slower                                                            |
| asyncio_tcp                | 508 ms                                                     | 511 ms: 1.01x slower                                                             |
| async_generators           | 442 ms                                                     | 445 ms: 1.01x slower                                                             |
| meteor_contest             | 110 ms                                                     | 111 ms: 1.01x slower                                                             |
| logging_simple             | 5.74 us                                                    | 5.80 us: 1.01x slower                                                            |
| xml_etree_process          | 61.2 ms                                                    | 61.8 ms: 1.01x slower                                                            |
| json                       | 5.31 ms                                                    | 5.37 ms: 1.01x slower                                                            |
| unpickle                   | 15.1 us                                                    | 15.3 us: 1.01x slower                                                            |
| pathlib                    | 17.3 ms                                                    | 17.6 ms: 1.01x slower                                                            |
| telco                      | 8.41 ms                                                    | 8.53 ms: 1.01x slower                                                            |
| pickle_pure_python         | 305 us                                                     | 311 us: 1.02x slower                                                             |
| xml_etree_generate         | 87.4 ms                                                    | 89.0 ms: 1.02x slower                                                            |
| mako                       | 11.2 ms                                                    | 11.5 ms: 1.02x slower                                                            |
| scimark_monte_carlo        | 69.2 ms                                                    | 70.5 ms: 1.02x slower                                                            |
| html5lib                   | 67.2 ms                                                    | 68.6 ms: 1.02x slower                                                            |
| tomli_loads                | 2.12 sec                                                   | 2.17 sec: 1.02x slower                                                           |
| regex_v8                   | 25.1 ms                                                    | 25.8 ms: 1.03x slower                                                            |
| scimark_sor                | 127 ms                                                     | 131 ms: 1.03x slower                                                             |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 610 ms: 1.04x slower                                                             |
| regex_dna                  | 221 ms                                                     | 230 ms: 1.04x slower                                                             |
| pickle                     | 11.5 us                                                    | 12.0 us: 1.04x slower                                                            |
| pycparser                  | 1.16 sec                                                   | 1.21 sec: 1.05x slower                                                           |
| regex_effbot               | 3.67 ms                                                    | 3.89 ms: 1.06x slower                                                            |
| Geometric mean             | (ref)                                                      | 1.01x faster                                                                     |

Benchmark hidden because not significant (23): async_tree_io, async_tree_io_tg, async_tree_memoization_tg, mypy2, django_template, dask, genshi_xml, async_tree_none_tg, go, xml_etree_iterparse, docutils, pprint_pformat, typing_runtime_protocols, coverage, gunicorn, nbody, pprint_safe_repr, bench_mp_pool, raytrace, async_tree_cpu_io_mixed, pylint, async_tree_memoization, djangocms
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 98.75% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.98x