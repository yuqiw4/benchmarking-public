# Results vs. 3.13.0b2

- fork: mdboom
- ref: tier2_funcs
- machine: linux-x86_64
- commit hash: 27267d7
- commit date: 2024-04-03
- overall geometric mean: 1.03x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.05x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-27267d7 |
|----------------|:----------------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 291 ms                                                           | 300 ms: 1.03x slower                                                |
| chameleon      | 7.40 ms                                                          | 7.44 ms: 1.01x slower                                               |
| docutils       | 2.98 sec                                                         | 3.07 sec: 1.03x slower                                              |
| html5lib       | 74.7 ms                                                          | 73.8 ms: 1.01x faster                                               |
| tornado_http   | 119 ms                                                           | 123 ms: 1.03x slower                                                |
| Geometric mean | (ref)                                                            | 1.02x slower                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-27267d7 |
|---------------------------|:----------------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_memoization    | 460 ms                                                           | 443 ms: 1.04x faster                                                |
| async_tree_memoization_tg | 421 ms                                                           | 439 ms: 1.04x slower                                                |
| Geometric mean            | (ref)                                                            | 1.00x slower                                                        |

Benchmark hidden because not significant (6): async_tree_none, async_tree_cpu_io_mixed, async_tree_none_tg, async_tree_io_tg, async_tree_cpu_io_mixed_tg, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-27267d7 |
|----------------|:----------------------------------------------------------------:|:-------------------------------------------------------------------:|
| float          | 80.2 ms                                                          | 77.6 ms: 1.03x faster                                               |
| pidigits       | 254 ms                                                           | 261 ms: 1.03x slower                                                |
| nbody          | 87.8 ms                                                          | 98.4 ms: 1.12x slower                                               |
| Geometric mean | (ref)                                                            | 1.04x slower                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-27267d7 |
|----------------|:----------------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_dna      | 249 ms                                                           | 241 ms: 1.03x faster                                                |
| regex_compile  | 144 ms                                                           | 150 ms: 1.04x slower                                                |
| regex_effbot   | 3.40 ms                                                          | 3.57 ms: 1.05x slower                                               |
| Geometric mean | (ref)                                                            | 1.01x slower                                                        |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-27267d7 |
|----------------------|:----------------------------------------------------------------:|:-------------------------------------------------------------------:|
| tomli_loads          | 2.40 sec                                                         | 2.15 sec: 1.12x faster                                              |
| pickle_dict          | 32.8 us                                                          | 31.0 us: 1.06x faster                                               |
| unpickle             | 15.7 us                                                          | 15.1 us: 1.04x faster                                               |
| unpickle_list        | 4.70 us                                                          | 4.55 us: 1.03x faster                                               |
| xml_etree_process    | 59.7 ms                                                          | 58.2 ms: 1.03x faster                                               |
| pickle               | 10.6 us                                                          | 10.5 us: 1.01x faster                                               |
| xml_etree_generate   | 85.7 ms                                                          | 85.2 ms: 1.01x faster                                               |
| pickle_pure_python   | 307 us                                                           | 306 us: 1.00x faster                                                |
| json_loads           | 25.0 us                                                          | 25.2 us: 1.01x slower                                               |
| xml_etree_parse      | 144 ms                                                           | 146 ms: 1.02x slower                                                |
| xml_etree_iterparse  | 103 ms                                                           | 104 ms: 1.02x slower                                                |
| unpickle_pure_python | 224 us                                                           | 240 us: 1.07x slower                                                |
| Geometric mean       | (ref)                                                            | 1.01x faster                                                        |

Benchmark hidden because not significant (2): json_dumps, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-27267d7 |
|------------------------|:----------------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup         | 13.2 ms                                                          | 13.5 ms: 1.02x slower                                               |
| python_startup_no_site | 8.85 ms                                                          | 11.8 ms: 1.33x slower                                               |
| Geometric mean         | (ref)                                                            | 1.17x slower                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-27267d7 |
|-----------------|:----------------------------------------------------------------:|:-------------------------------------------------------------------:|
| mako            | 10.4 ms                                                          | 10.1 ms: 1.03x faster                                               |
| genshi_xml      | 58.1 ms                                                          | 58.8 ms: 1.01x slower                                               |
| django_template | 39.0 ms                                                          | 40.1 ms: 1.03x slower                                               |
| genshi_text     | 25.9 ms                                                          | 27.2 ms: 1.05x slower                                               |
| Geometric mean  | (ref)                                                            | 1.02x slower                                                        |

All benchmarks:
===============

