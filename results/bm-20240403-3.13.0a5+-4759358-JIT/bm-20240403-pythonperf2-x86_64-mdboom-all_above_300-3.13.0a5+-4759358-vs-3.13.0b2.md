# Results vs. 3.13.0b2

- fork: mdboom
- ref: all_above_300
- machine: linux-x86_64
- commit hash: 4759358
- commit date: 2024-04-03
- overall geometric mean: 1.03x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x slower
- Memory change: 1.05x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-pythonperf2-x86_64-mdboom-all_above_300-3.13.0a5+-4759358 |
|----------------|:----------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 291 ms                                                           | 301 ms: 1.03x slower                                                  |
| chameleon      | 7.40 ms                                                          | 7.23 ms: 1.02x faster                                                 |
| docutils       | 2.98 sec                                                         | 3.05 sec: 1.02x slower                                                |
| html5lib       | 74.7 ms                                                          | 73.5 ms: 1.02x faster                                                 |
| tornado_http   | 119 ms                                                           | 125 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                            | 1.01x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-pythonperf2-x86_64-mdboom-all_above_300-3.13.0a5+-4759358 |
|----------------------------|:----------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization_tg  | 421 ms                                                           | 432 ms: 1.03x slower                                                  |
| async_tree_cpu_io_mixed_tg | 573 ms                                                           | 593 ms: 1.03x slower                                                  |
| async_tree_io              | 873 ms                                                           | 909 ms: 1.04x slower                                                  |
| async_tree_none            | 365 ms                                                           | 380 ms: 1.04x slower                                                  |
| Geometric mean             | (ref)                                                            | 1.01x slower                                                          |

Benchmark hidden because not significant (4): async_tree_io_tg, async_tree_memoization, async_tree_cpu_io_mixed, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-pythonperf2-x86_64-mdboom-all_above_300-3.13.0a5+-4759358 |
|----------------|:----------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.2 ms                                                          | 79.5 ms: 1.01x faster                                                 |
| pidigits       | 254 ms                                                           | 261 ms: 1.03x slower                                                  |
| nbody          | 87.8 ms                                                          | 95.4 ms: 1.09x slower                                                 |
| Geometric mean | (ref)                                                            | 1.04x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-pythonperf2-x86_64-mdboom-all_above_300-3.13.0a5+-4759358 |
|----------------|:----------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna      | 249 ms                                                           | 246 ms: 1.01x faster                                                  |
| regex_v8       | 26.0 ms                                                          | 25.9 ms: 1.01x faster                                                 |
| regex_effbot   | 3.40 ms                                                          | 3.50 ms: 1.03x slower                                                 |
| regex_compile  | 144 ms                                                           | 149 ms: 1.03x slower                                                  |
| Geometric mean | (ref)                                                            | 1.01x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-pythonperf2-x86_64-mdboom-all_above_300-3.13.0a5+-4759358 |
|----------------------|:----------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.40 sec                                                         | 2.21 sec: 1.09x faster                                                |
| unpickle             | 15.7 us                                                          | 14.9 us: 1.05x faster                                                 |
| xml_etree_process    | 59.7 ms                                                          | 58.0 ms: 1.03x faster                                                 |
| xml_etree_generate   | 85.7 ms                                                          | 84.3 ms: 1.02x faster                                                 |
| pickle_list          | 4.44 us                                                          | 4.38 us: 1.01x faster                                                 |
| xml_etree_parse      | 144 ms                                                           | 142 ms: 1.01x faster                                                  |
| xml_etree_iterparse  | 103 ms                                                           | 102 ms: 1.01x faster                                                  |
| pickle_dict          | 32.8 us                                                          | 32.7 us: 1.00x faster                                                 |
| json_loads           | 25.0 us                                                          | 25.3 us: 1.01x slower                                                 |
| pickle               | 10.6 us                                                          | 10.8 us: 1.02x slower                                                 |
| unpickle_pure_python | 224 us                                                           | 241 us: 1.07x slower                                                  |
| Geometric mean       | (ref)                                                            | 1.01x faster                                                          |

