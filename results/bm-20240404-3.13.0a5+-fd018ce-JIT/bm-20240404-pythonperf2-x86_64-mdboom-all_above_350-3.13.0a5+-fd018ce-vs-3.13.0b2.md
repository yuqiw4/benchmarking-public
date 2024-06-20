# Results vs. 3.13.0b2

- fork: mdboom
- ref: all_above_350
- machine: linux-x86_64
- commit hash: fd018ce
- commit date: 2024-04-04
- overall geometric mean: 1.03x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.05x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf2-x86_64-mdboom-all_above_350-3.13.0a5+-fd018ce |
|----------------|:----------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 291 ms                                                           | 302 ms: 1.04x slower                                                  |
| chameleon      | 7.40 ms                                                          | 7.34 ms: 1.01x faster                                                 |
| docutils       | 2.98 sec                                                         | 3.07 sec: 1.03x slower                                                |
| html5lib       | 74.7 ms                                                          | 72.8 ms: 1.03x faster                                                 |
| tornado_http   | 119 ms                                                           | 124 ms: 1.04x slower                                                  |
| Geometric mean | (ref)                                                            | 1.01x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf2-x86_64-mdboom-all_above_350-3.13.0a5+-fd018ce |
|---------------------------|:----------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization    | 460 ms                                                           | 442 ms: 1.04x faster                                                  |
| async_tree_none           | 365 ms                                                           | 359 ms: 1.02x faster                                                  |
| async_tree_io_tg          | 900 ms                                                           | 910 ms: 1.01x slower                                                  |
| async_tree_memoization_tg | 421 ms                                                           | 433 ms: 1.03x slower                                                  |
| Geometric mean            | (ref)                                                            | 1.00x faster                                                          |

Benchmark hidden because not significant (4): async_tree_cpu_io_mixed, async_tree_none_tg, async_tree_cpu_io_mixed_tg, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf2-x86_64-mdboom-all_above_350-3.13.0a5+-fd018ce |
|----------------|:----------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.2 ms                                                          | 79.5 ms: 1.01x faster                                                 |
| pidigits       | 254 ms                                                           | 261 ms: 1.03x slower                                                  |
| nbody          | 87.8 ms                                                          | 94.6 ms: 1.08x slower                                                 |
| Geometric mean | (ref)                                                            | 1.03x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf2-x86_64-mdboom-all_above_350-3.13.0a5+-fd018ce |
|----------------|:----------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna      | 249 ms                                                           | 242 ms: 1.03x faster                                                  |
| regex_compile  | 144 ms                                                           | 150 ms: 1.04x slower                                                  |
| regex_effbot   | 3.40 ms                                                          | 3.63 ms: 1.07x slower                                                 |
| Geometric mean | (ref)                                                            | 1.02x slower                                                          |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf2-x86_64-mdboom-all_above_350-3.13.0a5+-fd018ce |
|----------------------|:----------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.40 sec                                                         | 2.24 sec: 1.07x faster                                                |
| pickle_dict          | 32.8 us                                                          | 31.0 us: 1.06x faster                                                 |
| unpickle             | 15.7 us                                                          | 15.0 us: 1.04x faster                                                 |
| xml_etree_process    | 59.7 ms                                                          | 58.2 ms: 1.03x faster                                                 |
| xml_etree_generate   | 85.7 ms                                                          | 83.6 ms: 1.03x faster                                                 |
| xml_etree_parse      | 144 ms                                                           | 142 ms: 1.01x faster                                                  |
| pickle               | 10.6 us                                                          | 10.5 us: 1.01x faster                                                 |
| json_dumps           | 10.8 ms                                                          | 10.9 ms: 1.01x slower                                                 |
| json_loads           | 25.0 us                                                          | 25.3 us: 1.01x slower                                                 |
| unpickle_pure_python | 224 us                                                           | 243 us: 1.08x slower                                                  |
| Geometric mean       | (ref)                                                            | 1.01x faster                                                          |

