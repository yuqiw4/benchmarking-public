# Results vs. 3.13.0b2

- fork: faster-cpython
- ref: tier2_hot_cold_split
- machine: linux-x86_64
- commit hash: 37627d3
- commit date: 2024-03-25
- overall geometric mean: 1.01x slower
- HPT reliability: 99.89%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.05x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240325-linux-x86_64-faster%2dcpython-tier2_hot_cold_split-3.13.0a5+-37627d3 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 278 ms: 1.01x slower                                                             |
| chameleon      | 7.22 ms                                                    | 7.14 ms: 1.01x faster                                                            |
| docutils       | 2.83 sec                                                   | 2.88 sec: 1.02x slower                                                           |
| html5lib       | 67.2 ms                                                    | 67.7 ms: 1.01x slower                                                            |
| tornado_http   | 94.6 ms                                                    | 96.8 ms: 1.02x slower                                                            |
| Geometric mean | (ref)                                                      | 1.01x slower                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240325-linux-x86_64-faster%2dcpython-tier2_hot_cold_split-3.13.0a5+-37627d3 |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed    | 611 ms                                                     | 595 ms: 1.03x faster                                                             |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 611 ms: 1.04x slower                                                             |
| async_tree_none_tg         | 336 ms                                                     | 354 ms: 1.05x slower                                                             |
| Geometric mean             | (ref)                                                      | 1.00x slower                                                                     |

Benchmark hidden because not significant (5): async_tree_io, async_tree_none, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240325-linux-x86_64-faster%2dcpython-tier2_hot_cold_split-3.13.0a5+-37627d3 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| float          | 78.9 ms                                                    | 77.1 ms: 1.02x faster                                                            |
| pidigits       | 191 ms                                                     | 190 ms: 1.01x faster                                                             |
| nbody          | 88.3 ms                                                    | 91.1 ms: 1.03x slower                                                            |
| Geometric mean | (ref)                                                      | 1.00x slower                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240325-linux-x86_64-faster%2dcpython-tier2_hot_cold_split-3.13.0a5+-37627d3 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_effbot   | 3.67 ms                                                    | 3.53 ms: 1.04x faster                                                            |
| regex_v8       | 25.1 ms                                                    | 24.2 ms: 1.04x faster                                                            |
| regex_dna      | 221 ms                                                     | 218 ms: 1.01x faster                                                             |
| regex_compile  | 137 ms                                                     | 146 ms: 1.07x slower                                                             |
| Geometric mean | (ref)                                                      | 1.01x faster                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240325-linux-x86_64-faster%2dcpython-tier2_hot_cold_split-3.13.0a5+-37627d3 |
|----------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| unpickle_list        | 5.34 us                                                    | 5.08 us: 1.05x faster                                                            |
| tomli_loads          | 2.12 sec                                                   | 2.07 sec: 1.02x faster                                                           |
| json_dumps           | 10.7 ms                                                    | 10.5 ms: 1.02x faster                                                            |
| xml_etree_process    | 61.2 ms                                                    | 60.4 ms: 1.01x faster                                                            |
| json_loads           | 28.9 us                                                    | 28.6 us: 1.01x faster                                                            |
| pickle_list          | 5.11 us                                                    | 5.13 us: 1.00x slower                                                            |
| xml_etree_generate   | 87.4 ms                                                    | 87.8 ms: 1.00x slower                                                            |
| pickle_pure_python   | 305 us                                                     | 310 us: 1.01x slower                                                             |
| pickle               | 11.5 us                                                    | 11.8 us: 1.03x slower                                                            |
| unpickle_pure_python | 218 us                                                     | 240 us: 1.10x slower                                                             |
| Geometric mean       | (ref)                                                      | 1.00x slower                                                                     |

