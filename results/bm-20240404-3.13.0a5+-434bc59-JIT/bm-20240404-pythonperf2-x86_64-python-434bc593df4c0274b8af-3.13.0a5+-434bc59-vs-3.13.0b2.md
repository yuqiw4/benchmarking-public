# Results vs. 3.13.0b2

- fork: python
- ref: 434bc593df4c0274b8af
- machine: linux-x86_64
- commit hash: 434bc59
- commit date: 2024-04-04
- overall geometric mean: 1.02x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.06x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf2-x86_64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 291 ms                                                           | 298 ms: 1.02x slower                                                         |
| chameleon      | 7.40 ms                                                          | 7.72 ms: 1.04x slower                                                        |
| docutils       | 2.98 sec                                                         | 3.07 sec: 1.03x slower                                                       |
| html5lib       | 74.7 ms                                                          | 75.4 ms: 1.01x slower                                                        |
| tornado_http   | 119 ms                                                           | 122 ms: 1.02x slower                                                         |
| Geometric mean | (ref)                                                            | 1.03x slower                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf2-x86_64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_io_tg           | 900 ms                                                           | 858 ms: 1.05x faster                                                         |
| async_tree_memoization     | 460 ms                                                           | 439 ms: 1.05x faster                                                         |
| async_tree_io              | 873 ms                                                           | 846 ms: 1.03x faster                                                         |
| async_tree_none_tg         | 340 ms                                                           | 332 ms: 1.03x faster                                                         |
| async_tree_none            | 365 ms                                                           | 374 ms: 1.02x slower                                                         |
| async_tree_cpu_io_mixed_tg | 573 ms                                                           | 588 ms: 1.03x slower                                                         |
| Geometric mean             | (ref)                                                            | 1.01x faster                                                                 |

Benchmark hidden because not significant (2): async_tree_cpu_io_mixed, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf2-x86_64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 80.2 ms                                                          | 75.3 ms: 1.06x faster                                                        |
| pidigits       | 254 ms                                                           | 261 ms: 1.03x slower                                                         |
| nbody          | 87.8 ms                                                          | 96.3 ms: 1.10x slower                                                        |
| Geometric mean | (ref)                                                            | 1.02x slower                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf2-x86_64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_dna      | 249 ms                                                           | 237 ms: 1.05x faster                                                         |
| regex_v8       | 26.0 ms                                                          | 25.4 ms: 1.02x faster                                                        |
| regex_compile  | 144 ms                                                           | 147 ms: 1.02x slower                                                         |
| regex_effbot   | 3.40 ms                                                          | 3.61 ms: 1.06x slower                                                        |
| Geometric mean | (ref)                                                            | 1.00x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark          | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf2-x86_64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|--------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| tomli_loads        | 2.40 sec                                                         | 2.13 sec: 1.13x faster                                                       |
| pickle_dict        | 32.8 us                                                          | 30.6 us: 1.07x faster                                                        |
| unpickle           | 15.7 us                                                          | 15.1 us: 1.04x faster                                                        |
| pickle             | 10.6 us                                                          | 10.4 us: 1.02x faster                                                        |
| unpickle_list      | 4.70 us                                                          | 4.61 us: 1.02x faster                                                        |
| json_dumps         | 10.8 ms                                                          | 10.6 ms: 1.02x faster                                                        |
| xml_etree_process  | 59.7 ms                                                          | 58.9 ms: 1.01x faster                                                        |
| xml_etree_generate | 85.7 ms                                                          | 84.7 ms: 1.01x faster                                                        |
| json_loads         | 25.0 us                                                          | 25.2 us: 1.01x slower                                                        |
| pickle_pure_python | 307 us                                                           | 313 us: 1.02x slower                                                         |
| xml_etree_parse    | 144 ms                                                           | 148 ms: 1.03x slower                                                         |
| Geometric mean     | (ref)                                                            | 1.02x faster                                                                 |