Benchmark hidden because not significant (4): pickle_pure_python, pickle_list, xml_etree_iterparse, unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf2-x86_64-mdboom-all_above_350-3.13.0a5+-fd018ce |
|------------------------|:----------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 13.2 ms                                                          | 13.5 ms: 1.02x slower                                                 |
| python_startup_no_site | 8.85 ms                                                          | 11.8 ms: 1.33x slower                                                 |
| Geometric mean         | (ref)                                                            | 1.17x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf2-x86_64-mdboom-all_above_350-3.13.0a5+-fd018ce |
|-----------------|:----------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 10.4 ms                                                          | 9.87 ms: 1.05x faster                                                 |
| django_template | 39.0 ms                                                          | 40.9 ms: 1.05x slower                                                 |
| genshi_text     | 25.9 ms                                                          | 27.3 ms: 1.05x slower                                                 |
| Geometric mean  | (ref)                                                            | 1.01x slower                                                          |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                 | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf2-x86_64-mdboom-all_above_350-3.13.0a5+-fd018ce |
|---------------------------|:----------------------------------------------------------------:|:---------------------------------------------------------------------:|
| typing_runtime_protocols  | 171 us                                                           | 120 us: 1.42x faster                                                  |
| create_gc_cycles          | 2.00 ms                                                          | 1.79 ms: 1.12x faster                                                 |
| gc_traversal              | 4.69 ms                                                          | 4.36 ms: 1.08x faster                                                 |
| tomli_loads               | 2.40 sec                                                         | 2.24 sec: 1.07x faster                                                |
| pickle_dict               | 32.8 us                                                          | 31.0 us: 1.06x faster                                                 |
| mako                      | 10.4 ms                                                          | 9.87 ms: 1.05x faster                                                 |
| unpickle                  | 15.7 us                                                          | 15.0 us: 1.04x faster                                                 |
| async_tree_memoization    | 460 ms                                                           | 442 ms: 1.04x faster                                                  |
| coverage                  | 83.5 ms                                                          | 80.3 ms: 1.04x faster                                                 |
| richards_super            | 61.2 ms                                                          | 58.9 ms: 1.04x faster                                                 |
| scimark_sparse_mat_mult   | 4.28 ms                                                          | 4.13 ms: 1.04x faster                                                 |
| telco                     | 8.40 ms                                                          | 8.10 ms: 1.04x faster                                                 |
| regex_dna                 | 249 ms                                                           | 242 ms: 1.03x faster                                                  |
| sqlite_synth              | 2.80 us                                                          | 2.72 us: 1.03x faster                                                 |
| asyncio_websockets        | 395 ms                                                           | 385 ms: 1.03x faster                                                  |
| xml_etree_process         | 59.7 ms                                                          | 58.2 ms: 1.03x faster                                                 |
| html5lib                  | 74.7 ms                                                          | 72.8 ms: 1.03x faster                                                 |
| xml_etree_generate        | 85.7 ms                                                          | 83.6 ms: 1.03x faster                                                 |
| spectral_norm             | 97.3 ms                                                          | 95.4 ms: 1.02x faster                                                 |
| richards                  | 53.4 ms                                                          | 52.4 ms: 1.02x faster                                                 |
| async_tree_none           | 365 ms                                                           | 359 ms: 1.02x faster                                                  |
| xml_etree_parse           | 144 ms                                                           | 142 ms: 1.01x faster                                                  |
| asyncio_tcp               | 378 ms                                                           | 373 ms: 1.01x faster                                                  |
| pickle                    | 10.6 us                                                          | 10.5 us: 1.01x faster                                                 |
| float                     | 80.2 ms                                                          | 79.5 ms: 1.01x faster                                                 |
| deepcopy_reduce           | 3.39 us                                                          | 3.36 us: 1.01x faster                                                 |
| chameleon                 | 7.40 ms                                                          | 7.34 ms: 1.01x faster                                                 |
| generators                | 33.5 ms                                                          | 33.6 ms: 1.00x slower                                                 |
| coroutines                | 22.0 ms                                                          | 22.1 ms: 1.00x slower                                                 |
| json_dumps                | 10.8 ms                                                          | 10.9 ms: 1.01x slower                                                 |
| json_loads                | 25.0 us                                                          | 25.3 us: 1.01x slower                                                 |
| async_tree_io_tg          | 900 ms                                                           | 910 ms: 1.01x slower                                                  |
| logging_silent            | 96.3 ns                                                          | 97.4 ns: 1.01x slower                                                 |
| deepcopy_memo             | 37.3 us                                                          | 38.1 us: 1.02x slower                                                 |
| python_startup            | 13.2 ms                                                          | 13.5 ms: 1.02x slower                                                 |
| sqlglot_parse             | 1.39 ms                                                          | 1.43 ms: 1.02x slower                                                 |
| deepcopy                  | 377 us                                                           | 387 us: 1.03x slower                                                  |
| sympy_expand              | 501 ms                                                           | 515 ms: 1.03x slower                                                  |
| sqlglot_transpile         | 1.76 ms                                                          | 1.82 ms: 1.03x slower                                                 |
| dask                      | 391 ms                                                           | 402 ms: 1.03x slower                                                  |
| scimark_fft               | 312 ms                                                           | 321 ms: 1.03x slower                                                  |
| pidigits                  | 254 ms                                                           | 261 ms: 1.03x slower                                                  |
| async_tree_memoization_tg | 421 ms                                                           | 433 ms: 1.03x slower                                                  |
| docutils                  | 2.98 sec                                                         | 3.07 sec: 1.03x slower                                                |
| pprint_safe_repr          | 818 ms                                                           | 843 ms: 1.03x slower                                                  |
| sympy_str                 | 295 ms                                                           | 304 ms: 1.03x slower                                                  |
| logging_simple            | 6.40 us                                                          | 6.62 us: 1.03x slower                                                 |
| dulwich_log               | 67.3 ms                                                          | 69.6 ms: 1.03x slower                                                 |
| 2to3                      | 291 ms                                                           | 302 ms: 1.04x slower                                                  |
| sqlglot_normalize         | 120 ms                                                           | 125 ms: 1.04x slower                                                  |
| pprint_pformat            | 1.66 sec                                                         | 1.72 sec: 1.04x slower                                                |
| pycparser                 | 1.22 sec                                                         | 1.27 sec: 1.04x slower                                                |
| regex_compile             | 144 ms                                                           | 150 ms: 1.04x slower                                                  |
| gunicorn                  | 1.04 ms                                                          | 1.09 ms: 1.04x slower                                                 |
| aiohttp                   | 1.07 ms                                                          | 1.11 ms: 1.04x slower                                                 |
| tornado_http              | 119 ms                                                           | 124 ms: 1.04x slower                                                  |
| sympy_sum                 | 155 ms                                                           | 163 ms: 1.05x slower                                                  |
| django_template           | 39.0 ms                                                          | 40.9 ms: 1.05x slower                                                 |
| genshi_text               | 25.9 ms                                                          | 27.3 ms: 1.05x slower                                                 |
| pyflate                   | 482 ms                                                           | 507 ms: 1.05x slower                                                  |
| meteor_contest            | 128 ms                                                           | 135 ms: 1.06x slower                                                  |
| regex_effbot              | 3.40 ms                                                          | 3.63 ms: 1.07x slower                                                 |
| crypto_pyaes              | 73.6 ms                                                          | 78.7 ms: 1.07x slower                                                 |
| sqlglot_optimize          | 59.5 ms                                                          | 63.9 ms: 1.07x slower                                                 |
| pylint                    | 339 ms                                                           | 365 ms: 1.08x slower                                                  |
| nbody                     | 87.8 ms                                                          | 94.6 ms: 1.08x slower                                                 |
| async_generators          | 363 ms                                                           | 391 ms: 1.08x slower                                                  |
| go                        | 165 ms                                                           | 178 ms: 1.08x slower                                                  |
| mdp                       | 2.46 sec                                                         | 2.66 sec: 1.08x slower                                                |
| unpickle_pure_python      | 224 us                                                           | 243 us: 1.08x slower                                                  |
| mypy2                     | 764 ms                                                           | 831 ms: 1.09x slower                                                  |
| sympy_integrate           | 23.2 ms                                                          | 25.3 ms: 1.09x slower                                                 |
| fannkuch                  | 353 ms                                                           | 392 ms: 1.11x slower                                                  |
| chaos                     | 59.6 ms                                                          | 67.0 ms: 1.12x slower                                                 |
| deltablue                 | 3.37 ms                                                          | 3.79 ms: 1.12x slower                                                 |
| pathlib                   | 17.1 ms                                                          | 19.5 ms: 1.14x slower                                                 |
| scimark_monte_carlo       | 65.5 ms                                                          | 74.8 ms: 1.14x slower                                                 |
| comprehensions            | 17.0 us                                                          | 19.7 us: 1.16x slower                                                 |
| raytrace                  | 260 ms                                                           | 308 ms: 1.18x slower                                                  |
| nqueens                   | 88.4 ms                                                          | 106 ms: 1.20x slower                                                  |
| bench_thread_pool         | 908 us                                                           | 1.11 ms: 1.22x slower                                                 |
| hexiom                    | 6.35 ms                                                          | 7.74 ms: 1.22x slower                                                 |
| scimark_lu                | 97.5 ms                                                          | 125 ms: 1.28x slower                                                  |
| scimark_sor               | 119 ms                                                           | 155 ms: 1.30x slower                                                  |
| python_startup_no_site    | 8.85 ms                                                          | 11.8 ms: 1.33x slower                                                 |
| Geometric mean            | (ref)                                                            | 1.03x slower                                                          |

Benchmark hidden because not significant (15): async_tree_cpu_io_mixed, async_tree_none_tg, json, thrift, pickle_pure_python, asyncio_tcp_ssl, pickle_list, genshi_xml, xml_etree_iterparse, unpickle_list, regex_v8, logging_format, async_tree_cpu_io_mixed_tg, async_tree_io, bench_mp_pool
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.05x