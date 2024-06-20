# Results vs. 3.13.0b2

- fork: faster-cpython
- ref: use_attributes_to_gu
- machine: linux-x86_64
- commit hash: dedffa7
- commit date: 2024-05-01
- overall geometric mean: 1.00x faster
- HPT reliability: 85.28%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-dedffa7 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 272 ms: 1.01x faster                                                             |
| chameleon      | 7.22 ms                                                    | 7.41 ms: 1.03x slower                                                            |
| docutils       | 2.83 sec                                                   | 2.81 sec: 1.01x faster                                                           |
| html5lib       | 67.2 ms                                                    | 68.2 ms: 1.01x slower                                                            |
| tornado_http   | 94.6 ms                                                    | 93.8 ms: 1.01x faster                                                            |
| Geometric mean | (ref)                                                      | 1.00x slower                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-dedffa7 |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none            | 378 ms                                                     | 354 ms: 1.07x faster                                                             |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 610 ms: 1.04x slower                                                             |
| Geometric mean             | (ref)                                                      | 1.00x faster                                                                     |

Benchmark hidden because not significant (6): async_tree_io, async_tree_memoization, async_tree_memoization_tg, async_tree_none_tg, async_tree_cpu_io_mixed, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-dedffa7 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pidigits       | 191 ms                                                     | 195 ms: 1.02x slower                                                             |
| Geometric mean | (ref)                                                      | 1.01x slower                                                                     |

Benchmark hidden because not significant (2): nbody, float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-dedffa7 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 137 ms                                                     | 134 ms: 1.02x faster                                                             |
| regex_effbot   | 3.67 ms                                                    | 3.71 ms: 1.01x slower                                                            |
| regex_dna      | 221 ms                                                     | 225 ms: 1.02x slower                                                             |
| regex_v8       | 25.1 ms                                                    | 25.6 ms: 1.02x slower                                                            |
| Geometric mean | (ref)                                                      | 1.01x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-dedffa7 |
|----------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| json_dumps           | 10.7 ms                                                    | 10.5 ms: 1.02x faster                                                            |
| xml_etree_parse      | 162 ms                                                     | 159 ms: 1.02x faster                                                             |
| json_loads           | 28.9 us                                                    | 28.4 us: 1.02x faster                                                            |
| pickle_list          | 5.11 us                                                    | 5.12 us: 1.00x slower                                                            |
| pickle               | 11.5 us                                                    | 11.6 us: 1.01x slower                                                            |
| unpickle_pure_python | 218 us                                                     | 221 us: 1.01x slower                                                             |
| pickle_pure_python   | 305 us                                                     | 311 us: 1.02x slower                                                             |
| xml_etree_process    | 61.2 ms                                                    | 62.3 ms: 1.02x slower                                                            |
| tomli_loads          | 2.12 sec                                                   | 2.16 sec: 1.02x slower                                                           |
| xml_etree_generate   | 87.4 ms                                                    | 90.3 ms: 1.03x slower                                                            |
| pickle_dict          | 34.8 us                                                    | 35.9 us: 1.03x slower                                                            |
| Geometric mean       | (ref)                                                      | 1.01x slower                                                                     |

