# Results vs. 3.13.0b2

- fork: python
- ref: bfc57d43d8766120ba0c
- machine: linux-x86_64
- commit hash: bfc57d4
- commit date: 2024-03-29
- overall geometric mean: 1.03x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.06x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 291 ms                                                           | 300 ms: 1.03x slower                                                         |
| chameleon      | 7.40 ms                                                          | 7.58 ms: 1.02x slower                                                        |
| docutils       | 2.98 sec                                                         | 3.08 sec: 1.03x slower                                                       |
| tornado_http   | 119 ms                                                           | 124 ms: 1.04x slower                                                         |
| Geometric mean | (ref)                                                            | 1.02x slower                                                                 |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|---------------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_memoization    | 460 ms                                                           | 440 ms: 1.05x faster                                                         |
| async_tree_none           | 365 ms                                                           | 358 ms: 1.02x faster                                                         |
| async_tree_cpu_io_mixed   | 604 ms                                                           | 592 ms: 1.02x faster                                                         |
| async_tree_memoization_tg | 421 ms                                                           | 435 ms: 1.03x slower                                                         |
| Geometric mean            | (ref)                                                            | 1.01x faster                                                                 |

Benchmark hidden because not significant (4): async_tree_none_tg, async_tree_io_tg, async_tree_cpu_io_mixed_tg, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 80.2 ms                                                          | 78.5 ms: 1.02x faster                                                        |
| pidigits       | 254 ms                                                           | 261 ms: 1.03x slower                                                         |
| nbody          | 87.8 ms                                                          | 94.9 ms: 1.08x slower                                                        |
| Geometric mean | (ref)                                                            | 1.03x slower                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_dna      | 249 ms                                                           | 242 ms: 1.03x faster                                                         |
| regex_v8       | 26.0 ms                                                          | 25.6 ms: 1.02x faster                                                        |
| regex_compile  | 144 ms                                                           | 148 ms: 1.03x slower                                                         |
| regex_effbot   | 3.40 ms                                                          | 3.70 ms: 1.09x slower                                                        |
| Geometric mean | (ref)                                                            | 1.02x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| tomli_loads          | 2.40 sec                                                         | 2.17 sec: 1.11x faster                                                       |
| unpickle             | 15.7 us                                                          | 15.2 us: 1.03x faster                                                        |
| json_dumps           | 10.8 ms                                                          | 10.5 ms: 1.03x faster                                                        |
| xml_etree_process    | 59.7 ms                                                          | 58.3 ms: 1.02x faster                                                        |
| xml_etree_generate   | 85.7 ms                                                          | 84.1 ms: 1.02x faster                                                        |
| unpickle_list        | 4.70 us                                                          | 4.62 us: 1.02x faster                                                        |
| pickle_list          | 4.44 us                                                          | 4.42 us: 1.01x faster                                                        |
| pickle_dict          | 32.8 us                                                          | 33.1 us: 1.01x slower                                                        |
| pickle_pure_python   | 307 us                                                           | 311 us: 1.01x slower                                                         |
| json_loads           | 25.0 us                                                          | 25.3 us: 1.01x slower                                                        |
| pickle               | 10.6 us                                                          | 10.9 us: 1.03x slower                                                        |
| unpickle_pure_python | 224 us                                                           | 235 us: 1.05x slower                                                         |
| Geometric mean       | (ref)                                                            | 1.01x faster                                                                 |

Benchmark hidden because not significant (2): xml_etree_parse, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|------------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 13.2 ms                                                          | 13.6 ms: 1.03x slower                                                        |
| python_startup_no_site | 8.85 ms                                                          | 11.8 ms: 1.34x slower                                                        |
| Geometric mean         | (ref)                                                            | 1.17x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|-----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 10.4 ms                                                          | 10.0 ms: 1.04x faster                                                        |
| genshi_xml      | 58.1 ms                                                          | 59.4 ms: 1.02x slower                                                        |
| django_template | 39.0 ms                                                          | 40.1 ms: 1.03x slower                                                        |
| genshi_text     | 25.9 ms                                                          | 27.4 ms: 1.06x slower                                                        |
| Geometric mean  | (ref)                                                            | 1.02x slower                                                                 |

All benchmarks:
===============

