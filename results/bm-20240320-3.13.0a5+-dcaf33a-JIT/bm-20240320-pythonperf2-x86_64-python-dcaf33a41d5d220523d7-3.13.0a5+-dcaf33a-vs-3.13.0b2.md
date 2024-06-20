# Results vs. 3.13.0b2

- fork: python
- ref: dcaf33a41d5d220523d7
- machine: linux-x86_64
- commit hash: dcaf33a
- commit date: 2024-03-20
- overall geometric mean: 1.27x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240320-pythonperf2-x86_64-python-dcaf33a41d5d220523d7-3.13.0a5+-dcaf33a |
|----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 291 ms                                                           | 332 ms: 1.14x slower                                                         |
| chameleon      | 7.40 ms                                                          | 7.21 ms: 1.03x faster                                                        |
| docutils       | 2.98 sec                                                         | 4.70 sec: 1.57x slower                                                       |
| html5lib       | 74.7 ms                                                          | 82.5 ms: 1.11x slower                                                        |
| tornado_http   | 119 ms                                                           | 128 ms: 1.07x slower                                                         |
| Geometric mean | (ref)                                                            | 1.16x slower                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240320-pythonperf2-x86_64-python-dcaf33a41d5d220523d7-3.13.0a5+-dcaf33a |
|----------------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed    | 604 ms                                                           | 3.32 sec: 5.49x slower                                                       |
| async_tree_cpu_io_mixed_tg | 573 ms                                                           | 3.44 sec: 6.00x slower                                                       |
| async_tree_memoization     | 460 ms                                                           | 3.44 sec: 7.49x slower                                                       |
| async_tree_none            | 365 ms                                                           | 2.74 sec: 7.51x slower                                                       |
| async_tree_memoization_tg  | 421 ms                                                           | 3.53 sec: 8.39x slower                                                       |
| async_tree_none_tg         | 340 ms                                                           | 2.88 sec: 8.45x slower                                                       |
| async_tree_io              | 873 ms                                                           | 9.75 sec: 11.16x slower                                                      |
| async_tree_io_tg           | 900 ms                                                           | 10.2 sec: 11.34x slower                                                      |
| Geometric mean             | (ref)                                                            | 7.99x slower                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240320-pythonperf2-x86_64-python-dcaf33a41d5d220523d7-3.13.0a5+-dcaf33a |
|----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pidigits       | 254 ms                                                           | 261 ms: 1.03x slower                                                         |
| nbody          | 87.8 ms                                                          | 94.7 ms: 1.08x slower                                                        |
| float          | 80.2 ms                                                          | 154 ms: 1.92x slower                                                         |
| Geometric mean | (ref)                                                            | 1.29x slower                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240320-pythonperf2-x86_64-python-dcaf33a41d5d220523d7-3.13.0a5+-dcaf33a |
|----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_dna      | 249 ms                                                           | 241 ms: 1.03x faster                                                         |
| regex_v8       | 26.0 ms                                                          | 25.9 ms: 1.01x faster                                                        |
| regex_compile  | 144 ms                                                           | 146 ms: 1.01x slower                                                         |
| regex_effbot   | 3.40 ms                                                          | 3.57 ms: 1.05x slower                                                        |
| Geometric mean | (ref)                                                            | 1.01x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240320-pythonperf2-x86_64-python-dcaf33a41d5d220523d7-3.13.0a5+-dcaf33a |
|----------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| tomli_loads          | 2.40 sec                                                         | 2.15 sec: 1.12x faster                                                       |
| json_dumps           | 10.8 ms                                                          | 10.5 ms: 1.02x faster                                                        |
| unpickle             | 15.7 us                                                          | 15.4 us: 1.02x faster                                                        |
| unpickle_list        | 4.70 us                                                          | 4.64 us: 1.01x faster                                                        |
| json_loads           | 25.0 us                                                          | 24.8 us: 1.01x faster                                                        |
| pickle               | 10.6 us                                                          | 10.5 us: 1.01x faster                                                        |
| pickle_dict          | 32.8 us                                                          | 33.0 us: 1.00x slower                                                        |
| unpickle_pure_python | 224 us                                                           | 229 us: 1.02x slower                                                         |
| pickle_pure_python   | 307 us                                                           | 319 us: 1.04x slower                                                         |
| xml_etree_process    | 59.7 ms                                                          | 68.1 ms: 1.14x slower                                                        |
| xml_etree_generate   | 85.7 ms                                                          | 98.9 ms: 1.15x slower                                                        |
| xml_etree_parse      | 144 ms                                                           | 209 ms: 1.45x slower                                                         |
| xml_etree_iterparse  | 103 ms                                                           | 168 ms: 1.64x slower                                                         |
| Geometric mean       | (ref)                                                            | 1.08x slower                                                                 |

