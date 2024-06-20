# Results vs. 3.13.0b2

- fork: faster-cpython
- ref: specialize_binary_op
- machine: linux-x86_64
- commit hash: accc60a
- commit date: 2024-04-04
- overall geometric mean: 1.00x slower
- HPT reliability: 55.83%
- HPT 99th percentile: 1.00x slower
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-accc60a |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 268 ms: 1.02x faster                                                             |
| chameleon      | 7.22 ms                                                    | 6.96 ms: 1.04x faster                                                            |
| docutils       | 2.83 sec                                                   | 2.78 sec: 1.02x faster                                                           |
| html5lib       | 67.2 ms                                                    | 68.2 ms: 1.02x slower                                                            |
| tornado_http   | 94.6 ms                                                    | 94.3 ms: 1.00x faster                                                            |
| Geometric mean | (ref)                                                      | 1.01x faster                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-accc60a |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none            | 378 ms                                                     | 350 ms: 1.08x faster                                                             |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 602 ms: 1.02x slower                                                             |
| Geometric mean             | (ref)                                                      | 1.01x faster                                                                     |

Benchmark hidden because not significant (6): async_tree_io, async_tree_memoization, async_tree_none_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-accc60a |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pidigits       | 191 ms                                                     | 195 ms: 1.02x slower                                                             |
| float          | 78.9 ms                                                    | 81.7 ms: 1.04x slower                                                            |
| nbody          | 88.3 ms                                                    | 127 ms: 1.43x slower                                                             |
| Geometric mean | (ref)                                                      | 1.15x slower                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-accc60a |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 137 ms                                                     | 135 ms: 1.01x faster                                                             |
| regex_effbot   | 3.67 ms                                                    | 3.66 ms: 1.00x faster                                                            |
| regex_v8       | 25.1 ms                                                    | 25.4 ms: 1.01x slower                                                            |
| regex_dna      | 221 ms                                                     | 227 ms: 1.02x slower                                                             |
| Geometric mean | (ref)                                                      | 1.00x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-accc60a |
|----------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| unpickle_list        | 5.34 us                                                    | 5.09 us: 1.05x faster                                                            |
| pickle_pure_python   | 305 us                                                     | 297 us: 1.03x faster                                                             |
| json_loads           | 28.9 us                                                    | 28.5 us: 1.01x faster                                                            |
| xml_etree_iterparse  | 107 ms                                                     | 106 ms: 1.01x faster                                                             |
| json_dumps           | 10.7 ms                                                    | 10.7 ms: 1.01x faster                                                            |
| unpickle_pure_python | 218 us                                                     | 219 us: 1.00x slower                                                             |
| xml_etree_generate   | 87.4 ms                                                    | 88.6 ms: 1.01x slower                                                            |
| pickle_dict          | 34.8 us                                                    | 35.2 us: 1.01x slower                                                            |
| pickle_list          | 5.11 us                                                    | 5.26 us: 1.03x slower                                                            |
| unpickle             | 15.1 us                                                    | 15.6 us: 1.03x slower                                                            |
| pickle               | 11.5 us                                                    | 12.0 us: 1.05x slower                                                            |
| tomli_loads          | 2.12 sec                                                   | 2.26 sec: 1.07x slower                                                           |
| Geometric mean       | (ref)                                                      | 1.01x slower                                                                     |

