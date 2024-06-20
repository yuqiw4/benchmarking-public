# Results vs. 3.13.0b2

- fork: faster-cpython
- ref: specialize_binary_op
- machine: linux-x86_64
- commit hash: 198ceb6
- commit date: 2024-04-03
- overall geometric mean: 1.00x faster
- HPT reliability: 94.14%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.97x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-198ceb6 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 266 ms: 1.03x faster                                                             |
| chameleon      | 7.22 ms                                                    | 6.86 ms: 1.05x faster                                                            |
| docutils       | 2.83 sec                                                   | 2.78 sec: 1.02x faster                                                           |
| html5lib       | 67.2 ms                                                    | 66.1 ms: 1.02x faster                                                            |
| tornado_http   | 94.6 ms                                                    | 95.6 ms: 1.01x slower                                                            |
| Geometric mean | (ref)                                                      | 1.02x faster                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-198ceb6 |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed    | 611 ms                                                     | 594 ms: 1.03x faster                                                             |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 605 ms: 1.03x slower                                                             |
| async_tree_none_tg         | 336 ms                                                     | 350 ms: 1.04x slower                                                             |
| Geometric mean             | (ref)                                                      | 1.00x faster                                                                     |

Benchmark hidden because not significant (5): async_tree_io, async_tree_io_tg, async_tree_memoization_tg, async_tree_none, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-198ceb6 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pidigits       | 191 ms                                                     | 191 ms: 1.00x faster                                                             |
| float          | 78.9 ms                                                    | 80.8 ms: 1.02x slower                                                            |
| nbody          | 88.3 ms                                                    | 120 ms: 1.36x slower                                                             |
| Geometric mean | (ref)                                                      | 1.12x slower                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-198ceb6 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 137 ms                                                     | 135 ms: 1.02x faster                                                             |
| regex_v8       | 25.1 ms                                                    | 25.3 ms: 1.01x slower                                                            |
| regex_dna      | 221 ms                                                     | 223 ms: 1.01x slower                                                             |
| regex_effbot   | 3.67 ms                                                    | 3.73 ms: 1.02x slower                                                            |
| Geometric mean | (ref)                                                      | 1.00x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-198ceb6 |
|----------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_list          | 5.11 us                                                    | 4.93 us: 1.04x faster                                                            |
| xml_etree_process    | 61.2 ms                                                    | 59.6 ms: 1.03x faster                                                            |
| pickle_dict          | 34.8 us                                                    | 34.0 us: 1.02x faster                                                            |
| xml_etree_generate   | 87.4 ms                                                    | 85.9 ms: 1.02x faster                                                            |
| json_loads           | 28.9 us                                                    | 28.5 us: 1.01x faster                                                            |
| pickle_pure_python   | 305 us                                                     | 301 us: 1.01x faster                                                             |
| unpickle_pure_python | 218 us                                                     | 215 us: 1.01x faster                                                             |
| pickle               | 11.5 us                                                    | 11.6 us: 1.01x slower                                                            |
| tomli_loads          | 2.12 sec                                                   | 2.26 sec: 1.06x slower                                                           |
| unpickle             | 15.1 us                                                    | 16.1 us: 1.07x slower                                                            |
| Geometric mean       | (ref)                                                      | 1.00x faster                                                                     |