Benchmark hidden because not significant (3): unpickle, xml_etree_iterparse, unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-dedffa7 |
|------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 10.5 ms: 1.03x faster                                                            |
| python_startup_no_site | 7.11 ms                                                    | 7.08 ms: 1.00x faster                                                            |
| Geometric mean         | (ref)                                                      | 1.01x faster                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-dedffa7 |
|-----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_xml      | 51.6 ms                                                    | 51.3 ms: 1.01x faster                                                            |
| mako            | 11.2 ms                                                    | 11.3 ms: 1.01x slower                                                            |
| django_template | 34.8 ms                                                    | 35.1 ms: 1.01x slower                                                            |
| Geometric mean  | (ref)                                                      | 1.00x slower                                                                     |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-dedffa7 |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mdp                        | 2.79 sec                                                   | 2.57 sec: 1.09x faster                                                           |
| async_tree_none            | 378 ms                                                     | 354 ms: 1.07x faster                                                             |
| spectral_norm              | 116 ms                                                     | 111 ms: 1.04x faster                                                             |
| scimark_fft                | 392 ms                                                     | 377 ms: 1.04x faster                                                             |
| richards                   | 50.9 ms                                                    | 49.0 ms: 1.04x faster                                                            |
| deepcopy_reduce            | 3.35 us                                                    | 3.23 us: 1.04x faster                                                            |
| create_gc_cycles           | 1.82 ms                                                    | 1.75 ms: 1.04x faster                                                            |
| scimark_lu                 | 122 ms                                                     | 118 ms: 1.03x faster                                                             |
| richards_super             | 57.4 ms                                                    | 55.6 ms: 1.03x faster                                                            |
| deepcopy_memo              | 39.7 us                                                    | 38.7 us: 1.03x faster                                                            |
| python_startup             | 10.8 ms                                                    | 10.5 ms: 1.03x faster                                                            |
| crypto_pyaes               | 77.5 ms                                                    | 75.6 ms: 1.03x faster                                                            |
| nqueens                    | 81.4 ms                                                    | 79.6 ms: 1.02x faster                                                            |
| regex_compile              | 137 ms                                                     | 134 ms: 1.02x faster                                                             |
| json_dumps                 | 10.7 ms                                                    | 10.5 ms: 1.02x faster                                                            |
| dulwich_log                | 67.2 ms                                                    | 65.9 ms: 1.02x faster                                                            |
| coroutines                 | 23.2 ms                                                    | 22.8 ms: 1.02x faster                                                            |
| xml_etree_parse            | 162 ms                                                     | 159 ms: 1.02x faster                                                             |
| json_loads                 | 28.9 us                                                    | 28.4 us: 1.02x faster                                                            |
| sqlite_synth               | 2.99 us                                                    | 2.94 us: 1.02x faster                                                            |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 5.19 ms: 1.02x faster                                                            |
| sqlglot_transpile          | 1.63 ms                                                    | 1.61 ms: 1.01x faster                                                            |
| generators                 | 29.6 ms                                                    | 29.2 ms: 1.01x faster                                                            |
| sqlglot_parse              | 1.32 ms                                                    | 1.30 ms: 1.01x faster                                                            |
| chaos                      | 61.3 ms                                                    | 60.6 ms: 1.01x faster                                                            |
| deepcopy                   | 367 us                                                     | 364 us: 1.01x faster                                                             |
| bench_thread_pool          | 834 us                                                     | 826 us: 1.01x faster                                                             |
| tornado_http               | 94.6 ms                                                    | 93.8 ms: 1.01x faster                                                            |
| 2to3                       | 274 ms                                                     | 272 ms: 1.01x faster                                                             |
| comprehensions             | 16.6 us                                                    | 16.5 us: 1.01x faster                                                            |
| aiohttp                    | 1.18 ms                                                    | 1.17 ms: 1.01x faster                                                            |
| logging_format             | 6.47 us                                                    | 6.42 us: 1.01x faster                                                            |
| gunicorn                   | 1.28 ms                                                    | 1.27 ms: 1.01x faster                                                            |
| deltablue                  | 3.25 ms                                                    | 3.23 ms: 1.01x faster                                                            |
| sqlglot_optimize           | 55.5 ms                                                    | 55.2 ms: 1.01x faster                                                            |
| asyncio_websockets         | 567 ms                                                     | 564 ms: 1.01x faster                                                             |
| genshi_xml                 | 51.6 ms                                                    | 51.3 ms: 1.01x faster                                                            |
| docutils                   | 2.83 sec                                                   | 2.81 sec: 1.01x faster                                                           |
| raytrace                   | 267 ms                                                     | 266 ms: 1.00x faster                                                             |
| python_startup_no_site     | 7.11 ms                                                    | 7.08 ms: 1.00x faster                                                            |
| sympy_integrate            | 20.5 ms                                                    | 20.4 ms: 1.00x faster                                                            |
| sqlglot_normalize          | 110 ms                                                     | 110 ms: 1.00x slower                                                             |
| pickle_list                | 5.11 us                                                    | 5.12 us: 1.00x slower                                                            |
| async_generators           | 442 ms                                                     | 445 ms: 1.01x slower                                                             |
| hexiom                     | 6.30 ms                                                    | 6.33 ms: 1.01x slower                                                            |
| mako                       | 11.2 ms                                                    | 11.3 ms: 1.01x slower                                                            |
| logging_simple             | 5.74 us                                                    | 5.79 us: 1.01x slower                                                            |
| django_template            | 34.8 ms                                                    | 35.1 ms: 1.01x slower                                                            |
| pickle                     | 11.5 us                                                    | 11.6 us: 1.01x slower                                                            |
| go                         | 145 ms                                                     | 146 ms: 1.01x slower                                                             |
| pyflate                    | 484 ms                                                     | 489 ms: 1.01x slower                                                             |
| regex_effbot               | 3.67 ms                                                    | 3.71 ms: 1.01x slower                                                            |
| scimark_monte_carlo        | 69.2 ms                                                    | 70.0 ms: 1.01x slower                                                            |
| unpickle_pure_python       | 218 us                                                     | 221 us: 1.01x slower                                                             |
| pathlib                    | 17.3 ms                                                    | 17.5 ms: 1.01x slower                                                            |
| telco                      | 8.41 ms                                                    | 8.52 ms: 1.01x slower                                                            |
| logging_silent             | 105 ns                                                     | 106 ns: 1.01x slower                                                             |
| meteor_contest             | 110 ms                                                     | 111 ms: 1.01x slower                                                             |
| html5lib                   | 67.2 ms                                                    | 68.2 ms: 1.01x slower                                                            |
| pidigits                   | 191 ms                                                     | 195 ms: 1.02x slower                                                             |
| pickle_pure_python         | 305 us                                                     | 311 us: 1.02x slower                                                             |
| xml_etree_process          | 61.2 ms                                                    | 62.3 ms: 1.02x slower                                                            |
| tomli_loads                | 2.12 sec                                                   | 2.16 sec: 1.02x slower                                                           |
| regex_dna                  | 221 ms                                                     | 225 ms: 1.02x slower                                                             |
| regex_v8                   | 25.1 ms                                                    | 25.6 ms: 1.02x slower                                                            |
| chameleon                  | 7.22 ms                                                    | 7.41 ms: 1.03x slower                                                            |
| xml_etree_generate         | 87.4 ms                                                    | 90.3 ms: 1.03x slower                                                            |
| pickle_dict                | 34.8 us                                                    | 35.9 us: 1.03x slower                                                            |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 610 ms: 1.04x slower                                                             |
| json                       | 5.31 ms                                                    | 5.53 ms: 1.04x slower                                                            |
| pycparser                  | 1.16 sec                                                   | 1.21 sec: 1.05x slower                                                           |
| scimark_sor                | 127 ms                                                     | 134 ms: 1.05x slower                                                             |
| Geometric mean             | (ref)                                                      | 1.00x faster                                                                     |

Benchmark hidden because not significant (29): async_tree_io, djangocms, async_tree_memoization, mypy2, sympy_str, unpickle, dask, sympy_sum, xml_etree_iterparse, async_tree_memoization_tg, sympy_expand, genshi_text, typing_runtime_protocols, bench_mp_pool, thrift, fannkuch, asyncio_tcp, asyncio_tcp_ssl, pprint_pformat, unpickle_list, nbody, gc_traversal, async_tree_none_tg, float, pprint_safe_repr, pylint, async_tree_cpu_io_mixed, coverage, async_tree_io_tg
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 85.28% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.98x