Benchmark hidden because not significant (1): pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240320-pythonperf2-x86_64-python-dcaf33a41d5d220523d7-3.13.0a5+-dcaf33a |
|------------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 13.2 ms                                                          | 14.5 ms: 1.10x slower                                                        |
| python_startup_no_site | 8.85 ms                                                          | 12.6 ms: 1.43x slower                                                        |
| Geometric mean         | (ref)                                                            | 1.25x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240320-pythonperf2-x86_64-python-dcaf33a41d5d220523d7-3.13.0a5+-dcaf33a |
|-----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 10.4 ms                                                          | 9.98 ms: 1.04x faster                                                        |
| django_template | 39.0 ms                                                          | 38.1 ms: 1.02x faster                                                        |
| genshi_text     | 25.9 ms                                                          | 29.5 ms: 1.14x slower                                                        |
| genshi_xml      | 58.1 ms                                                          | 66.9 ms: 1.15x slower                                                        |
| Geometric mean  | (ref)                                                            | 1.05x slower                                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240320-pythonperf2-x86_64-python-dcaf33a41d5d220523d7-3.13.0a5+-dcaf33a |
|----------------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 171 us                                                           | 115 us: 1.48x faster                                                         |
| create_gc_cycles           | 2.00 ms                                                          | 1.68 ms: 1.19x faster                                                        |
| tomli_loads                | 2.40 sec                                                         | 2.15 sec: 1.12x faster                                                       |
| richards_super             | 61.2 ms                                                          | 57.3 ms: 1.07x faster                                                        |
| gc_traversal               | 4.69 ms                                                          | 4.47 ms: 1.05x faster                                                        |
| telco                      | 8.40 ms                                                          | 8.07 ms: 1.04x faster                                                        |
| mako                       | 10.4 ms                                                          | 9.98 ms: 1.04x faster                                                        |
| richards                   | 53.4 ms                                                          | 51.5 ms: 1.04x faster                                                        |
| spectral_norm              | 97.3 ms                                                          | 93.8 ms: 1.04x faster                                                        |
| sqlite_synth               | 2.80 us                                                          | 2.71 us: 1.03x faster                                                        |
| regex_dna                  | 249 ms                                                           | 241 ms: 1.03x faster                                                         |
| coverage                   | 83.5 ms                                                          | 81.0 ms: 1.03x faster                                                        |
| chameleon                  | 7.40 ms                                                          | 7.21 ms: 1.03x faster                                                        |
| thrift                     | 880 us                                                           | 859 us: 1.02x faster                                                         |
| json_dumps                 | 10.8 ms                                                          | 10.5 ms: 1.02x faster                                                        |
| django_template            | 39.0 ms                                                          | 38.1 ms: 1.02x faster                                                        |
| asyncio_websockets         | 395 ms                                                           | 387 ms: 1.02x faster                                                         |
| unpickle                   | 15.7 us                                                          | 15.4 us: 1.02x faster                                                        |
| asyncio_tcp                | 378 ms                                                           | 371 ms: 1.02x faster                                                         |
| unpickle_list              | 4.70 us                                                          | 4.64 us: 1.01x faster                                                        |
| deepcopy_memo              | 37.3 us                                                          | 36.9 us: 1.01x faster                                                        |
| sqlglot_normalize          | 120 ms                                                           | 119 ms: 1.01x faster                                                         |
| json_loads                 | 25.0 us                                                          | 24.8 us: 1.01x faster                                                        |
| pickle                     | 10.6 us                                                          | 10.5 us: 1.01x faster                                                        |
| regex_v8                   | 26.0 ms                                                          | 25.9 ms: 1.01x faster                                                        |
| generators                 | 33.5 ms                                                          | 33.3 ms: 1.01x faster                                                        |
| asyncio_tcp_ssl            | 1.58 sec                                                         | 1.58 sec: 1.00x faster                                                       |
| pickle_dict                | 32.8 us                                                          | 33.0 us: 1.00x slower                                                        |
| deepcopy                   | 377 us                                                           | 379 us: 1.01x slower                                                         |
| logging_format             | 7.11 us                                                          | 7.16 us: 1.01x slower                                                        |
| regex_compile              | 144 ms                                                           | 146 ms: 1.01x slower                                                         |
| logging_silent             | 96.3 ns                                                          | 97.7 ns: 1.01x slower                                                        |
| pprint_safe_repr           | 818 ms                                                           | 830 ms: 1.02x slower                                                         |
| sympy_str                  | 295 ms                                                           | 300 ms: 1.02x slower                                                         |
| logging_simple             | 6.40 us                                                          | 6.52 us: 1.02x slower                                                        |
| unpickle_pure_python       | 224 us                                                           | 229 us: 1.02x slower                                                         |
| sympy_expand               | 501 ms                                                           | 511 ms: 1.02x slower                                                         |
| scimark_sparse_mat_mult    | 4.28 ms                                                          | 4.37 ms: 1.02x slower                                                        |
| dulwich_log                | 67.3 ms                                                          | 68.9 ms: 1.02x slower                                                        |
| pprint_pformat             | 1.66 sec                                                         | 1.70 sec: 1.02x slower                                                       |
| meteor_contest             | 128 ms                                                           | 131 ms: 1.02x slower                                                         |
| sympy_sum                  | 155 ms                                                           | 159 ms: 1.03x slower                                                         |
| pidigits                   | 254 ms                                                           | 261 ms: 1.03x slower                                                         |
| bench_thread_pool          | 908 us                                                           | 935 us: 1.03x slower                                                         |
| scimark_fft                | 312 ms                                                           | 322 ms: 1.03x slower                                                         |
| coroutines                 | 22.0 ms                                                          | 22.8 ms: 1.04x slower                                                        |
| pickle_pure_python         | 307 us                                                           | 319 us: 1.04x slower                                                         |
| sympy_integrate            | 23.2 ms                                                          | 24.3 ms: 1.05x slower                                                        |
| regex_effbot               | 3.40 ms                                                          | 3.57 ms: 1.05x slower                                                        |
| crypto_pyaes               | 73.6 ms                                                          | 77.8 ms: 1.06x slower                                                        |
| go                         | 165 ms                                                           | 175 ms: 1.06x slower                                                         |
| pyflate                    | 482 ms                                                           | 513 ms: 1.06x slower                                                         |
| tornado_http               | 119 ms                                                           | 128 ms: 1.07x slower                                                         |
| gunicorn                   | 1.04 ms                                                          | 1.12 ms: 1.07x slower                                                        |
| aiohttp                    | 1.07 ms                                                          | 1.15 ms: 1.07x slower                                                        |
| nbody                      | 87.8 ms                                                          | 94.7 ms: 1.08x slower                                                        |
| sqlglot_optimize           | 59.5 ms                                                          | 64.5 ms: 1.08x slower                                                        |
| mdp                        | 2.46 sec                                                         | 2.68 sec: 1.09x slower                                                       |
| python_startup             | 13.2 ms                                                          | 14.5 ms: 1.10x slower                                                        |
| html5lib                   | 74.7 ms                                                          | 82.5 ms: 1.11x slower                                                        |
| sqlglot_parse              | 1.39 ms                                                          | 1.55 ms: 1.12x slower                                                        |
| chaos                      | 59.6 ms                                                          | 66.7 ms: 1.12x slower                                                        |
| pathlib                    | 17.1 ms                                                          | 19.2 ms: 1.12x slower                                                        |
| fannkuch                   | 353 ms                                                           | 396 ms: 1.12x slower                                                         |
| comprehensions             | 17.0 us                                                          | 19.1 us: 1.12x slower                                                        |
| mypy2                      | 764 ms                                                           | 863 ms: 1.13x slower                                                         |
| hexiom                     | 6.35 ms                                                          | 7.21 ms: 1.14x slower                                                        |
| nqueens                    | 88.4 ms                                                          | 100 ms: 1.14x slower                                                         |
| genshi_text                | 25.9 ms                                                          | 29.5 ms: 1.14x slower                                                        |
| 2to3                       | 291 ms                                                           | 332 ms: 1.14x slower                                                         |
| xml_etree_process          | 59.7 ms                                                          | 68.1 ms: 1.14x slower                                                        |
| sqlglot_transpile          | 1.76 ms                                                          | 2.02 ms: 1.14x slower                                                        |
| genshi_xml                 | 58.1 ms                                                          | 66.9 ms: 1.15x slower                                                        |
| xml_etree_generate         | 85.7 ms                                                          | 98.9 ms: 1.15x slower                                                        |
| scimark_monte_carlo        | 65.5 ms                                                          | 76.6 ms: 1.17x slower                                                        |
| scimark_lu                 | 97.5 ms                                                          | 115 ms: 1.18x slower                                                         |
| raytrace                   | 260 ms                                                           | 310 ms: 1.19x slower                                                         |
| deltablue                  | 3.37 ms                                                          | 4.02 ms: 1.19x slower                                                        |
| scimark_sor                | 119 ms                                                           | 153 ms: 1.29x slower                                                         |
| async_generators           | 363 ms                                                           | 474 ms: 1.31x slower                                                         |
| pycparser                  | 1.22 sec                                                         | 1.60 sec: 1.31x slower                                                       |
| python_startup_no_site     | 8.85 ms                                                          | 12.6 ms: 1.43x slower                                                        |
| xml_etree_parse            | 144 ms                                                           | 209 ms: 1.45x slower                                                         |
| docutils                   | 2.98 sec                                                         | 4.70 sec: 1.57x slower                                                       |
| xml_etree_iterparse        | 103 ms                                                           | 168 ms: 1.64x slower                                                         |
| dask                       | 391 ms                                                           | 711 ms: 1.82x slower                                                         |
| float                      | 80.2 ms                                                          | 154 ms: 1.92x slower                                                         |
| pylint                     | 339 ms                                                           | 839 ms: 2.47x slower                                                         |
| async_tree_cpu_io_mixed    | 604 ms                                                           | 3.32 sec: 5.49x slower                                                       |
| async_tree_cpu_io_mixed_tg | 573 ms                                                           | 3.44 sec: 6.00x slower                                                       |
| async_tree_memoization     | 460 ms                                                           | 3.44 sec: 7.49x slower                                                       |
| async_tree_none            | 365 ms                                                           | 2.74 sec: 7.51x slower                                                       |
| async_tree_memoization_tg  | 421 ms                                                           | 3.53 sec: 8.39x slower                                                       |
| async_tree_none_tg         | 340 ms                                                           | 2.88 sec: 8.45x slower                                                       |
| async_tree_io              | 873 ms                                                           | 9.75 sec: 11.16x slower                                                      |
| async_tree_io_tg           | 900 ms                                                           | 10.2 sec: 11.34x slower                                                      |
| Geometric mean             | (ref)                                                            | 1.27x slower                                                                 |

Benchmark hidden because not significant (4): bench_mp_pool, deepcopy_reduce, pickle_list, json
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging
Ignored benchmarks (1) of results/bm-20240320-3.13.0a5+-dcaf33a-JIT/bm-20240320-pythonperf2-x86_64-python-dcaf33a41d5d220523d7-3.13.0a5+-dcaf33a.json: unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.09x