Benchmark hidden because not significant (4): xml_etree_parse, json_dumps, unpickle_list, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-198ceb6 |
|------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 10.5 ms: 1.02x faster                                                            |
| python_startup_no_site | 7.11 ms                                                    | 8.89 ms: 1.25x slower                                                            |
| Geometric mean         | (ref)                                                      | 1.11x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-198ceb6 |
|-----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako            | 11.2 ms                                                    | 10.9 ms: 1.03x faster                                                            |
| genshi_xml      | 51.6 ms                                                    | 51.2 ms: 1.01x faster                                                            |
| django_template | 34.8 ms                                                    | 35.1 ms: 1.01x slower                                                            |
| Geometric mean  | (ref)                                                      | 1.01x faster                                                                     |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-198ceb6 |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 111 us: 1.48x faster                                                             |
| create_gc_cycles           | 1.82 ms                                                    | 1.44 ms: 1.26x faster                                                            |
| richards                   | 50.9 ms                                                    | 45.7 ms: 1.11x faster                                                            |
| richards_super             | 57.4 ms                                                    | 51.7 ms: 1.11x faster                                                            |
| gc_traversal               | 3.98 ms                                                    | 3.73 ms: 1.07x faster                                                            |
| deepcopy_reduce            | 3.35 us                                                    | 3.17 us: 1.06x faster                                                            |
| chameleon                  | 7.22 ms                                                    | 6.86 ms: 1.05x faster                                                            |
| mdp                        | 2.79 sec                                                   | 2.66 sec: 1.05x faster                                                           |
| logging_silent             | 105 ns                                                     | 99.9 ns: 1.05x faster                                                            |
| deepcopy_memo              | 39.7 us                                                    | 37.9 us: 1.05x faster                                                            |
| pickle_list                | 5.11 us                                                    | 4.93 us: 1.04x faster                                                            |
| deepcopy                   | 367 us                                                     | 355 us: 1.03x faster                                                             |
| pprint_safe_repr           | 758 ms                                                     | 734 ms: 1.03x faster                                                             |
| sympy_str                  | 282 ms                                                     | 273 ms: 1.03x faster                                                             |
| pprint_pformat             | 1.56 sec                                                   | 1.51 sec: 1.03x faster                                                           |
| 2to3                       | 274 ms                                                     | 266 ms: 1.03x faster                                                             |
| async_tree_cpu_io_mixed    | 611 ms                                                     | 594 ms: 1.03x faster                                                             |
| mako                       | 11.2 ms                                                    | 10.9 ms: 1.03x faster                                                            |
| hexiom                     | 6.30 ms                                                    | 6.13 ms: 1.03x faster                                                            |
| xml_etree_process          | 61.2 ms                                                    | 59.6 ms: 1.03x faster                                                            |
| sympy_integrate            | 20.5 ms                                                    | 20.0 ms: 1.03x faster                                                            |
| sympy_sum                  | 156 ms                                                     | 152 ms: 1.03x faster                                                             |
| scimark_lu                 | 122 ms                                                     | 119 ms: 1.02x faster                                                             |
| python_startup             | 10.8 ms                                                    | 10.5 ms: 1.02x faster                                                            |
| pickle_dict                | 34.8 us                                                    | 34.0 us: 1.02x faster                                                            |
| crypto_pyaes               | 77.5 ms                                                    | 75.9 ms: 1.02x faster                                                            |
| thrift                     | 823 us                                                     | 806 us: 1.02x faster                                                             |
| sqlglot_transpile          | 1.63 ms                                                    | 1.60 ms: 1.02x faster                                                            |
| sympy_expand               | 473 ms                                                     | 464 ms: 1.02x faster                                                             |
| docutils                   | 2.83 sec                                                   | 2.78 sec: 1.02x faster                                                           |
| sqlglot_parse              | 1.32 ms                                                    | 1.30 ms: 1.02x faster                                                            |
| xml_etree_generate         | 87.4 ms                                                    | 85.9 ms: 1.02x faster                                                            |
| html5lib                   | 67.2 ms                                                    | 66.1 ms: 1.02x faster                                                            |
| asyncio_tcp                | 508 ms                                                     | 500 ms: 1.02x faster                                                             |
| sqlite_synth               | 2.99 us                                                    | 2.94 us: 1.02x faster                                                            |
| meteor_contest             | 110 ms                                                     | 108 ms: 1.02x faster                                                             |
| go                         | 145 ms                                                     | 142 ms: 1.02x faster                                                             |
| regex_compile              | 137 ms                                                     | 135 ms: 1.02x faster                                                             |
| json_loads                 | 28.9 us                                                    | 28.5 us: 1.01x faster                                                            |
| pickle_pure_python         | 305 us                                                     | 301 us: 1.01x faster                                                             |
| unpickle_pure_python       | 218 us                                                     | 215 us: 1.01x faster                                                             |
| comprehensions             | 16.6 us                                                    | 16.5 us: 1.01x faster                                                            |
| deltablue                  | 3.25 ms                                                    | 3.23 ms: 1.01x faster                                                            |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.83 sec: 1.01x faster                                                           |
| bench_thread_pool          | 834 us                                                     | 827 us: 1.01x faster                                                             |
| genshi_xml                 | 51.6 ms                                                    | 51.2 ms: 1.01x faster                                                            |
| aiohttp                    | 1.18 ms                                                    | 1.17 ms: 1.01x faster                                                            |
| sqlglot_optimize           | 55.5 ms                                                    | 55.2 ms: 1.01x faster                                                            |
| sqlglot_normalize          | 110 ms                                                     | 110 ms: 1.00x faster                                                             |
| pyflate                    | 484 ms                                                     | 482 ms: 1.00x faster                                                             |
| pidigits                   | 191 ms                                                     | 191 ms: 1.00x faster                                                             |
| fannkuch                   | 402 ms                                                     | 404 ms: 1.00x slower                                                             |
| django_template            | 34.8 ms                                                    | 35.1 ms: 1.01x slower                                                            |
| regex_v8                   | 25.1 ms                                                    | 25.3 ms: 1.01x slower                                                            |
| regex_dna                  | 221 ms                                                     | 223 ms: 1.01x slower                                                             |
| tornado_http               | 94.6 ms                                                    | 95.6 ms: 1.01x slower                                                            |
| pickle                     | 11.5 us                                                    | 11.6 us: 1.01x slower                                                            |
| logging_format             | 6.47 us                                                    | 6.56 us: 1.01x slower                                                            |
| dulwich_log                | 67.2 ms                                                    | 68.2 ms: 1.02x slower                                                            |
| regex_effbot               | 3.67 ms                                                    | 3.73 ms: 1.02x slower                                                            |
| nqueens                    | 81.4 ms                                                    | 83.0 ms: 1.02x slower                                                            |
| float                      | 78.9 ms                                                    | 80.8 ms: 1.02x slower                                                            |
| generators                 | 29.6 ms                                                    | 30.4 ms: 1.02x slower                                                            |
| logging_simple             | 5.74 us                                                    | 5.91 us: 1.03x slower                                                            |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 605 ms: 1.03x slower                                                             |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 5.45 ms: 1.03x slower                                                            |
| coroutines                 | 23.2 ms                                                    | 24.1 ms: 1.04x slower                                                            |
| async_tree_none_tg         | 336 ms                                                     | 350 ms: 1.04x slower                                                             |
| scimark_monte_carlo        | 69.2 ms                                                    | 72.8 ms: 1.05x slower                                                            |
| coverage                   | 93.1 ms                                                    | 98.1 ms: 1.05x slower                                                            |
| scimark_sor                | 127 ms                                                     | 134 ms: 1.05x slower                                                             |
| tomli_loads                | 2.12 sec                                                   | 2.26 sec: 1.06x slower                                                           |
| unpickle                   | 15.1 us                                                    | 16.1 us: 1.07x slower                                                            |
| scimark_fft                | 392 ms                                                     | 422 ms: 1.08x slower                                                             |
| raytrace                   | 267 ms                                                     | 288 ms: 1.08x slower                                                             |
| pathlib                    | 17.3 ms                                                    | 18.8 ms: 1.09x slower                                                            |
| chaos                      | 61.3 ms                                                    | 68.7 ms: 1.12x slower                                                            |
| spectral_norm              | 116 ms                                                     | 140 ms: 1.21x slower                                                             |
| python_startup_no_site     | 7.11 ms                                                    | 8.89 ms: 1.25x slower                                                            |
| nbody                      | 88.3 ms                                                    | 120 ms: 1.36x slower                                                             |
| Geometric mean             | (ref)                                                      | 1.00x faster                                                                     |

Benchmark hidden because not significant (21): async_tree_io, async_tree_io_tg, async_tree_memoization_tg, xml_etree_parse, gunicorn, mypy2, json_dumps, unpickle_list, async_generators, dask, async_tree_none, asyncio_websockets, telco, async_tree_memoization, bench_mp_pool, genshi_text, pycparser, xml_etree_iterparse, json, pylint, djangocms
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 94.14% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.97x