Benchmark hidden because not significant (4): xml_etree_parse, pickle_dict, unpickle, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240325-linux-x86_64-faster%2dcpython-tier2_hot_cold_split-3.13.0a5+-37627d3 |
|------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 11.0 ms: 1.02x slower                                                            |
| python_startup_no_site | 7.11 ms                                                    | 9.44 ms: 1.33x slower                                                            |
| Geometric mean         | (ref)                                                      | 1.17x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240325-linux-x86_64-faster%2dcpython-tier2_hot_cold_split-3.13.0a5+-37627d3 |
|-----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako            | 11.2 ms                                                    | 10.8 ms: 1.04x faster                                                            |
| genshi_text     | 23.7 ms                                                    | 24.4 ms: 1.03x slower                                                            |
| django_template | 34.8 ms                                                    | 36.2 ms: 1.04x slower                                                            |
| genshi_xml      | 51.6 ms                                                    | 54.0 ms: 1.05x slower                                                            |
| Geometric mean  | (ref)                                                      | 1.02x slower                                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240325-linux-x86_64-faster%2dcpython-tier2_hot_cold_split-3.13.0a5+-37627d3 |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 112 us: 1.47x faster                                                             |
| create_gc_cycles           | 1.82 ms                                                    | 1.47 ms: 1.23x faster                                                            |
| scimark_fft                | 392 ms                                                     | 339 ms: 1.16x faster                                                             |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 4.69 ms: 1.12x faster                                                            |
| richards                   | 50.9 ms                                                    | 45.7 ms: 1.11x faster                                                            |
| richards_super             | 57.4 ms                                                    | 52.0 ms: 1.10x faster                                                            |
| logging_silent             | 105 ns                                                     | 99.3 ns: 1.05x faster                                                            |
| unpickle_list              | 5.34 us                                                    | 5.08 us: 1.05x faster                                                            |
| deepcopy_reduce            | 3.35 us                                                    | 3.18 us: 1.05x faster                                                            |
| crypto_pyaes               | 77.5 ms                                                    | 74.1 ms: 1.05x faster                                                            |
| sqlite_synth               | 2.99 us                                                    | 2.87 us: 1.04x faster                                                            |
| mako                       | 11.2 ms                                                    | 10.8 ms: 1.04x faster                                                            |
| gc_traversal               | 3.98 ms                                                    | 3.82 ms: 1.04x faster                                                            |
| regex_effbot               | 3.67 ms                                                    | 3.53 ms: 1.04x faster                                                            |
| regex_v8                   | 25.1 ms                                                    | 24.2 ms: 1.04x faster                                                            |
| fannkuch                   | 402 ms                                                     | 391 ms: 1.03x faster                                                             |
| async_tree_cpu_io_mixed    | 611 ms                                                     | 595 ms: 1.03x faster                                                             |
| tomli_loads                | 2.12 sec                                                   | 2.07 sec: 1.02x faster                                                           |
| json_dumps                 | 10.7 ms                                                    | 10.5 ms: 1.02x faster                                                            |
| float                      | 78.9 ms                                                    | 77.1 ms: 1.02x faster                                                            |
| coroutines                 | 23.2 ms                                                    | 22.8 ms: 1.02x faster                                                            |
| pprint_pformat             | 1.56 sec                                                   | 1.53 sec: 1.01x faster                                                           |
| regex_dna                  | 221 ms                                                     | 218 ms: 1.01x faster                                                             |
| deepcopy                   | 367 us                                                     | 363 us: 1.01x faster                                                             |
| xml_etree_process          | 61.2 ms                                                    | 60.4 ms: 1.01x faster                                                            |
| deepcopy_memo              | 39.7 us                                                    | 39.3 us: 1.01x faster                                                            |
| json_loads                 | 28.9 us                                                    | 28.6 us: 1.01x faster                                                            |
| chameleon                  | 7.22 ms                                                    | 7.14 ms: 1.01x faster                                                            |
| thrift                     | 823 us                                                     | 816 us: 1.01x faster                                                             |
| pidigits                   | 191 ms                                                     | 190 ms: 1.01x faster                                                             |
| pyflate                    | 484 ms                                                     | 481 ms: 1.01x faster                                                             |
| mdp                        | 2.79 sec                                                   | 2.80 sec: 1.00x slower                                                           |
| pickle_list                | 5.11 us                                                    | 5.13 us: 1.00x slower                                                            |
| xml_etree_generate         | 87.4 ms                                                    | 87.8 ms: 1.00x slower                                                            |
| asyncio_websockets         | 567 ms                                                     | 570 ms: 1.01x slower                                                             |
| asyncio_tcp                | 508 ms                                                     | 511 ms: 1.01x slower                                                             |
| bench_mp_pool              | 23.9 ms                                                    | 24.0 ms: 1.01x slower                                                            |
| html5lib                   | 67.2 ms                                                    | 67.7 ms: 1.01x slower                                                            |
| json                       | 5.31 ms                                                    | 5.35 ms: 1.01x slower                                                            |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.86 sec: 1.01x slower                                                           |
| sqlglot_parse              | 1.32 ms                                                    | 1.33 ms: 1.01x slower                                                            |
| scimark_monte_carlo        | 69.2 ms                                                    | 70.0 ms: 1.01x slower                                                            |
| telco                      | 8.41 ms                                                    | 8.51 ms: 1.01x slower                                                            |
| logging_format             | 6.47 us                                                    | 6.55 us: 1.01x slower                                                            |
| 2to3                       | 274 ms                                                     | 278 ms: 1.01x slower                                                             |
| pickle_pure_python         | 305 us                                                     | 310 us: 1.01x slower                                                             |
| meteor_contest             | 110 ms                                                     | 112 ms: 1.02x slower                                                             |
| sqlglot_transpile          | 1.63 ms                                                    | 1.66 ms: 1.02x slower                                                            |
| pycparser                  | 1.16 sec                                                   | 1.18 sec: 1.02x slower                                                           |
| docutils                   | 2.83 sec                                                   | 2.88 sec: 1.02x slower                                                           |
| dask                       | 369 ms                                                     | 378 ms: 1.02x slower                                                             |
| tornado_http               | 94.6 ms                                                    | 96.8 ms: 1.02x slower                                                            |
| python_startup             | 10.8 ms                                                    | 11.0 ms: 1.02x slower                                                            |
| pickle                     | 11.5 us                                                    | 11.8 us: 1.03x slower                                                            |
| generators                 | 29.6 ms                                                    | 30.4 ms: 1.03x slower                                                            |
| logging_simple             | 5.74 us                                                    | 5.90 us: 1.03x slower                                                            |
| gunicorn                   | 1.28 ms                                                    | 1.31 ms: 1.03x slower                                                            |
| chaos                      | 61.3 ms                                                    | 63.1 ms: 1.03x slower                                                            |
| sqlglot_normalize          | 110 ms                                                     | 113 ms: 1.03x slower                                                             |
| bench_thread_pool          | 834 us                                                     | 859 us: 1.03x slower                                                             |
| sympy_str                  | 282 ms                                                     | 291 ms: 1.03x slower                                                             |
| nbody                      | 88.3 ms                                                    | 91.1 ms: 1.03x slower                                                            |
| genshi_text                | 23.7 ms                                                    | 24.4 ms: 1.03x slower                                                            |
| aiohttp                    | 1.18 ms                                                    | 1.22 ms: 1.04x slower                                                            |
| coverage                   | 93.1 ms                                                    | 96.7 ms: 1.04x slower                                                            |
| django_template            | 34.8 ms                                                    | 36.2 ms: 1.04x slower                                                            |
| sympy_expand               | 473 ms                                                     | 491 ms: 1.04x slower                                                             |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 611 ms: 1.04x slower                                                             |
| async_generators           | 442 ms                                                     | 460 ms: 1.04x slower                                                             |
| sqlglot_optimize           | 55.5 ms                                                    | 58.1 ms: 1.05x slower                                                            |
| genshi_xml                 | 51.6 ms                                                    | 54.0 ms: 1.05x slower                                                            |
| async_tree_none_tg         | 336 ms                                                     | 354 ms: 1.05x slower                                                             |
| dulwich_log                | 67.2 ms                                                    | 70.9 ms: 1.05x slower                                                            |
| sympy_sum                  | 156 ms                                                     | 165 ms: 1.06x slower                                                             |
| deltablue                  | 3.25 ms                                                    | 3.46 ms: 1.06x slower                                                            |
| sympy_integrate            | 20.5 ms                                                    | 21.8 ms: 1.06x slower                                                            |
| regex_compile              | 137 ms                                                     | 146 ms: 1.07x slower                                                             |
| scimark_sor                | 127 ms                                                     | 136 ms: 1.07x slower                                                             |
| mypy2                      | 742 ms                                                     | 795 ms: 1.07x slower                                                             |
| go                         | 145 ms                                                     | 155 ms: 1.07x slower                                                             |
| scimark_lu                 | 122 ms                                                     | 132 ms: 1.08x slower                                                             |
| comprehensions             | 16.6 us                                                    | 18.2 us: 1.09x slower                                                            |
| raytrace                   | 267 ms                                                     | 292 ms: 1.10x slower                                                             |
| unpickle_pure_python       | 218 us                                                     | 240 us: 1.10x slower                                                             |
| pathlib                    | 17.3 ms                                                    | 19.1 ms: 1.10x slower                                                            |
| nqueens                    | 81.4 ms                                                    | 90.8 ms: 1.11x slower                                                            |
| hexiom                     | 6.30 ms                                                    | 7.22 ms: 1.15x slower                                                            |
| python_startup_no_site     | 7.11 ms                                                    | 9.44 ms: 1.33x slower                                                            |
| Geometric mean             | (ref)                                                      | 1.01x slower                                                                     |

Benchmark hidden because not significant (13): async_tree_io, xml_etree_parse, async_tree_none, async_tree_io_tg, djangocms, pprint_safe_repr, async_tree_memoization, pickle_dict, spectral_norm, unpickle, xml_etree_iterparse, async_tree_memoization_tg, pylint
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging
Ignored benchmarks (1) of results/bm-20240325-3.13.0a5+-37627d3-JIT/bm-20240325-linux-x86_64-faster%2dcpython-tier2_hot_cold_split-3.13.0a5+-37627d3.json: unpack_sequence

# HPT report

- Reliability score: 99.89% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.05x