Benchmark hidden because not significant (2): xml_etree_parse, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-accc60a |
|------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 10.6 ms: 1.01x faster                                                            |
| python_startup_no_site | 7.11 ms                                                    | 9.01 ms: 1.27x slower                                                            |
| Geometric mean         | (ref)                                                      | 1.12x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-accc60a |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako           | 11.2 ms                                                    | 11.0 ms: 1.02x faster                                                            |
| genshi_text    | 23.7 ms                                                    | 23.5 ms: 1.01x faster                                                            |
| genshi_xml     | 51.6 ms                                                    | 51.2 ms: 1.01x faster                                                            |
| Geometric mean | (ref)                                                      | 1.01x faster                                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-accc60a |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 113 us: 1.46x faster                                                             |
| pylint                     | 317 ms                                                     | 278 ms: 1.14x faster                                                             |
| richards_super             | 57.4 ms                                                    | 52.0 ms: 1.10x faster                                                            |
| richards                   | 50.9 ms                                                    | 46.2 ms: 1.10x faster                                                            |
| deepcopy_memo              | 39.7 us                                                    | 36.5 us: 1.09x faster                                                            |
| async_tree_none            | 378 ms                                                     | 350 ms: 1.08x faster                                                             |
| deepcopy_reduce            | 3.35 us                                                    | 3.12 us: 1.07x faster                                                            |
| deepcopy                   | 367 us                                                     | 347 us: 1.06x faster                                                             |
| logging_silent             | 105 ns                                                     | 99.2 ns: 1.06x faster                                                            |
| mdp                        | 2.79 sec                                                   | 2.65 sec: 1.05x faster                                                           |
| unpickle_list              | 5.34 us                                                    | 5.09 us: 1.05x faster                                                            |
| create_gc_cycles           | 1.82 ms                                                    | 1.75 ms: 1.04x faster                                                            |
| chameleon                  | 7.22 ms                                                    | 6.96 ms: 1.04x faster                                                            |
| pprint_safe_repr           | 758 ms                                                     | 733 ms: 1.03x faster                                                             |
| pprint_pformat             | 1.56 sec                                                   | 1.50 sec: 1.03x faster                                                           |
| crypto_pyaes               | 77.5 ms                                                    | 75.0 ms: 1.03x faster                                                            |
| deltablue                  | 3.25 ms                                                    | 3.17 ms: 1.03x faster                                                            |
| pickle_pure_python         | 305 us                                                     | 297 us: 1.03x faster                                                             |
| sqlglot_transpile          | 1.63 ms                                                    | 1.59 ms: 1.03x faster                                                            |
| 2to3                       | 274 ms                                                     | 268 ms: 1.02x faster                                                             |
| sqlglot_parse              | 1.32 ms                                                    | 1.29 ms: 1.02x faster                                                            |
| mako                       | 11.2 ms                                                    | 11.0 ms: 1.02x faster                                                            |
| comprehensions             | 16.6 us                                                    | 16.3 us: 1.02x faster                                                            |
| sqlglot_optimize           | 55.5 ms                                                    | 54.7 ms: 1.02x faster                                                            |
| docutils                   | 2.83 sec                                                   | 2.78 sec: 1.02x faster                                                           |
| sympy_expand               | 473 ms                                                     | 466 ms: 1.01x faster                                                             |
| thrift                     | 823 us                                                     | 811 us: 1.01x faster                                                             |
| sympy_str                  | 282 ms                                                     | 278 ms: 1.01x faster                                                             |
| aiohttp                    | 1.18 ms                                                    | 1.16 ms: 1.01x faster                                                            |
| gunicorn                   | 1.28 ms                                                    | 1.26 ms: 1.01x faster                                                            |
| python_startup             | 10.8 ms                                                    | 10.6 ms: 1.01x faster                                                            |
| regex_compile              | 137 ms                                                     | 135 ms: 1.01x faster                                                             |
| json_loads                 | 28.9 us                                                    | 28.5 us: 1.01x faster                                                            |
| meteor_contest             | 110 ms                                                     | 109 ms: 1.01x faster                                                             |
| sqlite_synth               | 2.99 us                                                    | 2.96 us: 1.01x faster                                                            |
| sympy_integrate            | 20.5 ms                                                    | 20.3 ms: 1.01x faster                                                            |
| xml_etree_iterparse        | 107 ms                                                     | 106 ms: 1.01x faster                                                             |
| genshi_text                | 23.7 ms                                                    | 23.5 ms: 1.01x faster                                                            |
| genshi_xml                 | 51.6 ms                                                    | 51.2 ms: 1.01x faster                                                            |
| bench_thread_pool          | 834 us                                                     | 828 us: 1.01x faster                                                             |
| sqlglot_normalize          | 110 ms                                                     | 109 ms: 1.01x faster                                                             |
| json_dumps                 | 10.7 ms                                                    | 10.7 ms: 1.01x faster                                                            |
| logging_format             | 6.47 us                                                    | 6.43 us: 1.01x faster                                                            |
| asyncio_websockets         | 567 ms                                                     | 563 ms: 1.01x faster                                                             |
| tornado_http               | 94.6 ms                                                    | 94.3 ms: 1.00x faster                                                            |
| regex_effbot               | 3.67 ms                                                    | 3.66 ms: 1.00x faster                                                            |
| unpickle_pure_python       | 218 us                                                     | 219 us: 1.00x slower                                                             |
| asyncio_tcp                | 508 ms                                                     | 510 ms: 1.00x slower                                                             |
| pyflate                    | 484 ms                                                     | 486 ms: 1.00x slower                                                             |
| async_generators           | 442 ms                                                     | 444 ms: 1.00x slower                                                             |
| dulwich_log                | 67.2 ms                                                    | 67.6 ms: 1.01x slower                                                            |
| go                         | 145 ms                                                     | 146 ms: 1.01x slower                                                             |
| regex_v8                   | 25.1 ms                                                    | 25.4 ms: 1.01x slower                                                            |
| gc_traversal               | 3.98 ms                                                    | 4.02 ms: 1.01x slower                                                            |
| xml_etree_generate         | 87.4 ms                                                    | 88.6 ms: 1.01x slower                                                            |
| pickle_dict                | 34.8 us                                                    | 35.2 us: 1.01x slower                                                            |
| html5lib                   | 67.2 ms                                                    | 68.2 ms: 1.02x slower                                                            |
| pidigits                   | 191 ms                                                     | 195 ms: 1.02x slower                                                             |
| telco                      | 8.41 ms                                                    | 8.60 ms: 1.02x slower                                                            |
| json                       | 5.31 ms                                                    | 5.43 ms: 1.02x slower                                                            |
| regex_dna                  | 221 ms                                                     | 227 ms: 1.02x slower                                                             |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 602 ms: 1.02x slower                                                             |
| pycparser                  | 1.16 sec                                                   | 1.19 sec: 1.03x slower                                                           |
| nqueens                    | 81.4 ms                                                    | 83.8 ms: 1.03x slower                                                            |
| pickle_list                | 5.11 us                                                    | 5.26 us: 1.03x slower                                                            |
| fannkuch                   | 402 ms                                                     | 414 ms: 1.03x slower                                                             |
| unpickle                   | 15.1 us                                                    | 15.6 us: 1.03x slower                                                            |
| float                      | 78.9 ms                                                    | 81.7 ms: 1.04x slower                                                            |
| coroutines                 | 23.2 ms                                                    | 24.1 ms: 1.04x slower                                                            |
| pickle                     | 11.5 us                                                    | 12.0 us: 1.05x slower                                                            |
| raytrace                   | 267 ms                                                     | 280 ms: 1.05x slower                                                             |
| scimark_monte_carlo        | 69.2 ms                                                    | 73.0 ms: 1.06x slower                                                            |
| scimark_sor                | 127 ms                                                     | 135 ms: 1.06x slower                                                             |
| tomli_loads                | 2.12 sec                                                   | 2.26 sec: 1.07x slower                                                           |
| coverage                   | 93.1 ms                                                    | 101 ms: 1.08x slower                                                             |
| pathlib                    | 17.3 ms                                                    | 18.8 ms: 1.08x slower                                                            |
| scimark_fft                | 392 ms                                                     | 427 ms: 1.09x slower                                                             |
| chaos                      | 61.3 ms                                                    | 69.9 ms: 1.14x slower                                                            |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 6.13 ms: 1.16x slower                                                            |
| spectral_norm              | 116 ms                                                     | 141 ms: 1.22x slower                                                             |
| python_startup_no_site     | 7.11 ms                                                    | 9.01 ms: 1.27x slower                                                            |
| nbody                      | 88.3 ms                                                    | 127 ms: 1.43x slower                                                             |
| Geometric mean             | (ref)                                                      | 1.00x slower                                                                     |

Benchmark hidden because not significant (17): async_tree_io, async_tree_memoization, async_tree_none_tg, async_tree_io_tg, mypy2, xml_etree_parse, async_tree_memoization_tg, async_tree_cpu_io_mixed, scimark_lu, dask, generators, xml_etree_process, bench_mp_pool, sympy_sum, asyncio_tcp_ssl, hexiom, logging_simple
Ignored benchmarks (4) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, django_template, djangocms, flaskblogging

# HPT report

- Reliability score: 55.83% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 0.98x