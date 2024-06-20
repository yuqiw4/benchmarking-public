# Results vs. 3.13.0b2

- fork: python
- ref: d610d821fd210dce63a1
- machine: linux-x86_64
- commit hash: d610d82
- commit date: 2024-03-23
- overall geometric mean: 1.02x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf2-x86_64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 291 ms                                                           | 302 ms: 1.04x slower                                                         |
| chameleon      | 7.40 ms                                                          | 7.29 ms: 1.01x faster                                                        |
| docutils       | 2.98 sec                                                         | 3.04 sec: 1.02x slower                                                       |
| html5lib       | 74.7 ms                                                          | 73.4 ms: 1.02x faster                                                        |
| tornado_http   | 119 ms                                                           | 123 ms: 1.03x slower                                                         |
| Geometric mean | (ref)                                                            | 1.01x slower                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf2-x86_64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|----------------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_memoization     | 460 ms                                                           | 442 ms: 1.04x faster                                                         |
| async_tree_io_tg           | 900 ms                                                           | 868 ms: 1.04x faster                                                         |
| async_tree_cpu_io_mixed_tg | 573 ms                                                           | 588 ms: 1.03x slower                                                         |
| async_tree_memoization_tg  | 421 ms                                                           | 436 ms: 1.04x slower                                                         |
| async_tree_none            | 365 ms                                                           | 385 ms: 1.05x slower                                                         |
| Geometric mean             | (ref)                                                            | 1.01x slower                                                                 |

Benchmark hidden because not significant (3): async_tree_io, async_tree_cpu_io_mixed, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf2-x86_64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 80.2 ms                                                          | 76.2 ms: 1.05x faster                                                        |
| pidigits       | 254 ms                                                           | 262 ms: 1.03x slower                                                         |
| nbody          | 87.8 ms                                                          | 100 ms: 1.14x slower                                                         |
| Geometric mean | (ref)                                                            | 1.04x slower                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf2-x86_64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_v8       | 26.0 ms                                                          | 25.7 ms: 1.01x faster                                                        |
| regex_compile  | 144 ms                                                           | 145 ms: 1.00x slower                                                         |
| regex_effbot   | 3.40 ms                                                          | 3.47 ms: 1.02x slower                                                        |
| Geometric mean | (ref)                                                            | 1.00x slower                                                                 |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf2-x86_64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|----------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| tomli_loads          | 2.40 sec                                                         | 2.14 sec: 1.12x faster                                                       |
| pickle_dict          | 32.8 us                                                          | 30.6 us: 1.07x faster                                                        |
| pickle               | 10.6 us                                                          | 10.2 us: 1.04x faster                                                        |
| unpickle             | 15.7 us                                                          | 15.1 us: 1.04x faster                                                        |
| xml_etree_generate   | 85.7 ms                                                          | 82.9 ms: 1.03x faster                                                        |
| unpickle_list        | 4.70 us                                                          | 4.60 us: 1.02x faster                                                        |
| xml_etree_process    | 59.7 ms                                                          | 58.6 ms: 1.02x faster                                                        |
| json_dumps           | 10.8 ms                                                          | 10.6 ms: 1.01x faster                                                        |
| pickle_list          | 4.44 us                                                          | 4.49 us: 1.01x slower                                                        |
| json_loads           | 25.0 us                                                          | 25.4 us: 1.01x slower                                                        |
| xml_etree_iterparse  | 103 ms                                                           | 104 ms: 1.02x slower                                                         |
| unpickle_pure_python | 224 us                                                           | 230 us: 1.02x slower                                                         |
| xml_etree_parse      | 144 ms                                                           | 147 ms: 1.02x slower                                                         |
| Geometric mean       | (ref)                                                            | 1.02x faster                                                                 |

