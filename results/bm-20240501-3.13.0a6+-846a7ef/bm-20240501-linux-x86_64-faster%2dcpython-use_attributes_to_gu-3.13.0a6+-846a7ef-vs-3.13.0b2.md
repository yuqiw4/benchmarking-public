# Results vs. 3.13.0b2

- fork: faster-cpython
- ref: use_attributes_to_gu
- machine: linux-x86_64
- commit hash: 846a7ef
- commit date: 2024-05-01
- overall geometric mean: 1.01x faster
- HPT reliability: 99.17%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-846a7ef |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 272 ms: 1.01x faster                                                             |
| chameleon      | 7.22 ms                                                    | 7.03 ms: 1.03x faster                                                            |
| html5lib       | 67.2 ms                                                    | 69.5 ms: 1.03x slower                                                            |
| tornado_http   | 94.6 ms                                                    | 93.7 ms: 1.01x faster                                                            |
| Geometric mean | (ref)                                                      | 1.00x faster                                                                     |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-846a7ef |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none            | 378 ms                                                     | 353 ms: 1.07x faster                                                             |
| async_tree_io              | 939 ms                                                     | 914 ms: 1.03x faster                                                             |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 614 ms: 1.04x slower                                                             |
| Geometric mean             | (ref)                                                      | 1.00x faster                                                                     |

Benchmark hidden because not significant (5): async_tree_memoization, async_tree_cpu_io_mixed, async_tree_io_tg, async_tree_none_tg, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-846a7ef |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pidigits       | 191 ms                                                     | 190 ms: 1.01x faster                                                             |
| float          | 78.9 ms                                                    | 78.2 ms: 1.01x faster                                                            |
| nbody          | 88.3 ms                                                    | 89.6 ms: 1.02x slower                                                            |
| Geometric mean | (ref)                                                      | 1.00x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-846a7ef |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_v8       | 25.1 ms                                                    | 24.4 ms: 1.03x faster                                                            |
| regex_compile  | 137 ms                                                     | 134 ms: 1.02x faster                                                             |
| regex_dna      | 221 ms                                                     | 221 ms: 1.00x faster                                                             |
| regex_effbot   | 3.67 ms                                                    | 3.77 ms: 1.03x slower                                                            |
| Geometric mean | (ref)                                                      | 1.01x faster                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark          | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-846a7ef |
|--------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| unpickle_list      | 5.34 us                                                    | 5.18 us: 1.03x faster                                                            |
| xml_etree_parse    | 162 ms                                                     | 158 ms: 1.02x faster                                                             |
| pickle_list        | 5.11 us                                                    | 5.00 us: 1.02x faster                                                            |
| json_loads         | 28.9 us                                                    | 28.6 us: 1.01x faster                                                            |
| unpickle           | 15.1 us                                                    | 15.0 us: 1.01x faster                                                            |
| pickle_dict        | 34.8 us                                                    | 34.8 us: 1.00x slower                                                            |
| json_dumps         | 10.7 ms                                                    | 10.8 ms: 1.01x slower                                                            |
| xml_etree_process  | 61.2 ms                                                    | 61.8 ms: 1.01x slower                                                            |
| xml_etree_generate | 87.4 ms                                                    | 88.4 ms: 1.01x slower                                                            |
| pickle             | 11.5 us                                                    | 11.6 us: 1.01x slower                                                            |
| tomli_loads        | 2.12 sec                                                   | 2.16 sec: 1.02x slower                                                           |
| pickle_pure_python | 305 us                                                     | 318 us: 1.04x slower                                                             |
| Geometric mean     | (ref)                                                      | 1.00x slower                                                                     |