| Benchmark                 | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-27267d7 |
|---------------------------|:----------------------------------------------------------------:|:-------------------------------------------------------------------:|
| typing_runtime_protocols  | 171 us                                                           | 121 us: 1.40x faster                                                |
| tomli_loads               | 2.40 sec                                                         | 2.15 sec: 1.12x faster                                              |
| create_gc_cycles          | 2.00 ms                                                          | 1.82 ms: 1.10x faster                                               |
| pickle_dict               | 32.8 us                                                          | 31.0 us: 1.06x faster                                               |
| sqlite_synth              | 2.80 us                                                          | 2.69 us: 1.04x faster                                               |
| unpickle                  | 15.7 us                                                          | 15.1 us: 1.04x faster                                               |
| async_tree_memoization    | 460 ms                                                           | 443 ms: 1.04x faster                                                |
| scimark_sparse_mat_mult   | 4.28 ms                                                          | 4.13 ms: 1.04x faster                                               |
| float                     | 80.2 ms                                                          | 77.6 ms: 1.03x faster                                               |
| unpickle_list             | 4.70 us                                                          | 4.55 us: 1.03x faster                                               |
| regex_dna                 | 249 ms                                                           | 241 ms: 1.03x faster                                                |
| mako                      | 10.4 ms                                                          | 10.1 ms: 1.03x faster                                               |
| richards_super            | 61.2 ms                                                          | 59.4 ms: 1.03x faster                                               |
| telco                     | 8.40 ms                                                          | 8.18 ms: 1.03x faster                                               |
| xml_etree_process         | 59.7 ms                                                          | 58.2 ms: 1.03x faster                                               |
| asyncio_tcp               | 378 ms                                                           | 371 ms: 1.02x faster                                                |
| spectral_norm             | 97.3 ms                                                          | 95.7 ms: 1.02x faster                                               |
| asyncio_websockets        | 395 ms                                                           | 389 ms: 1.02x faster                                                |
| html5lib                  | 74.7 ms                                                          | 73.8 ms: 1.01x faster                                               |
| richards                  | 53.4 ms                                                          | 52.9 ms: 1.01x faster                                               |
| pickle                    | 10.6 us                                                          | 10.5 us: 1.01x faster                                               |
| xml_etree_generate        | 85.7 ms                                                          | 85.2 ms: 1.01x faster                                               |
| generators                | 33.5 ms                                                          | 33.3 ms: 1.01x faster                                               |
| deepcopy_reduce           | 3.39 us                                                          | 3.37 us: 1.01x faster                                               |
| pickle_pure_python        | 307 us                                                           | 306 us: 1.00x faster                                                |
| json                      | 5.35 ms                                                          | 5.38 ms: 1.00x slower                                               |
| json_loads                | 25.0 us                                                          | 25.2 us: 1.01x slower                                               |
| sqlglot_parse             | 1.39 ms                                                          | 1.40 ms: 1.01x slower                                               |
| chameleon                 | 7.40 ms                                                          | 7.44 ms: 1.01x slower                                               |
| thrift                    | 880 us                                                           | 887 us: 1.01x slower                                                |
| logging_silent            | 96.3 ns                                                          | 97.2 ns: 1.01x slower                                               |
| pprint_safe_repr          | 818 ms                                                           | 827 ms: 1.01x slower                                                |
| genshi_xml                | 58.1 ms                                                          | 58.8 ms: 1.01x slower                                               |
| xml_etree_parse           | 144 ms                                                           | 146 ms: 1.02x slower                                                |
| xml_etree_iterparse       | 103 ms                                                           | 104 ms: 1.02x slower                                                |
| sympy_expand              | 501 ms                                                           | 510 ms: 1.02x slower                                                |
| sqlglot_transpile         | 1.76 ms                                                          | 1.80 ms: 1.02x slower                                               |
| sqlglot_normalize         | 120 ms                                                           | 123 ms: 1.02x slower                                                |
| gc_traversal              | 4.69 ms                                                          | 4.80 ms: 1.02x slower                                               |
| python_startup            | 13.2 ms                                                          | 13.5 ms: 1.02x slower                                               |
| sympy_str                 | 295 ms                                                           | 302 ms: 1.03x slower                                                |
| deepcopy                  | 377 us                                                           | 388 us: 1.03x slower                                                |
| dulwich_log               | 67.3 ms                                                          | 69.2 ms: 1.03x slower                                               |
| docutils                  | 2.98 sec                                                         | 3.07 sec: 1.03x slower                                              |
| pidigits                  | 254 ms                                                           | 261 ms: 1.03x slower                                                |
| django_template           | 39.0 ms                                                          | 40.1 ms: 1.03x slower                                               |
| 2to3                      | 291 ms                                                           | 300 ms: 1.03x slower                                                |
| tornado_http              | 119 ms                                                           | 123 ms: 1.03x slower                                                |
| deepcopy_memo             | 37.3 us                                                          | 38.5 us: 1.03x slower                                               |
| dask                      | 391 ms                                                           | 403 ms: 1.03x slower                                                |
| pycparser                 | 1.22 sec                                                         | 1.26 sec: 1.03x slower                                              |
| meteor_contest            | 128 ms                                                           | 132 ms: 1.03x slower                                                |
| logging_format            | 7.11 us                                                          | 7.37 us: 1.04x slower                                               |
| regex_compile             | 144 ms                                                           | 150 ms: 1.04x slower                                                |
| async_tree_memoization_tg | 421 ms                                                           | 439 ms: 1.04x slower                                                |
| pprint_pformat            | 1.66 sec                                                         | 1.73 sec: 1.04x slower                                              |
| coroutines                | 22.0 ms                                                          | 22.9 ms: 1.04x slower                                               |
| pyflate                   | 482 ms                                                           | 502 ms: 1.04x slower                                                |
| gunicorn                  | 1.04 ms                                                          | 1.09 ms: 1.04x slower                                               |
| sympy_sum                 | 155 ms                                                           | 162 ms: 1.05x slower                                                |
| genshi_text               | 25.9 ms                                                          | 27.2 ms: 1.05x slower                                               |
| aiohttp                   | 1.07 ms                                                          | 1.13 ms: 1.05x slower                                               |
| regex_effbot              | 3.40 ms                                                          | 3.57 ms: 1.05x slower                                               |
| sqlglot_optimize          | 59.5 ms                                                          | 62.6 ms: 1.05x slower                                               |
| go                        | 165 ms                                                           | 174 ms: 1.05x slower                                                |
| crypto_pyaes              | 73.6 ms                                                          | 77.9 ms: 1.06x slower                                               |
| mdp                       | 2.46 sec                                                         | 2.62 sec: 1.06x slower                                              |
| logging_simple            | 6.40 us                                                          | 6.82 us: 1.07x slower                                               |
| unpickle_pure_python      | 224 us                                                           | 240 us: 1.07x slower                                                |
| fannkuch                  | 353 ms                                                           | 378 ms: 1.07x slower                                                |
| async_generators          | 363 ms                                                           | 391 ms: 1.08x slower                                                |
| pylint                    | 339 ms                                                           | 366 ms: 1.08x slower                                                |
| mypy2                     | 764 ms                                                           | 826 ms: 1.08x slower                                                |
| sympy_integrate           | 23.2 ms                                                          | 25.3 ms: 1.09x slower                                               |
| deltablue                 | 3.37 ms                                                          | 3.73 ms: 1.11x slower                                               |
| chaos                     | 59.6 ms                                                          | 66.8 ms: 1.12x slower                                               |
| nbody                     | 87.8 ms                                                          | 98.4 ms: 1.12x slower                                               |
| scimark_monte_carlo       | 65.5 ms                                                          | 74.4 ms: 1.14x slower                                               |
| pathlib                   | 17.1 ms                                                          | 19.8 ms: 1.15x slower                                               |
| raytrace                  | 260 ms                                                           | 302 ms: 1.16x slower                                                |
| comprehensions            | 17.0 us                                                          | 20.0 us: 1.18x slower                                               |
| nqueens                   | 88.4 ms                                                          | 104 ms: 1.18x slower                                                |
| hexiom                    | 6.35 ms                                                          | 7.56 ms: 1.19x slower                                               |
| bench_thread_pool         | 908 us                                                           | 1.12 ms: 1.23x slower                                               |
| scimark_lu                | 97.5 ms                                                          | 125 ms: 1.28x slower                                                |
| scimark_sor               | 119 ms                                                           | 155 ms: 1.31x slower                                                |
| python_startup_no_site    | 8.85 ms                                                          | 11.8 ms: 1.33x slower                                               |
| Geometric mean            | (ref)                                                            | 1.03x slower                                                        |

Benchmark hidden because not significant (13): async_tree_none, async_tree_cpu_io_mixed, json_dumps, asyncio_tcp_ssl, coverage, async_tree_none_tg, pickle_list, regex_v8, async_tree_io_tg, async_tree_cpu_io_mixed_tg, scimark_fft, async_tree_io, bench_mp_pool
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.05x