Benchmark hidden because not significant (1): pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf2-x86_64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|------------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 13.2 ms                                                          | 14.2 ms: 1.08x slower                                                        |
| python_startup_no_site | 8.85 ms                                                          | 12.5 ms: 1.41x slower                                                        |
| Geometric mean         | (ref)                                                            | 1.23x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf2-x86_64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|-----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 10.4 ms                                                          | 10.0 ms: 1.03x faster                                                        |
| django_template | 39.0 ms                                                          | 40.4 ms: 1.04x slower                                                        |
| genshi_xml      | 58.1 ms                                                          | 62.5 ms: 1.08x slower                                                        |
| genshi_text     | 25.9 ms                                                          | 29.2 ms: 1.13x slower                                                        |
| Geometric mean  | (ref)                                                            | 1.05x slower                                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf2-x86_64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|----------------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 171 us                                                           | 121 us: 1.41x faster                                                         |
| create_gc_cycles           | 2.00 ms                                                          | 1.50 ms: 1.33x faster                                                        |
| tomli_loads                | 2.40 sec                                                         | 2.14 sec: 1.12x faster                                                       |
| gc_traversal               | 4.69 ms                                                          | 4.30 ms: 1.09x faster                                                        |
| pickle_dict                | 32.8 us                                                          | 30.6 us: 1.07x faster                                                        |
| richards_super             | 61.2 ms                                                          | 57.2 ms: 1.07x faster                                                        |
| float                      | 80.2 ms                                                          | 76.2 ms: 1.05x faster                                                        |
| richards                   | 53.4 ms                                                          | 50.9 ms: 1.05x faster                                                        |
| async_tree_memoization     | 460 ms                                                           | 442 ms: 1.04x faster                                                         |
| pickle                     | 10.6 us                                                          | 10.2 us: 1.04x faster                                                        |
| async_tree_io_tg           | 900 ms                                                           | 868 ms: 1.04x faster                                                         |
| unpickle                   | 15.7 us                                                          | 15.1 us: 1.04x faster                                                        |
| mako                       | 10.4 ms                                                          | 10.0 ms: 1.03x faster                                                        |
| scimark_sparse_mat_mult    | 4.28 ms                                                          | 4.14 ms: 1.03x faster                                                        |
| xml_etree_generate         | 85.7 ms                                                          | 82.9 ms: 1.03x faster                                                        |
| telco                      | 8.40 ms                                                          | 8.14 ms: 1.03x faster                                                        |
| sqlite_synth               | 2.80 us                                                          | 2.72 us: 1.03x faster                                                        |
| spectral_norm              | 97.3 ms                                                          | 94.9 ms: 1.03x faster                                                        |
| unpickle_list              | 4.70 us                                                          | 4.60 us: 1.02x faster                                                        |
| xml_etree_process          | 59.7 ms                                                          | 58.6 ms: 1.02x faster                                                        |
| html5lib                   | 74.7 ms                                                          | 73.4 ms: 1.02x faster                                                        |
| json_dumps                 | 10.8 ms                                                          | 10.6 ms: 1.01x faster                                                        |
| chameleon                  | 7.40 ms                                                          | 7.29 ms: 1.01x faster                                                        |
| regex_v8                   | 26.0 ms                                                          | 25.7 ms: 1.01x faster                                                        |
| asyncio_websockets         | 395 ms                                                           | 391 ms: 1.01x faster                                                         |
| deepcopy_reduce            | 3.39 us                                                          | 3.36 us: 1.01x faster                                                        |
| generators                 | 33.5 ms                                                          | 33.3 ms: 1.01x faster                                                        |
| asyncio_tcp_ssl            | 1.58 sec                                                         | 1.58 sec: 1.00x slower                                                       |
| regex_compile              | 144 ms                                                           | 145 ms: 1.00x slower                                                         |
| logging_silent             | 96.3 ns                                                          | 96.9 ns: 1.01x slower                                                        |
| deepcopy                   | 377 us                                                           | 380 us: 1.01x slower                                                         |
| coverage                   | 83.5 ms                                                          | 84.1 ms: 1.01x slower                                                        |
| pickle_list                | 4.44 us                                                          | 4.49 us: 1.01x slower                                                        |
| dulwich_log                | 67.3 ms                                                          | 67.9 ms: 1.01x slower                                                        |
| sqlglot_parse              | 1.39 ms                                                          | 1.41 ms: 1.01x slower                                                        |
| json_loads                 | 25.0 us                                                          | 25.4 us: 1.01x slower                                                        |
| meteor_contest             | 128 ms                                                           | 130 ms: 1.02x slower                                                         |
| xml_etree_iterparse        | 103 ms                                                           | 104 ms: 1.02x slower                                                         |
| regex_effbot               | 3.40 ms                                                          | 3.47 ms: 1.02x slower                                                        |
| docutils                   | 2.98 sec                                                         | 3.04 sec: 1.02x slower                                                       |
| deepcopy_memo              | 37.3 us                                                          | 38.0 us: 1.02x slower                                                        |
| sqlglot_normalize          | 120 ms                                                           | 123 ms: 1.02x slower                                                         |
| dask                       | 391 ms                                                           | 399 ms: 1.02x slower                                                         |
| sympy_expand               | 501 ms                                                           | 512 ms: 1.02x slower                                                         |
| unpickle_pure_python       | 224 us                                                           | 230 us: 1.02x slower                                                         |
| xml_etree_parse            | 144 ms                                                           | 147 ms: 1.02x slower                                                         |
| pprint_safe_repr           | 818 ms                                                           | 837 ms: 1.02x slower                                                         |
| sympy_str                  | 295 ms                                                           | 302 ms: 1.03x slower                                                         |
| async_tree_cpu_io_mixed_tg | 573 ms                                                           | 588 ms: 1.03x slower                                                         |
| coroutines                 | 22.0 ms                                                          | 22.6 ms: 1.03x slower                                                        |
| bench_thread_pool          | 908 us                                                           | 936 us: 1.03x slower                                                         |
| sqlglot_transpile          | 1.76 ms                                                          | 1.82 ms: 1.03x slower                                                        |
| pprint_pformat             | 1.66 sec                                                         | 1.71 sec: 1.03x slower                                                       |
| pidigits                   | 254 ms                                                           | 262 ms: 1.03x slower                                                         |
| logging_format             | 7.11 us                                                          | 7.35 us: 1.03x slower                                                        |
| tornado_http               | 119 ms                                                           | 123 ms: 1.03x slower                                                         |
| aiohttp                    | 1.07 ms                                                          | 1.11 ms: 1.04x slower                                                        |
| 2to3                       | 291 ms                                                           | 302 ms: 1.04x slower                                                         |
| django_template            | 39.0 ms                                                          | 40.4 ms: 1.04x slower                                                        |
| async_tree_memoization_tg  | 421 ms                                                           | 436 ms: 1.04x slower                                                         |
| logging_simple             | 6.40 us                                                          | 6.64 us: 1.04x slower                                                        |
| pycparser                  | 1.22 sec                                                         | 1.27 sec: 1.04x slower                                                       |
| sympy_sum                  | 155 ms                                                           | 161 ms: 1.04x slower                                                         |
| go                         | 165 ms                                                           | 172 ms: 1.04x slower                                                         |
| gunicorn                   | 1.04 ms                                                          | 1.09 ms: 1.04x slower                                                        |
| mdp                        | 2.46 sec                                                         | 2.58 sec: 1.05x slower                                                       |
| async_tree_none            | 365 ms                                                           | 385 ms: 1.05x slower                                                         |
| async_generators           | 363 ms                                                           | 383 ms: 1.06x slower                                                         |
| sqlglot_optimize           | 59.5 ms                                                          | 63.0 ms: 1.06x slower                                                        |
| pylint                     | 339 ms                                                           | 361 ms: 1.06x slower                                                         |
| crypto_pyaes               | 73.6 ms                                                          | 78.6 ms: 1.07x slower                                                        |
| mypy2                      | 764 ms                                                           | 818 ms: 1.07x slower                                                         |
| genshi_xml                 | 58.1 ms                                                          | 62.5 ms: 1.08x slower                                                        |
| python_startup             | 13.2 ms                                                          | 14.2 ms: 1.08x slower                                                        |
| sympy_integrate            | 23.2 ms                                                          | 25.1 ms: 1.08x slower                                                        |
| pyflate                    | 482 ms                                                           | 523 ms: 1.08x slower                                                         |
| deltablue                  | 3.37 ms                                                          | 3.70 ms: 1.10x slower                                                        |
| pathlib                    | 17.1 ms                                                          | 19.2 ms: 1.12x slower                                                        |
| genshi_text                | 25.9 ms                                                          | 29.2 ms: 1.13x slower                                                        |
| fannkuch                   | 353 ms                                                           | 398 ms: 1.13x slower                                                         |
| chaos                      | 59.6 ms                                                          | 67.6 ms: 1.13x slower                                                        |
| nbody                      | 87.8 ms                                                          | 100 ms: 1.14x slower                                                         |
| nqueens                    | 88.4 ms                                                          | 102 ms: 1.15x slower                                                         |
| hexiom                     | 6.35 ms                                                          | 7.34 ms: 1.16x slower                                                        |
| comprehensions             | 17.0 us                                                          | 19.6 us: 1.16x slower                                                        |
| scimark_monte_carlo        | 65.5 ms                                                          | 75.9 ms: 1.16x slower                                                        |
| scimark_lu                 | 97.5 ms                                                          | 116 ms: 1.19x slower                                                         |
| raytrace                   | 260 ms                                                           | 311 ms: 1.20x slower                                                         |
| scimark_sor                | 119 ms                                                           | 152 ms: 1.28x slower                                                         |
| python_startup_no_site     | 8.85 ms                                                          | 12.5 ms: 1.41x slower                                                        |
| Geometric mean             | (ref)                                                            | 1.02x slower                                                                 |

Benchmark hidden because not significant (10): bench_mp_pool, async_tree_io, thrift, regex_dna, asyncio_tcp, pickle_pure_python, async_tree_cpu_io_mixed, json, async_tree_none_tg, scimark_fft
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging
Ignored benchmarks (1) of results/bm-20240323-3.13.0a5+-d610d82-JIT/bm-20240323-pythonperf2-x86_64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82.json: unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.11x