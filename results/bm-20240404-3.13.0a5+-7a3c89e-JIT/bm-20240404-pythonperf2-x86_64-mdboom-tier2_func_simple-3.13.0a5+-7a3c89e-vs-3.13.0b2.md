# Results vs. 3.13.0b2

- fork: mdboom
- ref: tier2_func_simple
- machine: linux-x86_64
- commit hash: 7a3c89e
- commit date: 2024-04-04
- overall geometric mean: 1.02x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.05x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-7a3c89e |
|----------------|:----------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 291 ms                                                           | 300 ms: 1.03x slower                                                      |
| chameleon      | 7.40 ms                                                          | 7.26 ms: 1.02x faster                                                     |
| docutils       | 2.98 sec                                                         | 3.07 sec: 1.03x slower                                                    |
| html5lib       | 74.7 ms                                                          | 73.6 ms: 1.01x faster                                                     |
| tornado_http   | 119 ms                                                           | 122 ms: 1.02x slower                                                      |
| Geometric mean | (ref)                                                            | 1.01x slower                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-7a3c89e |
|---------------------------|:----------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_memoization    | 460 ms                                                           | 440 ms: 1.04x faster                                                      |
| async_tree_none           | 365 ms                                                           | 358 ms: 1.02x faster                                                      |
| async_tree_cpu_io_mixed   | 604 ms                                                           | 595 ms: 1.02x faster                                                      |
| async_tree_memoization_tg | 421 ms                                                           | 437 ms: 1.04x slower                                                      |
| Geometric mean            | (ref)                                                            | 1.00x faster                                                              |

Benchmark hidden because not significant (4): async_tree_none_tg, async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-7a3c89e |
|----------------|:----------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| float          | 80.2 ms                                                          | 76.4 ms: 1.05x faster                                                     |
| pidigits       | 254 ms                                                           | 261 ms: 1.03x slower                                                      |
| nbody          | 87.8 ms                                                          | 97.8 ms: 1.11x slower                                                     |
| Geometric mean | (ref)                                                            | 1.03x slower                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-7a3c89e |
|----------------|:----------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_dna      | 249 ms                                                           | 242 ms: 1.03x faster                                                      |
| regex_v8       | 26.0 ms                                                          | 25.5 ms: 1.02x faster                                                     |
| regex_compile  | 144 ms                                                           | 148 ms: 1.03x slower                                                      |
| regex_effbot   | 3.40 ms                                                          | 3.72 ms: 1.09x slower                                                     |
| Geometric mean | (ref)                                                            | 1.02x slower                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-7a3c89e |
|----------------------|:----------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| tomli_loads          | 2.40 sec                                                         | 2.16 sec: 1.11x faster                                                    |
| unpickle             | 15.7 us                                                          | 15.1 us: 1.04x faster                                                     |
| unpickle_list        | 4.70 us                                                          | 4.63 us: 1.02x faster                                                     |
| xml_etree_process    | 59.7 ms                                                          | 59.0 ms: 1.01x faster                                                     |
| xml_etree_generate   | 85.7 ms                                                          | 84.9 ms: 1.01x faster                                                     |
| pickle_list          | 4.44 us                                                          | 4.41 us: 1.01x faster                                                     |
| pickle_pure_python   | 307 us                                                           | 305 us: 1.01x faster                                                      |
| xml_etree_parse      | 144 ms                                                           | 143 ms: 1.01x faster                                                      |
| json_dumps           | 10.8 ms                                                          | 10.8 ms: 1.01x slower                                                     |
| xml_etree_iterparse  | 103 ms                                                           | 103 ms: 1.01x slower                                                      |
| json_loads           | 25.0 us                                                          | 25.3 us: 1.01x slower                                                     |
| pickle               | 10.6 us                                                          | 10.9 us: 1.03x slower                                                     |
| unpickle_pure_python | 224 us                                                           | 233 us: 1.04x slower                                                      |
| Geometric mean       | (ref)                                                            | 1.01x faster                                                              |

Benchmark hidden because not significant (1): pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-7a3c89e |
|------------------------|:----------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup         | 13.2 ms                                                          | 13.5 ms: 1.02x slower                                                     |
| python_startup_no_site | 8.85 ms                                                          | 11.8 ms: 1.33x slower                                                     |
| Geometric mean         | (ref)                                                            | 1.17x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-7a3c89e |
|-----------------|:----------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| mako            | 10.4 ms                                                          | 9.96 ms: 1.04x faster                                                     |
| genshi_xml      | 58.1 ms                                                          | 57.5 ms: 1.01x faster                                                     |
| genshi_text     | 25.9 ms                                                          | 26.4 ms: 1.02x slower                                                     |
| django_template | 39.0 ms                                                          | 39.9 ms: 1.02x slower                                                     |
| Geometric mean  | (ref)                                                            | 1.00x faster                                                              |