Benchmark hidden because not significant (3): xml_etree_iterparse, pickle_list, unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf2-x86_64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|------------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 13.2 ms                                                          | 13.4 ms: 1.02x slower                                                        |
| python_startup_no_site | 8.85 ms                                                          | 11.8 ms: 1.33x slower                                                        |
| Geometric mean         | (ref)                                                            | 1.16x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf2-x86_64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako           | 10.4 ms                                                          | 10.0 ms: 1.04x faster                                                        |
| genshi_xml     | 58.1 ms                                                          | 59.7 ms: 1.03x slower                                                        |
| genshi_text    | 25.9 ms                                                          | 26.7 ms: 1.03x slower                                                        |
| Geometric mean | (ref)                                                            | 1.01x slower                                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf2-x86_64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 171 us                                                           | 128 us: 1.33x faster                                                         |
| richards_super             | 61.2 ms                                                          | 51.9 ms: 1.18x faster                                                        |
| richards                   | 53.4 ms                                                          | 45.7 ms: 1.17x faster                                                        |
| tomli_loads                | 2.40 sec                                                         | 2.13 sec: 1.13x faster                                                       |
| create_gc_cycles           | 2.00 ms                                                          | 1.86 ms: 1.08x faster                                                        |
| pickle_dict                | 32.8 us                                                          | 30.6 us: 1.07x faster                                                        |
| float                      | 80.2 ms                                                          | 75.3 ms: 1.06x faster                                                        |
| regex_dna                  | 249 ms                                                           | 237 ms: 1.05x faster                                                         |
| async_tree_io_tg           | 900 ms                                                           | 858 ms: 1.05x faster                                                         |
| async_tree_memoization     | 460 ms                                                           | 439 ms: 1.05x faster                                                         |
| spectral_norm              | 97.3 ms                                                          | 93.2 ms: 1.04x faster                                                        |
| sqlite_synth               | 2.80 us                                                          | 2.69 us: 1.04x faster                                                        |
| mako                       | 10.4 ms                                                          | 10.0 ms: 1.04x faster                                                        |
| unpickle                   | 15.7 us                                                          | 15.1 us: 1.04x faster                                                        |
| scimark_sparse_mat_mult    | 4.28 ms                                                          | 4.14 ms: 1.03x faster                                                        |
| async_tree_io              | 873 ms                                                           | 846 ms: 1.03x faster                                                         |
| async_tree_none_tg         | 340 ms                                                           | 332 ms: 1.03x faster                                                         |
| pickle                     | 10.6 us                                                          | 10.4 us: 1.02x faster                                                        |
| regex_v8                   | 26.0 ms                                                          | 25.4 ms: 1.02x faster                                                        |
| coverage                   | 83.5 ms                                                          | 81.6 ms: 1.02x faster                                                        |
| gc_traversal               | 4.69 ms                                                          | 4.58 ms: 1.02x faster                                                        |
| telco                      | 8.40 ms                                                          | 8.22 ms: 1.02x faster                                                        |
| unpickle_list              | 4.70 us                                                          | 4.61 us: 1.02x faster                                                        |
| json_dumps                 | 10.8 ms                                                          | 10.6 ms: 1.02x faster                                                        |
| logging_format             | 7.11 us                                                          | 7.00 us: 1.02x faster                                                        |
| xml_etree_process          | 59.7 ms                                                          | 58.9 ms: 1.01x faster                                                        |
| asyncio_tcp                | 378 ms                                                           | 373 ms: 1.01x faster                                                         |
| xml_etree_generate         | 85.7 ms                                                          | 84.7 ms: 1.01x faster                                                        |
| json                       | 5.35 ms                                                          | 5.30 ms: 1.01x faster                                                        |
| logging_simple             | 6.40 us                                                          | 6.34 us: 1.01x faster                                                        |
| asyncio_websockets         | 395 ms                                                           | 391 ms: 1.01x faster                                                         |
| generators                 | 33.5 ms                                                          | 33.4 ms: 1.00x faster                                                        |
| asyncio_tcp_ssl            | 1.58 sec                                                         | 1.58 sec: 1.00x faster                                                       |
| json_loads                 | 25.0 us                                                          | 25.2 us: 1.01x slower                                                        |
| coroutines                 | 22.0 ms                                                          | 22.1 ms: 1.01x slower                                                        |
| thrift                     | 880 us                                                           | 885 us: 1.01x slower                                                         |
| dulwich_log                | 67.3 ms                                                          | 67.8 ms: 1.01x slower                                                        |
| logging_silent             | 96.3 ns                                                          | 97.2 ns: 1.01x slower                                                        |
| html5lib                   | 74.7 ms                                                          | 75.4 ms: 1.01x slower                                                        |
| sympy_expand               | 501 ms                                                           | 507 ms: 1.01x slower                                                         |
| python_startup             | 13.2 ms                                                          | 13.4 ms: 1.02x slower                                                        |
| sqlglot_parse              | 1.39 ms                                                          | 1.42 ms: 1.02x slower                                                        |
| pickle_pure_python         | 307 us                                                           | 313 us: 1.02x slower                                                         |
| pprint_safe_repr           | 818 ms                                                           | 834 ms: 1.02x slower                                                         |
| regex_compile              | 144 ms                                                           | 147 ms: 1.02x slower                                                         |
| tornado_http               | 119 ms                                                           | 122 ms: 1.02x slower                                                         |
| 2to3                       | 291 ms                                                           | 298 ms: 1.02x slower                                                         |
| async_tree_none            | 365 ms                                                           | 374 ms: 1.02x slower                                                         |
| dask                       | 391 ms                                                           | 400 ms: 1.02x slower                                                         |
| async_tree_cpu_io_mixed_tg | 573 ms                                                           | 588 ms: 1.03x slower                                                         |
| pycparser                  | 1.22 sec                                                         | 1.25 sec: 1.03x slower                                                       |
| genshi_xml                 | 58.1 ms                                                          | 59.7 ms: 1.03x slower                                                        |
| pidigits                   | 254 ms                                                           | 261 ms: 1.03x slower                                                         |
| xml_etree_parse            | 144 ms                                                           | 148 ms: 1.03x slower                                                         |
| sqlglot_transpile          | 1.76 ms                                                          | 1.82 ms: 1.03x slower                                                        |
| docutils                   | 2.98 sec                                                         | 3.07 sec: 1.03x slower                                                       |
| genshi_text                | 25.9 ms                                                          | 26.7 ms: 1.03x slower                                                        |
| pprint_pformat             | 1.66 sec                                                         | 1.71 sec: 1.03x slower                                                       |
| sympy_str                  | 295 ms                                                           | 305 ms: 1.03x slower                                                         |
| sqlglot_normalize          | 120 ms                                                           | 125 ms: 1.04x slower                                                         |
| deepcopy_reduce            | 3.39 us                                                          | 3.51 us: 1.04x slower                                                        |
| meteor_contest             | 128 ms                                                           | 133 ms: 1.04x slower                                                         |
| go                         | 165 ms                                                           | 172 ms: 1.04x slower                                                         |
| deepcopy_memo              | 37.3 us                                                          | 38.8 us: 1.04x slower                                                        |
| pyflate                    | 482 ms                                                           | 501 ms: 1.04x slower                                                         |
| mdp                        | 2.46 sec                                                         | 2.57 sec: 1.04x slower                                                       |
| bench_thread_pool          | 908 us                                                           | 947 us: 1.04x slower                                                         |
| raytrace                   | 260 ms                                                           | 272 ms: 1.04x slower                                                         |
| chameleon                  | 7.40 ms                                                          | 7.72 ms: 1.04x slower                                                        |
| aiohttp                    | 1.07 ms                                                          | 1.12 ms: 1.04x slower                                                        |
| async_generators           | 363 ms                                                           | 380 ms: 1.05x slower                                                         |
| gunicorn                   | 1.04 ms                                                          | 1.10 ms: 1.05x slower                                                        |
| sympy_sum                  | 155 ms                                                           | 163 ms: 1.05x slower                                                         |
| crypto_pyaes               | 73.6 ms                                                          | 77.2 ms: 1.05x slower                                                        |
| deepcopy                   | 377 us                                                           | 398 us: 1.05x slower                                                         |
| sqlglot_optimize           | 59.5 ms                                                          | 63.1 ms: 1.06x slower                                                        |
| regex_effbot               | 3.40 ms                                                          | 3.61 ms: 1.06x slower                                                        |
| mypy2                      | 764 ms                                                           | 819 ms: 1.07x slower                                                         |
| scimark_monte_carlo        | 65.5 ms                                                          | 70.2 ms: 1.07x slower                                                        |
| chaos                      | 59.6 ms                                                          | 64.6 ms: 1.08x slower                                                        |
| sympy_integrate            | 23.2 ms                                                          | 25.2 ms: 1.09x slower                                                        |
| nbody                      | 87.8 ms                                                          | 96.3 ms: 1.10x slower                                                        |
| fannkuch                   | 353 ms                                                           | 388 ms: 1.10x slower                                                         |
| deltablue                  | 3.37 ms                                                          | 3.76 ms: 1.11x slower                                                        |
| hexiom                     | 6.35 ms                                                          | 7.15 ms: 1.13x slower                                                        |
| comprehensions             | 17.0 us                                                          | 19.1 us: 1.13x slower                                                        |
| pathlib                    | 17.1 ms                                                          | 19.3 ms: 1.13x slower                                                        |
| nqueens                    | 88.4 ms                                                          | 102 ms: 1.15x slower                                                         |
| scimark_lu                 | 97.5 ms                                                          | 119 ms: 1.22x slower                                                         |
| scimark_sor                | 119 ms                                                           | 151 ms: 1.27x slower                                                         |
| python_startup_no_site     | 8.85 ms                                                          | 11.8 ms: 1.33x slower                                                        |
| Geometric mean             | (ref)                                                            | 1.02x slower                                                                 |

Benchmark hidden because not significant (8): bench_mp_pool, pylint, async_tree_cpu_io_mixed, async_tree_memoization_tg, xml_etree_iterparse, pickle_list, unpickle_pure_python, scimark_fft
Ignored benchmarks (3) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, django_template, flaskblogging

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.06x