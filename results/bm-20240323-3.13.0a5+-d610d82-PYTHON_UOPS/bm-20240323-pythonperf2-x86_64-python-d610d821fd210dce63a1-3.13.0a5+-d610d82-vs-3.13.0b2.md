# Results vs. 3.13.0b2

- fork: python
- ref: d610d821fd210dce63a1
- machine: linux-x86_64
- commit hash: d610d82
- commit date: 2024-03-23
- overall geometric mean: 1.11x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x slower
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf2-x86_64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 291 ms                                                           | 320 ms: 1.10x slower                                                         |
| chameleon      | 7.40 ms                                                          | 7.82 ms: 1.06x slower                                                        |
| docutils       | 2.98 sec                                                         | 3.20 sec: 1.07x slower                                                       |
| html5lib       | 74.7 ms                                                          | 77.2 ms: 1.03x slower                                                        |
| tornado_http   | 119 ms                                                           | 127 ms: 1.06x slower                                                         |
| Geometric mean | (ref)                                                            | 1.07x slower                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf2-x86_64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|----------------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed    | 604 ms                                                           | 617 ms: 1.02x slower                                                         |
| async_tree_none_tg         | 340 ms                                                           | 356 ms: 1.05x slower                                                         |
| async_tree_cpu_io_mixed_tg | 573 ms                                                           | 600 ms: 1.05x slower                                                         |
| async_tree_memoization_tg  | 421 ms                                                           | 448 ms: 1.07x slower                                                         |
| async_tree_none            | 365 ms                                                           | 395 ms: 1.08x slower                                                         |
| Geometric mean             | (ref)                                                            | 1.03x slower                                                                 |