All benchmarks:
===============

| Benchmark                 | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-7a3c89e |
|---------------------------|:----------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| typing_runtime_protocols  | 171 us                                                           | 120 us: 1.42x faster                                                      |
| create_gc_cycles          | 2.00 ms                                                          | 1.79 ms: 1.12x faster                                                     |
| tomli_loads               | 2.40 sec                                                         | 2.16 sec: 1.11x faster                                                    |
| gc_traversal              | 4.69 ms                                                          | 4.35 ms: 1.08x faster                                                     |
| richards_super            | 61.2 ms                                                          | 57.1 ms: 1.07x faster                                                     |
| richards                  | 53.4 ms                                                          | 50.2 ms: 1.06x faster                                                     |
| float                     | 80.2 ms                                                          | 76.4 ms: 1.05x faster                                                     |
| scimark_sparse_mat_mult   | 4.28 ms                                                          | 4.09 ms: 1.05x faster                                                     |
| async_tree_memoization    | 460 ms                                                           | 440 ms: 1.04x faster                                                      |
| mako                      | 10.4 ms                                                          | 9.96 ms: 1.04x faster                                                     |
| unpickle                  | 15.7 us                                                          | 15.1 us: 1.04x faster                                                     |
| coverage                  | 83.5 ms                                                          | 80.6 ms: 1.04x faster                                                     |
| sqlite_synth              | 2.80 us                                                          | 2.70 us: 1.03x faster                                                     |
| spectral_norm             | 97.3 ms                                                          | 94.3 ms: 1.03x faster                                                     |
| regex_dna                 | 249 ms                                                           | 242 ms: 1.03x faster                                                      |
| telco                     | 8.40 ms                                                          | 8.22 ms: 1.02x faster                                                     |
| regex_v8                  | 26.0 ms                                                          | 25.5 ms: 1.02x faster                                                     |
| async_tree_none           | 365 ms                                                           | 358 ms: 1.02x faster                                                      |
| asyncio_websockets        | 395 ms                                                           | 387 ms: 1.02x faster                                                      |
| chameleon                 | 7.40 ms                                                          | 7.26 ms: 1.02x faster                                                     |
| async_tree_cpu_io_mixed   | 604 ms                                                           | 595 ms: 1.02x faster                                                      |
| asyncio_tcp               | 378 ms                                                           | 372 ms: 1.02x faster                                                      |
| unpickle_list             | 4.70 us                                                          | 4.63 us: 1.02x faster                                                     |
| html5lib                  | 74.7 ms                                                          | 73.6 ms: 1.01x faster                                                     |
| xml_etree_process         | 59.7 ms                                                          | 59.0 ms: 1.01x faster                                                     |
| xml_etree_generate        | 85.7 ms                                                          | 84.9 ms: 1.01x faster                                                     |
| genshi_xml                | 58.1 ms                                                          | 57.5 ms: 1.01x faster                                                     |
| pickle_list               | 4.44 us                                                          | 4.41 us: 1.01x faster                                                     |
| pickle_pure_python        | 307 us                                                           | 305 us: 1.01x faster                                                      |
| xml_etree_parse           | 144 ms                                                           | 143 ms: 1.01x faster                                                      |
| sqlglot_parse             | 1.39 ms                                                          | 1.40 ms: 1.01x slower                                                     |
| json_dumps                | 10.8 ms                                                          | 10.8 ms: 1.01x slower                                                     |
| xml_etree_iterparse       | 103 ms                                                           | 103 ms: 1.01x slower                                                      |
| logging_silent            | 96.3 ns                                                          | 97.0 ns: 1.01x slower                                                     |
| sympy_expand              | 501 ms                                                           | 507 ms: 1.01x slower                                                      |
| json_loads                | 25.0 us                                                          | 25.3 us: 1.01x slower                                                     |
| sqlglot_normalize         | 120 ms                                                           | 122 ms: 1.01x slower                                                      |
| sqlglot_transpile         | 1.76 ms                                                          | 1.79 ms: 1.02x slower                                                     |
| thrift                    | 880 us                                                           | 893 us: 1.02x slower                                                      |
| deepcopy_reduce           | 3.39 us                                                          | 3.45 us: 1.02x slower                                                     |
| deepcopy                  | 377 us                                                           | 384 us: 1.02x slower                                                      |
| coroutines                | 22.0 ms                                                          | 22.4 ms: 1.02x slower                                                     |
| genshi_text               | 25.9 ms                                                          | 26.4 ms: 1.02x slower                                                     |
| pprint_safe_repr          | 818 ms                                                           | 834 ms: 1.02x slower                                                      |
| pycparser                 | 1.22 sec                                                         | 1.25 sec: 1.02x slower                                                    |
| python_startup            | 13.2 ms                                                          | 13.5 ms: 1.02x slower                                                     |
| tornado_http              | 119 ms                                                           | 122 ms: 1.02x slower                                                      |
| django_template           | 39.0 ms                                                          | 39.9 ms: 1.02x slower                                                     |
| sympy_str                 | 295 ms                                                           | 301 ms: 1.02x slower                                                      |
| deepcopy_memo             | 37.3 us                                                          | 38.2 us: 1.02x slower                                                     |
| logging_format            | 7.11 us                                                          | 7.29 us: 1.03x slower                                                     |
| docutils                  | 2.98 sec                                                         | 3.07 sec: 1.03x slower                                                    |
| regex_compile             | 144 ms                                                           | 148 ms: 1.03x slower                                                      |
| pickle                    | 10.6 us                                                          | 10.9 us: 1.03x slower                                                     |
| pyflate                   | 482 ms                                                           | 496 ms: 1.03x slower                                                      |
| pidigits                  | 254 ms                                                           | 261 ms: 1.03x slower                                                      |
| 2to3                      | 291 ms                                                           | 300 ms: 1.03x slower                                                      |
| pprint_pformat            | 1.66 sec                                                         | 1.71 sec: 1.03x slower                                                    |
| meteor_contest            | 128 ms                                                           | 132 ms: 1.03x slower                                                      |
| dulwich_log               | 67.3 ms                                                          | 69.7 ms: 1.04x slower                                                     |
| logging_simple            | 6.40 us                                                          | 6.64 us: 1.04x slower                                                     |
| dask                      | 391 ms                                                           | 406 ms: 1.04x slower                                                      |
| unpickle_pure_python      | 224 us                                                           | 233 us: 1.04x slower                                                      |
| async_tree_memoization_tg | 421 ms                                                           | 437 ms: 1.04x slower                                                      |
| sympy_sum                 | 155 ms                                                           | 161 ms: 1.04x slower                                                      |
| gunicorn                  | 1.04 ms                                                          | 1.09 ms: 1.05x slower                                                     |
| go                        | 165 ms                                                           | 173 ms: 1.05x slower                                                      |
| aiohttp                   | 1.07 ms                                                          | 1.12 ms: 1.05x slower                                                     |
| crypto_pyaes              | 73.6 ms                                                          | 77.4 ms: 1.05x slower                                                     |
| sqlglot_optimize          | 59.5 ms                                                          | 62.8 ms: 1.05x slower                                                     |
| async_generators          | 363 ms                                                           | 385 ms: 1.06x slower                                                      |
| pylint                    | 339 ms                                                           | 363 ms: 1.07x slower                                                      |
| mdp                       | 2.46 sec                                                         | 2.65 sec: 1.08x slower                                                    |
| sympy_integrate           | 23.2 ms                                                          | 25.0 ms: 1.08x slower                                                     |
| mypy2                     | 764 ms                                                           | 824 ms: 1.08x slower                                                      |
| fannkuch                  | 353 ms                                                           | 384 ms: 1.09x slower                                                      |
| regex_effbot              | 3.40 ms                                                          | 3.72 ms: 1.09x slower                                                     |
| deltablue                 | 3.37 ms                                                          | 3.72 ms: 1.10x slower                                                     |
| nbody                     | 87.8 ms                                                          | 97.8 ms: 1.11x slower                                                     |
| chaos                     | 59.6 ms                                                          | 66.6 ms: 1.12x slower                                                     |
| scimark_monte_carlo       | 65.5 ms                                                          | 73.7 ms: 1.13x slower                                                     |
| pathlib                   | 17.1 ms                                                          | 19.4 ms: 1.13x slower                                                     |
| nqueens                   | 88.4 ms                                                          | 103 ms: 1.16x slower                                                      |
| comprehensions            | 17.0 us                                                          | 19.7 us: 1.16x slower                                                     |
| raytrace                  | 260 ms                                                           | 305 ms: 1.17x slower                                                      |
| hexiom                    | 6.35 ms                                                          | 7.52 ms: 1.18x slower                                                     |
| scimark_lu                | 97.5 ms                                                          | 119 ms: 1.22x slower                                                      |
| bench_thread_pool         | 908 us                                                           | 1.12 ms: 1.23x slower                                                     |
| scimark_sor               | 119 ms                                                           | 153 ms: 1.29x slower                                                      |
| python_startup_no_site    | 8.85 ms                                                          | 11.8 ms: 1.33x slower                                                     |
| Geometric mean            | (ref)                                                            | 1.02x slower                                                              |

Benchmark hidden because not significant (10): async_tree_none_tg, asyncio_tcp_ssl, generators, pickle_dict, scimark_fft, json, async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_io, bench_mp_pool
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.05x