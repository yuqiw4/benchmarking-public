# Results vs. 3.13.0b2

- fork: python
- ref: c43f6a4dfaa1c1974141
- machine: linux-x86_64
- commit hash: c43f6a4
- commit date: 2024-04-03
- overall geometric mean: 1.13x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x slower
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-pythonperf2-x86_64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 |
|----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 291 ms                                                           | 320 ms: 1.10x slower                                                         |
| chameleon      | 7.40 ms                                                          | 8.00 ms: 1.08x slower                                                        |
| docutils       | 2.98 sec                                                         | 3.29 sec: 1.10x slower                                                       |
| html5lib       | 74.7 ms                                                          | 79.1 ms: 1.06x slower                                                        |
| tornado_http   | 119 ms                                                           | 128 ms: 1.07x slower                                                         |
| Geometric mean | (ref)                                                            | 1.08x slower                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-pythonperf2-x86_64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 |
|----------------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_io_tg           | 900 ms                                                           | 882 ms: 1.02x faster                                                         |
| async_tree_cpu_io_mixed    | 604 ms                                                           | 623 ms: 1.03x slower                                                         |
| async_tree_io              | 873 ms                                                           | 905 ms: 1.04x slower                                                         |
| async_tree_memoization_tg  | 421 ms                                                           | 436 ms: 1.04x slower                                                         |
| async_tree_cpu_io_mixed_tg | 573 ms                                                           | 601 ms: 1.05x slower                                                         |
| async_tree_none            | 365 ms                                                           | 394 ms: 1.08x slower                                                         |
| Geometric mean             | (ref)                                                            | 1.03x slower                                                                 |

Benchmark hidden because not significant (2): async_tree_memoization, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-pythonperf2-x86_64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 |
|----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pidigits       | 254 ms                                                           | 265 ms: 1.05x slower                                                         |
| float          | 80.2 ms                                                          | 101 ms: 1.25x slower                                                         |
| nbody          | 87.8 ms                                                          | 130 ms: 1.48x slower                                                         |
| Geometric mean | (ref)                                                            | 1.25x slower                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-pythonperf2-x86_64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 |
|----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_dna      | 249 ms                                                           | 239 ms: 1.04x faster                                                         |
| regex_v8       | 26.0 ms                                                          | 26.6 ms: 1.02x slower                                                        |
| regex_effbot   | 3.40 ms                                                          | 3.54 ms: 1.04x slower                                                        |
| regex_compile  | 144 ms                                                           | 208 ms: 1.44x slower                                                         |
| Geometric mean | (ref)                                                            | 1.10x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-pythonperf2-x86_64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 |
|----------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| unpickle             | 15.7 us                                                          | 15.3 us: 1.03x faster                                                        |
| json_dumps           | 10.8 ms                                                          | 10.7 ms: 1.01x faster                                                        |
| pickle_dict          | 32.8 us                                                          | 32.7 us: 1.00x faster                                                        |
| json_loads           | 25.0 us                                                          | 25.2 us: 1.01x slower                                                        |
| unpickle_list        | 4.70 us                                                          | 4.77 us: 1.01x slower                                                        |
| pickle               | 10.6 us                                                          | 10.8 us: 1.02x slower                                                        |
| xml_etree_parse      | 144 ms                                                           | 147 ms: 1.02x slower                                                         |
| pickle_pure_python   | 307 us                                                           | 324 us: 1.05x slower                                                         |
| xml_etree_process    | 59.7 ms                                                          | 64.6 ms: 1.08x slower                                                        |
| xml_etree_generate   | 85.7 ms                                                          | 93.8 ms: 1.09x slower                                                        |
| xml_etree_iterparse  | 103 ms                                                           | 114 ms: 1.11x slower                                                         |
| tomli_loads          | 2.40 sec                                                         | 2.89 sec: 1.20x slower                                                       |
| unpickle_pure_python | 224 us                                                           | 310 us: 1.38x slower                                                         |
| Geometric mean       | (ref)                                                            | 1.06x slower                                                                 |