| Benchmark                 | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|---------------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols  | 171 us                                                           | 128 us: 1.34x faster                                                         |
| create_gc_cycles          | 2.00 ms                                                          | 1.80 ms: 1.11x faster                                                        |
| tomli_loads               | 2.40 sec                                                         | 2.17 sec: 1.11x faster                                                       |
| telco                     | 8.40 ms                                                          | 8.00 ms: 1.05x faster                                                        |
| richards_super            | 61.2 ms                                                          | 58.4 ms: 1.05x faster                                                        |
| async_tree_memoization    | 460 ms                                                           | 440 ms: 1.05x faster                                                         |
| spectral_norm             | 97.3 ms                                                          | 93.2 ms: 1.04x faster                                                        |
| richards                  | 53.4 ms                                                          | 51.3 ms: 1.04x faster                                                        |
| scimark_sparse_mat_mult   | 4.28 ms                                                          | 4.11 ms: 1.04x faster                                                        |
| sqlite_synth              | 2.80 us                                                          | 2.70 us: 1.04x faster                                                        |
| mako                      | 10.4 ms                                                          | 10.0 ms: 1.04x faster                                                        |
| unpickle                  | 15.7 us                                                          | 15.2 us: 1.03x faster                                                        |
| regex_dna                 | 249 ms                                                           | 242 ms: 1.03x faster                                                         |
| json_dumps                | 10.8 ms                                                          | 10.5 ms: 1.03x faster                                                        |
| xml_etree_process         | 59.7 ms                                                          | 58.3 ms: 1.02x faster                                                        |
| gc_traversal              | 4.69 ms                                                          | 4.57 ms: 1.02x faster                                                        |
| async_tree_none           | 365 ms                                                           | 358 ms: 1.02x faster                                                         |
| async_tree_cpu_io_mixed   | 604 ms                                                           | 592 ms: 1.02x faster                                                         |
| float                     | 80.2 ms                                                          | 78.5 ms: 1.02x faster                                                        |
| asyncio_websockets        | 395 ms                                                           | 387 ms: 1.02x faster                                                         |
| xml_etree_generate        | 85.7 ms                                                          | 84.1 ms: 1.02x faster                                                        |
| asyncio_tcp               | 378 ms                                                           | 371 ms: 1.02x faster                                                         |
| unpickle_list             | 4.70 us                                                          | 4.62 us: 1.02x faster                                                        |
| regex_v8                  | 26.0 ms                                                          | 25.6 ms: 1.02x faster                                                        |
| coverage                  | 83.5 ms                                                          | 82.4 ms: 1.01x faster                                                        |
| pickle_list               | 4.44 us                                                          | 4.42 us: 1.01x faster                                                        |
| generators                | 33.5 ms                                                          | 33.6 ms: 1.00x slower                                                        |
| pickle_dict               | 32.8 us                                                          | 33.1 us: 1.01x slower                                                        |
| pickle_pure_python        | 307 us                                                           | 311 us: 1.01x slower                                                         |
| json_loads                | 25.0 us                                                          | 25.3 us: 1.01x slower                                                        |
| json                      | 5.35 ms                                                          | 5.44 ms: 1.02x slower                                                        |
| logging_format            | 7.11 us                                                          | 7.24 us: 1.02x slower                                                        |
| logging_silent            | 96.3 ns                                                          | 98.3 ns: 1.02x slower                                                        |
| pprint_safe_repr          | 818 ms                                                           | 836 ms: 1.02x slower                                                         |
| genshi_xml                | 58.1 ms                                                          | 59.4 ms: 1.02x slower                                                        |
| chameleon                 | 7.40 ms                                                          | 7.58 ms: 1.02x slower                                                        |
| sympy_expand              | 501 ms                                                           | 513 ms: 1.02x slower                                                         |
| sqlglot_parse             | 1.39 ms                                                          | 1.43 ms: 1.03x slower                                                        |
| python_startup            | 13.2 ms                                                          | 13.6 ms: 1.03x slower                                                        |
| pickle                    | 10.6 us                                                          | 10.9 us: 1.03x slower                                                        |
| deepcopy_reduce           | 3.39 us                                                          | 3.48 us: 1.03x slower                                                        |
| dulwich_log               | 67.3 ms                                                          | 69.2 ms: 1.03x slower                                                        |
| dask                      | 391 ms                                                           | 402 ms: 1.03x slower                                                         |
| 2to3                      | 291 ms                                                           | 300 ms: 1.03x slower                                                         |
| pidigits                  | 254 ms                                                           | 261 ms: 1.03x slower                                                         |
| regex_compile             | 144 ms                                                           | 148 ms: 1.03x slower                                                         |
| django_template           | 39.0 ms                                                          | 40.1 ms: 1.03x slower                                                        |
| pprint_pformat            | 1.66 sec                                                         | 1.71 sec: 1.03x slower                                                       |
| docutils                  | 2.98 sec                                                         | 3.08 sec: 1.03x slower                                                       |
| sympy_str                 | 295 ms                                                           | 304 ms: 1.03x slower                                                         |
| logging_simple            | 6.40 us                                                          | 6.61 us: 1.03x slower                                                        |
| coroutines                | 22.0 ms                                                          | 22.7 ms: 1.03x slower                                                        |
| async_tree_memoization_tg | 421 ms                                                           | 435 ms: 1.03x slower                                                         |
| pycparser                 | 1.22 sec                                                         | 1.26 sec: 1.03x slower                                                       |
| sqlglot_transpile         | 1.76 ms                                                          | 1.83 ms: 1.04x slower                                                        |
| sqlglot_normalize         | 120 ms                                                           | 125 ms: 1.04x slower                                                         |
| tornado_http              | 119 ms                                                           | 124 ms: 1.04x slower                                                         |
| sympy_sum                 | 155 ms                                                           | 161 ms: 1.04x slower                                                         |
| gunicorn                  | 1.04 ms                                                          | 1.09 ms: 1.04x slower                                                        |
| aiohttp                   | 1.07 ms                                                          | 1.12 ms: 1.05x slower                                                        |
| meteor_contest            | 128 ms                                                           | 134 ms: 1.05x slower                                                         |
| crypto_pyaes              | 73.6 ms                                                          | 77.1 ms: 1.05x slower                                                        |
| unpickle_pure_python      | 224 us                                                           | 235 us: 1.05x slower                                                         |
| deepcopy                  | 377 us                                                           | 398 us: 1.06x slower                                                         |
| genshi_text               | 25.9 ms                                                          | 27.4 ms: 1.06x slower                                                        |
| sqlglot_optimize          | 59.5 ms                                                          | 63.1 ms: 1.06x slower                                                        |
| go                        | 165 ms                                                           | 175 ms: 1.06x slower                                                         |
| mdp                       | 2.46 sec                                                         | 2.62 sec: 1.06x slower                                                       |
| pyflate                   | 482 ms                                                           | 514 ms: 1.07x slower                                                         |
| deepcopy_memo             | 37.3 us                                                          | 39.9 us: 1.07x slower                                                        |
| fannkuch                  | 353 ms                                                           | 379 ms: 1.07x slower                                                         |
| nbody                     | 87.8 ms                                                          | 94.9 ms: 1.08x slower                                                        |
| mypy2                     | 764 ms                                                           | 830 ms: 1.09x slower                                                         |
| async_generators          | 363 ms                                                           | 395 ms: 1.09x slower                                                         |
| regex_effbot              | 3.40 ms                                                          | 3.70 ms: 1.09x slower                                                        |
| sympy_integrate           | 23.2 ms                                                          | 25.3 ms: 1.09x slower                                                        |
| deltablue                 | 3.37 ms                                                          | 3.75 ms: 1.11x slower                                                        |
| scimark_monte_carlo       | 65.5 ms                                                          | 72.9 ms: 1.11x slower                                                        |
| chaos                     | 59.6 ms                                                          | 67.9 ms: 1.14x slower                                                        |
| pathlib                   | 17.1 ms                                                          | 19.8 ms: 1.15x slower                                                        |
| nqueens                   | 88.4 ms                                                          | 103 ms: 1.16x slower                                                         |
| raytrace                  | 260 ms                                                           | 304 ms: 1.17x slower                                                         |
| comprehensions            | 17.0 us                                                          | 20.1 us: 1.19x slower                                                        |
| hexiom                    | 6.35 ms                                                          | 7.59 ms: 1.20x slower                                                        |
| bench_thread_pool         | 908 us                                                           | 1.13 ms: 1.24x slower                                                        |
| scimark_sor               | 119 ms                                                           | 154 ms: 1.29x slower                                                         |
| scimark_lu                | 97.5 ms                                                          | 127 ms: 1.30x slower                                                         |
| python_startup_no_site    | 8.85 ms                                                          | 11.8 ms: 1.34x slower                                                        |
| Geometric mean            | (ref)                                                            | 1.03x slower                                                                 |

Benchmark hidden because not significant (12): async_tree_none_tg, html5lib, xml_etree_parse, thrift, xml_etree_iterparse, pylint, asyncio_tcp_ssl, async_tree_io_tg, async_tree_cpu_io_mixed_tg, async_tree_io, bench_mp_pool, scimark_fft
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging
Ignored benchmarks (1) of results/bm-20240329-3.13.0a5+-bfc57d4-JIT/bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4.json: unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.06x