Benchmark hidden because not significant (3): async_tree_memoization, async_tree_io_tg, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf2-x86_64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pidigits       | 254 ms                                                           | 265 ms: 1.04x slower                                                         |
| float          | 80.2 ms                                                          | 101 ms: 1.26x slower                                                         |
| nbody          | 87.8 ms                                                          | 130 ms: 1.48x slower                                                         |
| Geometric mean | (ref)                                                            | 1.25x slower                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf2-x86_64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_dna      | 249 ms                                                           | 241 ms: 1.03x faster                                                         |
| regex_v8       | 26.0 ms                                                          | 25.8 ms: 1.01x faster                                                        |
| regex_effbot   | 3.40 ms                                                          | 3.61 ms: 1.06x slower                                                        |
| regex_compile  | 144 ms                                                           | 204 ms: 1.41x slower                                                         |
| Geometric mean | (ref)                                                            | 1.10x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf2-x86_64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|----------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pickle_dict          | 32.8 us                                                          | 31.2 us: 1.05x faster                                                        |
| unpickle             | 15.7 us                                                          | 15.1 us: 1.04x faster                                                        |
| pickle               | 10.6 us                                                          | 10.3 us: 1.03x faster                                                        |
| json_dumps           | 10.8 ms                                                          | 10.7 ms: 1.01x faster                                                        |
| pickle_list          | 4.44 us                                                          | 4.41 us: 1.01x faster                                                        |
| json_loads           | 25.0 us                                                          | 25.2 us: 1.01x slower                                                        |
| xml_etree_parse      | 144 ms                                                           | 146 ms: 1.01x slower                                                         |
| pickle_pure_python   | 307 us                                                           | 316 us: 1.03x slower                                                         |
| xml_etree_process    | 59.7 ms                                                          | 62.4 ms: 1.04x slower                                                        |
| xml_etree_generate   | 85.7 ms                                                          | 90.3 ms: 1.05x slower                                                        |
| xml_etree_iterparse  | 103 ms                                                           | 115 ms: 1.12x slower                                                         |
| tomli_loads          | 2.40 sec                                                         | 2.90 sec: 1.21x slower                                                       |
| unpickle_pure_python | 224 us                                                           | 303 us: 1.35x slower                                                         |
| Geometric mean       | (ref)                                                            | 1.04x slower                                                                 |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf2-x86_64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|------------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 13.2 ms                                                          | 12.8 ms: 1.03x faster                                                        |
| python_startup_no_site | 8.85 ms                                                          | 11.1 ms: 1.25x slower                                                        |
| Geometric mean         | (ref)                                                            | 1.10x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf2-x86_64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|-----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| genshi_xml      | 58.1 ms                                                          | 62.1 ms: 1.07x slower                                                        |
| django_template | 39.0 ms                                                          | 42.2 ms: 1.08x slower                                                        |
| genshi_text     | 25.9 ms                                                          | 29.6 ms: 1.14x slower                                                        |
| mako            | 10.4 ms                                                          | 14.5 ms: 1.40x slower                                                        |
| Geometric mean  | (ref)                                                            | 1.17x slower                                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf2-x86_64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|----------------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 171 us                                                           | 129 us: 1.33x faster                                                         |
| create_gc_cycles           | 2.00 ms                                                          | 1.59 ms: 1.26x faster                                                        |
| pickle_dict                | 32.8 us                                                          | 31.2 us: 1.05x faster                                                        |
| unpickle                   | 15.7 us                                                          | 15.1 us: 1.04x faster                                                        |
| coverage                   | 83.5 ms                                                          | 80.5 ms: 1.04x faster                                                        |
| regex_dna                  | 249 ms                                                           | 241 ms: 1.03x faster                                                         |
| python_startup             | 13.2 ms                                                          | 12.8 ms: 1.03x faster                                                        |
| pickle                     | 10.6 us                                                          | 10.3 us: 1.03x faster                                                        |
| gc_traversal               | 4.69 ms                                                          | 4.59 ms: 1.02x faster                                                        |
| thrift                     | 880 us                                                           | 864 us: 1.02x faster                                                         |
| asyncio_tcp                | 378 ms                                                           | 373 ms: 1.01x faster                                                         |
| json_dumps                 | 10.8 ms                                                          | 10.7 ms: 1.01x faster                                                        |
| json                       | 5.35 ms                                                          | 5.31 ms: 1.01x faster                                                        |
| regex_v8                   | 26.0 ms                                                          | 25.8 ms: 1.01x faster                                                        |
| pickle_list                | 4.44 us                                                          | 4.41 us: 1.01x faster                                                        |
| generators                 | 33.5 ms                                                          | 33.6 ms: 1.00x slower                                                        |
| json_loads                 | 25.0 us                                                          | 25.2 us: 1.01x slower                                                        |
| asyncio_tcp_ssl            | 1.58 sec                                                         | 1.59 sec: 1.01x slower                                                       |
| deepcopy_reduce            | 3.39 us                                                          | 3.42 us: 1.01x slower                                                        |
| xml_etree_parse            | 144 ms                                                           | 146 ms: 1.01x slower                                                         |
| async_tree_cpu_io_mixed    | 604 ms                                                           | 617 ms: 1.02x slower                                                         |
| coroutines                 | 22.0 ms                                                          | 22.5 ms: 1.02x slower                                                        |
| pickle_pure_python         | 307 us                                                           | 316 us: 1.03x slower                                                         |
| html5lib                   | 74.7 ms                                                          | 77.2 ms: 1.03x slower                                                        |
| logging_format             | 7.11 us                                                          | 7.39 us: 1.04x slower                                                        |
| gunicorn                   | 1.04 ms                                                          | 1.09 ms: 1.04x slower                                                        |
| xml_etree_process          | 59.7 ms                                                          | 62.4 ms: 1.04x slower                                                        |
| pidigits                   | 254 ms                                                           | 265 ms: 1.04x slower                                                         |
| async_tree_none_tg         | 340 ms                                                           | 356 ms: 1.05x slower                                                         |
| async_tree_cpu_io_mixed_tg | 573 ms                                                           | 600 ms: 1.05x slower                                                         |
| aiohttp                    | 1.07 ms                                                          | 1.12 ms: 1.05x slower                                                        |
| deepcopy                   | 377 us                                                           | 396 us: 1.05x slower                                                         |
| dask                       | 391 ms                                                           | 410 ms: 1.05x slower                                                         |
| logging_silent             | 96.3 ns                                                          | 101 ns: 1.05x slower                                                         |
| xml_etree_generate         | 85.7 ms                                                          | 90.3 ms: 1.05x slower                                                        |
| logging_simple             | 6.40 us                                                          | 6.76 us: 1.06x slower                                                        |
| chameleon                  | 7.40 ms                                                          | 7.82 ms: 1.06x slower                                                        |
| richards_super             | 61.2 ms                                                          | 64.8 ms: 1.06x slower                                                        |
| bench_thread_pool          | 908 us                                                           | 962 us: 1.06x slower                                                         |
| sqlglot_normalize          | 120 ms                                                           | 128 ms: 1.06x slower                                                         |
| regex_effbot               | 3.40 ms                                                          | 3.61 ms: 1.06x slower                                                        |
| tornado_http               | 119 ms                                                           | 127 ms: 1.06x slower                                                         |
| async_tree_memoization_tg  | 421 ms                                                           | 448 ms: 1.07x slower                                                         |
| genshi_xml                 | 58.1 ms                                                          | 62.1 ms: 1.07x slower                                                        |
| docutils                   | 2.98 sec                                                         | 3.20 sec: 1.07x slower                                                       |
| async_generators           | 363 ms                                                           | 390 ms: 1.07x slower                                                         |
| mdp                        | 2.46 sec                                                         | 2.66 sec: 1.08x slower                                                       |
| async_tree_none            | 365 ms                                                           | 395 ms: 1.08x slower                                                         |
| django_template            | 39.0 ms                                                          | 42.2 ms: 1.08x slower                                                        |
| pylint                     | 339 ms                                                           | 369 ms: 1.09x slower                                                         |
| richards                   | 53.4 ms                                                          | 58.3 ms: 1.09x slower                                                        |
| 2to3                       | 291 ms                                                           | 320 ms: 1.10x slower                                                         |
| mypy2                      | 764 ms                                                           | 844 ms: 1.10x slower                                                         |
| sqlglot_transpile          | 1.76 ms                                                          | 1.96 ms: 1.11x slower                                                        |
| pycparser                  | 1.22 sec                                                         | 1.36 sec: 1.11x slower                                                       |
| sqlglot_optimize           | 59.5 ms                                                          | 66.3 ms: 1.11x slower                                                        |
| meteor_contest             | 128 ms                                                           | 143 ms: 1.11x slower                                                         |
| sqlglot_parse              | 1.39 ms                                                          | 1.55 ms: 1.12x slower                                                        |
| xml_etree_iterparse        | 103 ms                                                           | 115 ms: 1.12x slower                                                         |
| sympy_integrate            | 23.2 ms                                                          | 26.1 ms: 1.12x slower                                                        |
| dulwich_log                | 67.3 ms                                                          | 75.8 ms: 1.13x slower                                                        |
| sympy_expand               | 501 ms                                                           | 568 ms: 1.13x slower                                                         |
| deepcopy_memo              | 37.3 us                                                          | 42.5 us: 1.14x slower                                                        |
| sympy_sum                  | 155 ms                                                           | 176 ms: 1.14x slower                                                         |
| genshi_text                | 25.9 ms                                                          | 29.6 ms: 1.14x slower                                                        |
| pathlib                    | 17.1 ms                                                          | 19.6 ms: 1.15x slower                                                        |
| sympy_str                  | 295 ms                                                           | 340 ms: 1.15x slower                                                         |
| deltablue                  | 3.37 ms                                                          | 3.98 ms: 1.18x slower                                                        |
| pprint_safe_repr           | 818 ms                                                           | 980 ms: 1.20x slower                                                         |
| go                         | 165 ms                                                           | 199 ms: 1.20x slower                                                         |
| tomli_loads                | 2.40 sec                                                         | 2.90 sec: 1.21x slower                                                       |
| pprint_pformat             | 1.66 sec                                                         | 2.01 sec: 1.21x slower                                                       |
| python_startup_no_site     | 8.85 ms                                                          | 11.1 ms: 1.25x slower                                                        |
| crypto_pyaes               | 73.6 ms                                                          | 92.2 ms: 1.25x slower                                                        |
| float                      | 80.2 ms                                                          | 101 ms: 1.26x slower                                                         |
| chaos                      | 59.6 ms                                                          | 77.9 ms: 1.31x slower                                                        |
| unpickle_pure_python       | 224 us                                                           | 303 us: 1.35x slower                                                         |
| nqueens                    | 88.4 ms                                                          | 120 ms: 1.36x slower                                                         |
| pyflate                    | 482 ms                                                           | 655 ms: 1.36x slower                                                         |
| raytrace                   | 260 ms                                                           | 355 ms: 1.36x slower                                                         |
| scimark_sor                | 119 ms                                                           | 162 ms: 1.36x slower                                                         |
| mako                       | 10.4 ms                                                          | 14.5 ms: 1.40x slower                                                        |
| scimark_lu                 | 97.5 ms                                                          | 137 ms: 1.40x slower                                                         |
| regex_compile              | 144 ms                                                           | 204 ms: 1.41x slower                                                         |
| scimark_fft                | 312 ms                                                           | 444 ms: 1.42x slower                                                         |
| nbody                      | 87.8 ms                                                          | 130 ms: 1.48x slower                                                         |
| fannkuch                   | 353 ms                                                           | 532 ms: 1.51x slower                                                         |
| comprehensions             | 17.0 us                                                          | 26.1 us: 1.54x slower                                                        |
| scimark_sparse_mat_mult    | 4.28 ms                                                          | 6.61 ms: 1.54x slower                                                        |
| scimark_monte_carlo        | 65.5 ms                                                          | 102 ms: 1.56x slower                                                         |
| hexiom                     | 6.35 ms                                                          | 10.4 ms: 1.64x slower                                                        |
| spectral_norm              | 97.3 ms                                                          | 160 ms: 1.65x slower                                                         |
| Geometric mean             | (ref)                                                            | 1.11x slower                                                                 |

Benchmark hidden because not significant (8): bench_mp_pool, async_tree_memoization, async_tree_io_tg, asyncio_websockets, unpickle_list, sqlite_synth, telco, async_tree_io
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging
Ignored benchmarks (1) of results/bm-20240323-3.13.0a5+-d610d82-PYTHON_UOPS/bm-20240323-pythonperf2-x86_64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82.json: unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.08x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.07x

# Memory
- memory change: 0.98x