Benchmark hidden because not significant (1): pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-pythonperf2-x86_64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 |
|------------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 13.2 ms                                                          | 12.9 ms: 1.02x faster                                                        |
| python_startup_no_site | 8.85 ms                                                          | 11.2 ms: 1.26x slower                                                        |
| Geometric mean         | (ref)                                                            | 1.11x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-pythonperf2-x86_64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 |
|----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| genshi_xml     | 58.1 ms                                                          | 62.2 ms: 1.07x slower                                                        |
| genshi_text    | 25.9 ms                                                          | 27.9 ms: 1.08x slower                                                        |
| mako           | 10.4 ms                                                          | 14.0 ms: 1.35x slower                                                        |
| Geometric mean | (ref)                                                            | 1.16x slower                                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-pythonperf2-x86_64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 |
|----------------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 171 us                                                           | 126 us: 1.35x faster                                                         |
| gc_traversal               | 4.69 ms                                                          | 4.35 ms: 1.08x faster                                                        |
| regex_dna                  | 249 ms                                                           | 239 ms: 1.04x faster                                                         |
| create_gc_cycles           | 2.00 ms                                                          | 1.94 ms: 1.04x faster                                                        |
| unpickle                   | 15.7 us                                                          | 15.3 us: 1.03x faster                                                        |
| python_startup             | 13.2 ms                                                          | 12.9 ms: 1.02x faster                                                        |
| async_tree_io_tg           | 900 ms                                                           | 882 ms: 1.02x faster                                                         |
| generators                 | 33.5 ms                                                          | 33.0 ms: 1.02x faster                                                        |
| json_dumps                 | 10.8 ms                                                          | 10.7 ms: 1.01x faster                                                        |
| pickle_dict                | 32.8 us                                                          | 32.7 us: 1.00x faster                                                        |
| json_loads                 | 25.0 us                                                          | 25.2 us: 1.01x slower                                                        |
| asyncio_tcp_ssl            | 1.58 sec                                                         | 1.60 sec: 1.01x slower                                                       |
| unpickle_list              | 4.70 us                                                          | 4.77 us: 1.01x slower                                                        |
| thrift                     | 880 us                                                           | 893 us: 1.01x slower                                                         |
| coroutines                 | 22.0 ms                                                          | 22.3 ms: 1.02x slower                                                        |
| pickle                     | 10.6 us                                                          | 10.8 us: 1.02x slower                                                        |
| regex_v8                   | 26.0 ms                                                          | 26.6 ms: 1.02x slower                                                        |
| xml_etree_parse            | 144 ms                                                           | 147 ms: 1.02x slower                                                         |
| sqlite_synth               | 2.80 us                                                          | 2.87 us: 1.03x slower                                                        |
| async_tree_cpu_io_mixed    | 604 ms                                                           | 623 ms: 1.03x slower                                                         |
| logging_format             | 7.11 us                                                          | 7.33 us: 1.03x slower                                                        |
| logging_silent             | 96.3 ns                                                          | 99.4 ns: 1.03x slower                                                        |
| logging_simple             | 6.40 us                                                          | 6.63 us: 1.04x slower                                                        |
| async_tree_io              | 873 ms                                                           | 905 ms: 1.04x slower                                                         |
| async_tree_memoization_tg  | 421 ms                                                           | 436 ms: 1.04x slower                                                         |
| regex_effbot               | 3.40 ms                                                          | 3.54 ms: 1.04x slower                                                        |
| pidigits                   | 254 ms                                                           | 265 ms: 1.05x slower                                                         |
| coverage                   | 83.5 ms                                                          | 87.6 ms: 1.05x slower                                                        |
| async_tree_cpu_io_mixed_tg | 573 ms                                                           | 601 ms: 1.05x slower                                                         |
| pickle_pure_python         | 307 us                                                           | 324 us: 1.05x slower                                                         |
| aiohttp                    | 1.07 ms                                                          | 1.13 ms: 1.06x slower                                                        |
| html5lib                   | 74.7 ms                                                          | 79.1 ms: 1.06x slower                                                        |
| deepcopy_reduce            | 3.39 us                                                          | 3.59 us: 1.06x slower                                                        |
| dask                       | 391 ms                                                           | 416 ms: 1.07x slower                                                         |
| gunicorn                   | 1.04 ms                                                          | 1.12 ms: 1.07x slower                                                        |
| tornado_http               | 119 ms                                                           | 128 ms: 1.07x slower                                                         |
| genshi_xml                 | 58.1 ms                                                          | 62.2 ms: 1.07x slower                                                        |
| genshi_text                | 25.9 ms                                                          | 27.9 ms: 1.08x slower                                                        |
| async_tree_none            | 365 ms                                                           | 394 ms: 1.08x slower                                                         |
| sqlglot_normalize          | 120 ms                                                           | 130 ms: 1.08x slower                                                         |
| async_generators           | 363 ms                                                           | 391 ms: 1.08x slower                                                         |
| xml_etree_process          | 59.7 ms                                                          | 64.6 ms: 1.08x slower                                                        |
| chameleon                  | 7.40 ms                                                          | 8.00 ms: 1.08x slower                                                        |
| mdp                        | 2.46 sec                                                         | 2.68 sec: 1.09x slower                                                       |
| xml_etree_generate         | 85.7 ms                                                          | 93.8 ms: 1.09x slower                                                        |
| 2to3                       | 291 ms                                                           | 320 ms: 1.10x slower                                                         |
| richards_super             | 61.2 ms                                                          | 67.4 ms: 1.10x slower                                                        |
| docutils                   | 2.98 sec                                                         | 3.29 sec: 1.10x slower                                                       |
| deepcopy                   | 377 us                                                           | 417 us: 1.11x slower                                                         |
| xml_etree_iterparse        | 103 ms                                                           | 114 ms: 1.11x slower                                                         |
| pycparser                  | 1.22 sec                                                         | 1.36 sec: 1.11x slower                                                       |
| meteor_contest             | 128 ms                                                           | 143 ms: 1.12x slower                                                         |
| sqlglot_transpile          | 1.76 ms                                                          | 1.99 ms: 1.12x slower                                                        |
| mypy2                      | 764 ms                                                           | 862 ms: 1.13x slower                                                         |
| sqlglot_parse              | 1.39 ms                                                          | 1.57 ms: 1.13x slower                                                        |
| sqlglot_optimize           | 59.5 ms                                                          | 67.5 ms: 1.13x slower                                                        |
| richards                   | 53.4 ms                                                          | 61.0 ms: 1.14x slower                                                        |
| dulwich_log                | 67.3 ms                                                          | 77.8 ms: 1.16x slower                                                        |
| sympy_sum                  | 155 ms                                                           | 180 ms: 1.16x slower                                                         |
| sympy_integrate            | 23.2 ms                                                          | 26.9 ms: 1.16x slower                                                        |
| sympy_expand               | 501 ms                                                           | 584 ms: 1.17x slower                                                         |
| deltablue                  | 3.37 ms                                                          | 3.97 ms: 1.18x slower                                                        |
| pathlib                    | 17.1 ms                                                          | 20.3 ms: 1.18x slower                                                        |
| sympy_str                  | 295 ms                                                           | 350 ms: 1.19x slower                                                         |
| pprint_safe_repr           | 818 ms                                                           | 983 ms: 1.20x slower                                                         |
| tomli_loads                | 2.40 sec                                                         | 2.89 sec: 1.20x slower                                                       |
| deepcopy_memo              | 37.3 us                                                          | 45.1 us: 1.21x slower                                                        |
| pprint_pformat             | 1.66 sec                                                         | 2.01 sec: 1.21x slower                                                       |
| go                         | 165 ms                                                           | 205 ms: 1.24x slower                                                         |
| crypto_pyaes               | 73.6 ms                                                          | 92.2 ms: 1.25x slower                                                        |
| float                      | 80.2 ms                                                          | 101 ms: 1.25x slower                                                         |
| bench_thread_pool          | 908 us                                                           | 1.14 ms: 1.26x slower                                                        |
| python_startup_no_site     | 8.85 ms                                                          | 11.2 ms: 1.26x slower                                                        |
| chaos                      | 59.6 ms                                                          | 75.9 ms: 1.27x slower                                                        |
| raytrace                   | 260 ms                                                           | 336 ms: 1.29x slower                                                         |
| mako                       | 10.4 ms                                                          | 14.0 ms: 1.35x slower                                                        |
| pyflate                    | 482 ms                                                           | 649 ms: 1.35x slower                                                         |
| nqueens                    | 88.4 ms                                                          | 122 ms: 1.38x slower                                                         |
| unpickle_pure_python       | 224 us                                                           | 310 us: 1.38x slower                                                         |
| scimark_fft                | 312 ms                                                           | 437 ms: 1.40x slower                                                         |
| regex_compile              | 144 ms                                                           | 208 ms: 1.44x slower                                                         |
| scimark_sor                | 119 ms                                                           | 172 ms: 1.45x slower                                                         |
| fannkuch                   | 353 ms                                                           | 520 ms: 1.48x slower                                                         |
| nbody                      | 87.8 ms                                                          | 130 ms: 1.48x slower                                                         |
| scimark_monte_carlo        | 65.5 ms                                                          | 99.0 ms: 1.51x slower                                                        |
| scimark_lu                 | 97.5 ms                                                          | 149 ms: 1.53x slower                                                         |
| scimark_sparse_mat_mult    | 4.28 ms                                                          | 6.68 ms: 1.56x slower                                                        |
| comprehensions             | 17.0 us                                                          | 26.7 us: 1.57x slower                                                        |
| spectral_norm              | 97.3 ms                                                          | 154 ms: 1.59x slower                                                         |
| hexiom                     | 6.35 ms                                                          | 10.8 ms: 1.70x slower                                                        |
| Geometric mean             | (ref)                                                            | 1.13x slower                                                                 |

Benchmark hidden because not significant (9): telco, async_tree_memoization, asyncio_websockets, pickle_list, asyncio_tcp, json, bench_mp_pool, async_tree_none_tg, pylint
Ignored benchmarks (3) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, django_template, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.09x
- 99% likely to have a slowdown of 1.07x

# Memory
- memory change: 0.99x