Benchmark hidden because not significant (2): xml_etree_iterparse, unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-846a7ef |
|------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 10.5 ms: 1.02x faster                                                            |
| python_startup_no_site | 7.11 ms                                                    | 7.09 ms: 1.00x faster                                                            |
| Geometric mean         | (ref)                                                      | 1.01x faster                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-846a7ef |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_xml     | 51.6 ms                                                    | 50.6 ms: 1.02x faster                                                            |
| genshi_text    | 23.7 ms                                                    | 23.3 ms: 1.02x faster                                                            |
| mako           | 11.2 ms                                                    | 11.4 ms: 1.02x slower                                                            |
| Geometric mean | (ref)                                                      | 1.00x faster                                                                     |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-846a7ef |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| go                         | 145 ms                                                     | 119 ms: 1.21x faster                                                             |
| mdp                        | 2.79 sec                                                   | 2.59 sec: 1.08x faster                                                           |
| async_tree_none            | 378 ms                                                     | 353 ms: 1.07x faster                                                             |
| richards_super             | 57.4 ms                                                    | 53.7 ms: 1.07x faster                                                            |
| scimark_fft                | 392 ms                                                     | 367 ms: 1.07x faster                                                             |
| scimark_lu                 | 122 ms                                                     | 114 ms: 1.07x faster                                                             |
| richards                   | 50.9 ms                                                    | 47.9 ms: 1.06x faster                                                            |
| gc_traversal               | 3.98 ms                                                    | 3.75 ms: 1.06x faster                                                            |
| deepcopy_memo              | 39.7 us                                                    | 38.1 us: 1.04x faster                                                            |
| deepcopy                   | 367 us                                                     | 354 us: 1.04x faster                                                             |
| create_gc_cycles           | 1.82 ms                                                    | 1.75 ms: 1.04x faster                                                            |
| deepcopy_reduce            | 3.35 us                                                    | 3.23 us: 1.04x faster                                                            |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 5.10 ms: 1.03x faster                                                            |
| unpickle_list              | 5.34 us                                                    | 5.18 us: 1.03x faster                                                            |
| coroutines                 | 23.2 ms                                                    | 22.5 ms: 1.03x faster                                                            |
| nqueens                    | 81.4 ms                                                    | 78.9 ms: 1.03x faster                                                            |
| spectral_norm              | 116 ms                                                     | 113 ms: 1.03x faster                                                             |
| regex_v8                   | 25.1 ms                                                    | 24.4 ms: 1.03x faster                                                            |
| async_tree_io              | 939 ms                                                     | 914 ms: 1.03x faster                                                             |
| chameleon                  | 7.22 ms                                                    | 7.03 ms: 1.03x faster                                                            |
| typing_runtime_protocols   | 165 us                                                     | 161 us: 1.03x faster                                                             |
| python_startup             | 10.8 ms                                                    | 10.5 ms: 1.02x faster                                                            |
| sqlglot_transpile          | 1.63 ms                                                    | 1.60 ms: 1.02x faster                                                            |
| xml_etree_parse            | 162 ms                                                     | 158 ms: 1.02x faster                                                             |
| sqlglot_parse              | 1.32 ms                                                    | 1.29 ms: 1.02x faster                                                            |
| pickle_list                | 5.11 us                                                    | 5.00 us: 1.02x faster                                                            |
| genshi_xml                 | 51.6 ms                                                    | 50.6 ms: 1.02x faster                                                            |
| chaos                      | 61.3 ms                                                    | 60.1 ms: 1.02x faster                                                            |
| regex_compile              | 137 ms                                                     | 134 ms: 1.02x faster                                                             |
| pyflate                    | 484 ms                                                     | 476 ms: 1.02x faster                                                             |
| genshi_text                | 23.7 ms                                                    | 23.3 ms: 1.02x faster                                                            |
| dulwich_log                | 67.2 ms                                                    | 66.1 ms: 1.02x faster                                                            |
| logging_silent             | 105 ns                                                     | 103 ns: 1.01x faster                                                             |
| generators                 | 29.6 ms                                                    | 29.2 ms: 1.01x faster                                                            |
| sympy_sum                  | 156 ms                                                     | 154 ms: 1.01x faster                                                             |
| json_loads                 | 28.9 us                                                    | 28.6 us: 1.01x faster                                                            |
| sympy_str                  | 282 ms                                                     | 279 ms: 1.01x faster                                                             |
| sqlite_synth               | 2.99 us                                                    | 2.96 us: 1.01x faster                                                            |
| tornado_http               | 94.6 ms                                                    | 93.7 ms: 1.01x faster                                                            |
| pprint_safe_repr           | 758 ms                                                     | 751 ms: 1.01x faster                                                             |
| unpickle                   | 15.1 us                                                    | 15.0 us: 1.01x faster                                                            |
| 2to3                       | 274 ms                                                     | 272 ms: 1.01x faster                                                             |
| pidigits                   | 191 ms                                                     | 190 ms: 1.01x faster                                                             |
| sympy_integrate            | 20.5 ms                                                    | 20.3 ms: 1.01x faster                                                            |
| pprint_pformat             | 1.56 sec                                                   | 1.54 sec: 1.01x faster                                                           |
| float                      | 78.9 ms                                                    | 78.2 ms: 1.01x faster                                                            |
| deltablue                  | 3.25 ms                                                    | 3.23 ms: 1.01x faster                                                            |
| sqlglot_optimize           | 55.5 ms                                                    | 55.1 ms: 1.01x faster                                                            |
| asyncio_websockets         | 567 ms                                                     | 564 ms: 1.01x faster                                                             |
| bench_thread_pool          | 834 us                                                     | 831 us: 1.00x faster                                                             |
| regex_dna                  | 221 ms                                                     | 221 ms: 1.00x faster                                                             |
| raytrace                   | 267 ms                                                     | 266 ms: 1.00x faster                                                             |
| hexiom                     | 6.30 ms                                                    | 6.28 ms: 1.00x faster                                                            |
| python_startup_no_site     | 7.11 ms                                                    | 7.09 ms: 1.00x faster                                                            |
| pickle_dict                | 34.8 us                                                    | 34.8 us: 1.00x slower                                                            |
| sqlglot_normalize          | 110 ms                                                     | 111 ms: 1.00x slower                                                             |
| logging_simple             | 5.74 us                                                    | 5.78 us: 1.01x slower                                                            |
| comprehensions             | 16.6 us                                                    | 16.7 us: 1.01x slower                                                            |
| asyncio_tcp                | 508 ms                                                     | 511 ms: 1.01x slower                                                             |
| json_dumps                 | 10.7 ms                                                    | 10.8 ms: 1.01x slower                                                            |
| xml_etree_process          | 61.2 ms                                                    | 61.8 ms: 1.01x slower                                                            |
| async_generators           | 442 ms                                                     | 446 ms: 1.01x slower                                                             |
| xml_etree_generate         | 87.4 ms                                                    | 88.4 ms: 1.01x slower                                                            |
| pickle                     | 11.5 us                                                    | 11.6 us: 1.01x slower                                                            |
| thrift                     | 823 us                                                     | 833 us: 1.01x slower                                                             |
| pathlib                    | 17.3 ms                                                    | 17.6 ms: 1.01x slower                                                            |
| json                       | 5.31 ms                                                    | 5.39 ms: 1.01x slower                                                            |
| nbody                      | 88.3 ms                                                    | 89.6 ms: 1.02x slower                                                            |
| mako                       | 11.2 ms                                                    | 11.4 ms: 1.02x slower                                                            |
| tomli_loads                | 2.12 sec                                                   | 2.16 sec: 1.02x slower                                                           |
| telco                      | 8.41 ms                                                    | 8.62 ms: 1.03x slower                                                            |
| regex_effbot               | 3.67 ms                                                    | 3.77 ms: 1.03x slower                                                            |
| html5lib                   | 67.2 ms                                                    | 69.5 ms: 1.03x slower                                                            |
| scimark_sor                | 127 ms                                                     | 132 ms: 1.04x slower                                                             |
| coverage                   | 93.1 ms                                                    | 96.8 ms: 1.04x slower                                                            |
| pickle_pure_python         | 305 us                                                     | 318 us: 1.04x slower                                                             |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 614 ms: 1.04x slower                                                             |
| scimark_monte_carlo        | 69.2 ms                                                    | 73.9 ms: 1.07x slower                                                            |
| crypto_pyaes               | 77.5 ms                                                    | 83.5 ms: 1.08x slower                                                            |
| Geometric mean             | (ref)                                                      | 1.01x faster                                                                     |

Benchmark hidden because not significant (22): async_tree_memoization, dask, pycparser, aiohttp, djangocms, logging_format, gunicorn, mypy2, docutils, async_tree_cpu_io_mixed, xml_etree_iterparse, fannkuch, asyncio_tcp_ssl, bench_mp_pool, unpickle_pure_python, async_tree_io_tg, sympy_expand, meteor_contest, django_template, pylint, async_tree_none_tg, async_tree_memoization_tg
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 99.17% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.98x