Benchmark hidden because not significant (3): pickle_pure_python, unpickle_list, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-pythonperf2-x86_64-mdboom-all_above_300-3.13.0a5+-4759358 |
|------------------------|:----------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 13.2 ms                                                          | 13.5 ms: 1.02x slower                                                 |
| python_startup_no_site | 8.85 ms                                                          | 11.8 ms: 1.33x slower                                                 |
| Geometric mean         | (ref)                                                            | 1.17x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-pythonperf2-x86_64-mdboom-all_above_300-3.13.0a5+-4759358 |
|-----------------|:----------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 10.4 ms                                                          | 9.92 ms: 1.05x faster                                                 |
| genshi_text     | 25.9 ms                                                          | 26.7 ms: 1.03x slower                                                 |
| django_template | 39.0 ms                                                          | 40.2 ms: 1.03x slower                                                 |
| genshi_xml      | 58.1 ms                                                          | 60.3 ms: 1.04x slower                                                 |
| Geometric mean  | (ref)                                                            | 1.01x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-pythonperf2-x86_64-mdboom-all_above_300-3.13.0a5+-4759358 |
|----------------------------|:----------------------------------------------------------------:|:---------------------------------------------------------------------:|
| typing_runtime_protocols   | 171 us                                                           | 120 us: 1.43x faster                                                  |
| create_gc_cycles           | 2.00 ms                                                          | 1.80 ms: 1.11x faster                                                 |
| tomli_loads                | 2.40 sec                                                         | 2.21 sec: 1.09x faster                                                |
| gc_traversal               | 4.69 ms                                                          | 4.37 ms: 1.07x faster                                                 |
| unpickle                   | 15.7 us                                                          | 14.9 us: 1.05x faster                                                 |
| richards_super             | 61.2 ms                                                          | 58.3 ms: 1.05x faster                                                 |
| telco                      | 8.40 ms                                                          | 8.03 ms: 1.05x faster                                                 |
| mako                       | 10.4 ms                                                          | 9.92 ms: 1.05x faster                                                 |
| sqlite_synth               | 2.80 us                                                          | 2.70 us: 1.04x faster                                                 |
| xml_etree_process          | 59.7 ms                                                          | 58.0 ms: 1.03x faster                                                 |
| richards                   | 53.4 ms                                                          | 51.9 ms: 1.03x faster                                                 |
| chameleon                  | 7.40 ms                                                          | 7.23 ms: 1.02x faster                                                 |
| asyncio_tcp                | 378 ms                                                           | 370 ms: 1.02x faster                                                  |
| xml_etree_generate         | 85.7 ms                                                          | 84.3 ms: 1.02x faster                                                 |
| html5lib                   | 74.7 ms                                                          | 73.5 ms: 1.02x faster                                                 |
| asyncio_websockets         | 395 ms                                                           | 389 ms: 1.02x faster                                                  |
| regex_dna                  | 249 ms                                                           | 246 ms: 1.01x faster                                                  |
| pickle_list                | 4.44 us                                                          | 4.38 us: 1.01x faster                                                 |
| xml_etree_parse            | 144 ms                                                           | 142 ms: 1.01x faster                                                  |
| float                      | 80.2 ms                                                          | 79.5 ms: 1.01x faster                                                 |
| scimark_sparse_mat_mult    | 4.28 ms                                                          | 4.25 ms: 1.01x faster                                                 |
| xml_etree_iterparse        | 103 ms                                                           | 102 ms: 1.01x faster                                                  |
| spectral_norm              | 97.3 ms                                                          | 96.8 ms: 1.01x faster                                                 |
| regex_v8                   | 26.0 ms                                                          | 25.9 ms: 1.01x faster                                                 |
| pickle_dict                | 32.8 us                                                          | 32.7 us: 1.00x faster                                                 |
| generators                 | 33.5 ms                                                          | 33.4 ms: 1.00x faster                                                 |
| asyncio_tcp_ssl            | 1.58 sec                                                         | 1.58 sec: 1.00x faster                                                |
| json_loads                 | 25.0 us                                                          | 25.3 us: 1.01x slower                                                 |
| thrift                     | 880 us                                                           | 893 us: 1.01x slower                                                  |
| logging_silent             | 96.3 ns                                                          | 97.7 ns: 1.01x slower                                                 |
| pickle                     | 10.6 us                                                          | 10.8 us: 1.02x slower                                                 |
| python_startup             | 13.2 ms                                                          | 13.5 ms: 1.02x slower                                                 |
| docutils                   | 2.98 sec                                                         | 3.05 sec: 1.02x slower                                                |
| sympy_expand               | 501 ms                                                           | 513 ms: 1.02x slower                                                  |
| sqlglot_normalize          | 120 ms                                                           | 123 ms: 1.02x slower                                                  |
| coroutines                 | 22.0 ms                                                          | 22.6 ms: 1.03x slower                                                 |
| scimark_fft                | 312 ms                                                           | 320 ms: 1.03x slower                                                  |
| async_tree_memoization_tg  | 421 ms                                                           | 432 ms: 1.03x slower                                                  |
| sqlglot_parse              | 1.39 ms                                                          | 1.43 ms: 1.03x slower                                                 |
| deepcopy_memo              | 37.3 us                                                          | 38.4 us: 1.03x slower                                                 |
| regex_effbot               | 3.40 ms                                                          | 3.50 ms: 1.03x slower                                                 |
| pidigits                   | 254 ms                                                           | 261 ms: 1.03x slower                                                  |
| genshi_text                | 25.9 ms                                                          | 26.7 ms: 1.03x slower                                                 |
| dulwich_log                | 67.3 ms                                                          | 69.4 ms: 1.03x slower                                                 |
| dask                       | 391 ms                                                           | 403 ms: 1.03x slower                                                  |
| deepcopy                   | 377 us                                                           | 390 us: 1.03x slower                                                  |
| django_template            | 39.0 ms                                                          | 40.2 ms: 1.03x slower                                                 |
| 2to3                       | 291 ms                                                           | 301 ms: 1.03x slower                                                  |
| regex_compile              | 144 ms                                                           | 149 ms: 1.03x slower                                                  |
| async_tree_cpu_io_mixed_tg | 573 ms                                                           | 593 ms: 1.03x slower                                                  |
| sqlglot_transpile          | 1.76 ms                                                          | 1.83 ms: 1.04x slower                                                 |
| sympy_str                  | 295 ms                                                           | 305 ms: 1.04x slower                                                  |
| genshi_xml                 | 58.1 ms                                                          | 60.3 ms: 1.04x slower                                                 |
| logging_simple             | 6.40 us                                                          | 6.66 us: 1.04x slower                                                 |
| async_tree_io              | 873 ms                                                           | 909 ms: 1.04x slower                                                  |
| aiohttp                    | 1.07 ms                                                          | 1.12 ms: 1.04x slower                                                 |
| async_tree_none            | 365 ms                                                           | 380 ms: 1.04x slower                                                  |
| tornado_http               | 119 ms                                                           | 125 ms: 1.05x slower                                                  |
| gunicorn                   | 1.04 ms                                                          | 1.09 ms: 1.05x slower                                                 |
| pprint_safe_repr           | 818 ms                                                           | 858 ms: 1.05x slower                                                  |
| meteor_contest             | 128 ms                                                           | 135 ms: 1.05x slower                                                  |
| pycparser                  | 1.22 sec                                                         | 1.29 sec: 1.05x slower                                                |
| pprint_pformat             | 1.66 sec                                                         | 1.75 sec: 1.05x slower                                                |
| sympy_sum                  | 155 ms                                                           | 163 ms: 1.05x slower                                                  |
| coverage                   | 83.5 ms                                                          | 88.1 ms: 1.05x slower                                                 |
| sqlglot_optimize           | 59.5 ms                                                          | 63.2 ms: 1.06x slower                                                 |
| mdp                        | 2.46 sec                                                         | 2.62 sec: 1.06x slower                                                |
| bench_mp_pool              | 4.91 ms                                                          | 5.22 ms: 1.06x slower                                                 |
| crypto_pyaes               | 73.6 ms                                                          | 78.7 ms: 1.07x slower                                                 |
| unpickle_pure_python       | 224 us                                                           | 241 us: 1.07x slower                                                  |
| pylint                     | 339 ms                                                           | 365 ms: 1.08x slower                                                  |
| mypy2                      | 764 ms                                                           | 828 ms: 1.08x slower                                                  |
| async_generators           | 363 ms                                                           | 394 ms: 1.09x slower                                                  |
| nbody                      | 87.8 ms                                                          | 95.4 ms: 1.09x slower                                                 |
| go                         | 165 ms                                                           | 180 ms: 1.09x slower                                                  |
| sympy_integrate            | 23.2 ms                                                          | 25.3 ms: 1.09x slower                                                 |
| pyflate                    | 482 ms                                                           | 525 ms: 1.09x slower                                                  |
| fannkuch                   | 353 ms                                                           | 393 ms: 1.11x slower                                                  |
| deltablue                  | 3.37 ms                                                          | 3.76 ms: 1.11x slower                                                 |
| pathlib                    | 17.1 ms                                                          | 19.4 ms: 1.14x slower                                                 |
| chaos                      | 59.6 ms                                                          | 67.9 ms: 1.14x slower                                                 |
| scimark_monte_carlo        | 65.5 ms                                                          | 74.8 ms: 1.14x slower                                                 |
| comprehensions             | 17.0 us                                                          | 19.8 us: 1.16x slower                                                 |
| raytrace                   | 260 ms                                                           | 306 ms: 1.18x slower                                                  |
| nqueens                    | 88.4 ms                                                          | 107 ms: 1.21x slower                                                  |
| hexiom                     | 6.35 ms                                                          | 7.75 ms: 1.22x slower                                                 |
| bench_thread_pool          | 908 us                                                           | 1.13 ms: 1.24x slower                                                 |
| scimark_lu                 | 97.5 ms                                                          | 126 ms: 1.29x slower                                                  |
| scimark_sor                | 119 ms                                                           | 155 ms: 1.31x slower                                                  |
| python_startup_no_site     | 8.85 ms                                                          | 11.8 ms: 1.33x slower                                                 |
| Geometric mean             | (ref)                                                            | 1.03x slower                                                          |

Benchmark hidden because not significant (10): async_tree_io_tg, async_tree_memoization, async_tree_cpu_io_mixed, deepcopy_reduce, pickle_pure_python, json, unpickle_list, json_dumps, logging_format, async_tree_none_tg
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.03x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.02x

# Memory
- memory change: 1.05x