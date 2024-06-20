# Results vs. 3.13.0b2

- fork: python
- ref: 15fbd53ba96be4b6a5ab
- machine: linux-x86_64
- commit hash: 15fbd53
- commit date: 2024-04-20
- overall geometric mean: 1.01x faster
- HPT reliability: 97.42%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 291 ms                                                           | 285 ms: 1.02x faster                                                         |
| chameleon      | 7.40 ms                                                          | 7.57 ms: 1.02x slower                                                        |
| html5lib       | 74.7 ms                                                          | 73.1 ms: 1.02x faster                                                        |
| Geometric mean | (ref)                                                            | 1.00x faster                                                                 |

Benchmark hidden because not significant (2): docutils, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-------------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none         | 365 ms                                                           | 373 ms: 1.02x slower                                                         |
| async_tree_cpu_io_mixed | 604 ms                                                           | 618 ms: 1.02x slower                                                         |
| async_tree_io           | 873 ms                                                           | 898 ms: 1.03x slower                                                         |
| Geometric mean          | (ref)                                                            | 1.01x slower                                                                 |

Benchmark hidden because not significant (5): async_tree_io_tg, async_tree_none_tg, async_tree_memoization_tg, async_tree_cpu_io_mixed_tg, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 80.2 ms                                                          | 75.4 ms: 1.06x faster                                                        |
| pidigits       | 254 ms                                                           | 263 ms: 1.04x slower                                                         |
| Geometric mean | (ref)                                                            | 1.01x faster                                                                 |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_v8       | 26.0 ms                                                          | 25.2 ms: 1.03x faster                                                        |
| regex_dna      | 249 ms                                                           | 242 ms: 1.03x faster                                                         |
| regex_compile  | 144 ms                                                           | 143 ms: 1.00x faster                                                         |
| regex_effbot   | 3.40 ms                                                          | 3.51 ms: 1.03x slower                                                        |
| Geometric mean | (ref)                                                            | 1.01x faster                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| tomli_loads          | 2.40 sec                                                         | 2.19 sec: 1.10x faster                                                       |
| unpickle_pure_python | 224 us                                                           | 211 us: 1.07x faster                                                         |
| pickle_dict          | 32.8 us                                                          | 30.8 us: 1.07x faster                                                        |
| unpickle             | 15.7 us                                                          | 14.9 us: 1.05x faster                                                        |
| pickle               | 10.6 us                                                          | 10.2 us: 1.04x faster                                                        |
| xml_etree_generate   | 85.7 ms                                                          | 83.8 ms: 1.02x faster                                                        |
| json_dumps           | 10.8 ms                                                          | 10.6 ms: 1.02x faster                                                        |
| xml_etree_process    | 59.7 ms                                                          | 58.9 ms: 1.01x faster                                                        |
| json_loads           | 25.0 us                                                          | 24.7 us: 1.01x faster                                                        |
| pickle_list          | 4.44 us                                                          | 4.42 us: 1.01x faster                                                        |
| unpickle_list        | 4.70 us                                                          | 4.81 us: 1.02x slower                                                        |
| xml_etree_iterparse  | 103 ms                                                           | 106 ms: 1.04x slower                                                         |
| xml_etree_parse      | 144 ms                                                           | 151 ms: 1.05x slower                                                         |
| Geometric mean       | (ref)                                                            | 1.02x faster                                                                 |

Benchmark hidden because not significant (1): pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|------------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 13.2 ms                                                          | 12.9 ms: 1.02x faster                                                        |
| python_startup_no_site | 8.85 ms                                                          | 8.88 ms: 1.00x slower                                                        |
| Geometric mean         | (ref)                                                            | 1.01x faster                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| django_template | 39.0 ms                                                          | 37.9 ms: 1.03x faster                                                        |
| mako            | 10.4 ms                                                          | 10.1 ms: 1.03x faster                                                        |
| genshi_xml      | 58.1 ms                                                          | 57.2 ms: 1.01x faster                                                        |
| genshi_text     | 25.9 ms                                                          | 27.2 ms: 1.05x slower                                                        |
| Geometric mean  | (ref)                                                            | 1.00x faster                                                                 |

All benchmarks:
===============

| Benchmark                | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|--------------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols | 171 us                                                           | 118 us: 1.45x faster                                                         |
| tomli_loads              | 2.40 sec                                                         | 2.19 sec: 1.10x faster                                                       |
| scimark_monte_carlo      | 65.5 ms                                                          | 60.3 ms: 1.09x faster                                                        |
| bench_mp_pool            | 4.91 ms                                                          | 4.58 ms: 1.07x faster                                                        |
| scimark_fft              | 312 ms                                                           | 291 ms: 1.07x faster                                                         |
| unpickle_pure_python     | 224 us                                                           | 211 us: 1.07x faster                                                         |
| pickle_dict              | 32.8 us                                                          | 30.8 us: 1.07x faster                                                        |
| float                    | 80.2 ms                                                          | 75.4 ms: 1.06x faster                                                        |
| hexiom                   | 6.35 ms                                                          | 5.98 ms: 1.06x faster                                                        |
| richards_super           | 61.2 ms                                                          | 57.6 ms: 1.06x faster                                                        |
| go                       | 165 ms                                                           | 156 ms: 1.06x faster                                                         |
| unpickle                 | 15.7 us                                                          | 14.9 us: 1.05x faster                                                        |
| richards                 | 53.4 ms                                                          | 50.9 ms: 1.05x faster                                                        |
| coroutines               | 22.0 ms                                                          | 21.1 ms: 1.04x faster                                                        |
| create_gc_cycles         | 2.00 ms                                                          | 1.93 ms: 1.04x faster                                                        |
| pickle                   | 10.6 us                                                          | 10.2 us: 1.04x faster                                                        |
| deltablue                | 3.37 ms                                                          | 3.26 ms: 1.04x faster                                                        |
| regex_v8                 | 26.0 ms                                                          | 25.2 ms: 1.03x faster                                                        |
| telco                    | 8.40 ms                                                          | 8.13 ms: 1.03x faster                                                        |
| scimark_sparse_mat_mult  | 4.28 ms                                                          | 4.15 ms: 1.03x faster                                                        |
| sqlite_synth             | 2.80 us                                                          | 2.72 us: 1.03x faster                                                        |
| regex_dna                | 249 ms                                                           | 242 ms: 1.03x faster                                                         |
| django_template          | 39.0 ms                                                          | 37.9 ms: 1.03x faster                                                        |
| mako                     | 10.4 ms                                                          | 10.1 ms: 1.03x faster                                                        |
| raytrace                 | 260 ms                                                           | 254 ms: 1.02x faster                                                         |
| xml_etree_generate       | 85.7 ms                                                          | 83.8 ms: 1.02x faster                                                        |
| logging_simple           | 6.40 us                                                          | 6.26 us: 1.02x faster                                                        |
| 2to3                     | 291 ms                                                           | 285 ms: 1.02x faster                                                         |
| gc_traversal             | 4.69 ms                                                          | 4.58 ms: 1.02x faster                                                        |
| python_startup           | 13.2 ms                                                          | 12.9 ms: 1.02x faster                                                        |
| pprint_safe_repr         | 818 ms                                                           | 800 ms: 1.02x faster                                                         |
| pprint_pformat           | 1.66 sec                                                         | 1.62 sec: 1.02x faster                                                       |
| logging_silent           | 96.3 ns                                                          | 94.3 ns: 1.02x faster                                                        |
| html5lib                 | 74.7 ms                                                          | 73.1 ms: 1.02x faster                                                        |
| nqueens                  | 88.4 ms                                                          | 86.6 ms: 1.02x faster                                                        |
| crypto_pyaes             | 73.6 ms                                                          | 72.2 ms: 1.02x faster                                                        |
| chaos                    | 59.6 ms                                                          | 58.5 ms: 1.02x faster                                                        |
| scimark_lu               | 97.5 ms                                                          | 95.8 ms: 1.02x faster                                                        |
| json_dumps               | 10.8 ms                                                          | 10.6 ms: 1.02x faster                                                        |
| pyflate                  | 482 ms                                                           | 474 ms: 1.02x faster                                                         |
| genshi_xml               | 58.1 ms                                                          | 57.2 ms: 1.01x faster                                                        |
| xml_etree_process        | 59.7 ms                                                          | 58.9 ms: 1.01x faster                                                        |
| logging_format           | 7.11 us                                                          | 7.03 us: 1.01x faster                                                        |
| json_loads               | 25.0 us                                                          | 24.7 us: 1.01x faster                                                        |
| aiohttp                  | 1.07 ms                                                          | 1.06 ms: 1.01x faster                                                        |
| sqlglot_normalize        | 120 ms                                                           | 119 ms: 1.01x faster                                                         |
| gunicorn                 | 1.04 ms                                                          | 1.03 ms: 1.01x faster                                                        |
| sqlglot_parse            | 1.39 ms                                                          | 1.38 ms: 1.01x faster                                                        |
| async_generators         | 363 ms                                                           | 359 ms: 1.01x faster                                                         |
| asyncio_websockets       | 395 ms                                                           | 392 ms: 1.01x faster                                                         |
| coverage                 | 83.5 ms                                                          | 82.9 ms: 1.01x faster                                                        |
| dulwich_log              | 67.3 ms                                                          | 66.8 ms: 1.01x faster                                                        |
| pickle_list              | 4.44 us                                                          | 4.42 us: 1.01x faster                                                        |
| regex_compile            | 144 ms                                                           | 143 ms: 1.00x faster                                                         |
| generators               | 33.5 ms                                                          | 33.4 ms: 1.00x faster                                                        |
| sqlglot_optimize         | 59.5 ms                                                          | 59.3 ms: 1.00x faster                                                        |
| meteor_contest           | 128 ms                                                           | 128 ms: 1.00x faster                                                         |
| python_startup_no_site   | 8.85 ms                                                          | 8.88 ms: 1.00x slower                                                        |
| sympy_integrate          | 23.2 ms                                                          | 23.3 ms: 1.00x slower                                                        |
| sympy_str                | 295 ms                                                           | 296 ms: 1.01x slower                                                         |
| scimark_sor              | 119 ms                                                           | 120 ms: 1.01x slower                                                         |
| sympy_expand             | 501 ms                                                           | 506 ms: 1.01x slower                                                         |
| pathlib                  | 17.1 ms                                                          | 17.3 ms: 1.01x slower                                                        |
| json                     | 5.35 ms                                                          | 5.44 ms: 1.02x slower                                                        |
| mdp                      | 2.46 sec                                                         | 2.50 sec: 1.02x slower                                                       |
| deepcopy_memo            | 37.3 us                                                          | 38.0 us: 1.02x slower                                                        |
| thrift                   | 880 us                                                           | 897 us: 1.02x slower                                                         |
| async_tree_none          | 365 ms                                                           | 373 ms: 1.02x slower                                                         |
| async_tree_cpu_io_mixed  | 604 ms                                                           | 618 ms: 1.02x slower                                                         |
| chameleon                | 7.40 ms                                                          | 7.57 ms: 1.02x slower                                                        |
| unpickle_list            | 4.70 us                                                          | 4.81 us: 1.02x slower                                                        |
| fannkuch                 | 353 ms                                                           | 361 ms: 1.02x slower                                                         |
| async_tree_io            | 873 ms                                                           | 898 ms: 1.03x slower                                                         |
| deepcopy_reduce          | 3.39 us                                                          | 3.50 us: 1.03x slower                                                        |
| regex_effbot             | 3.40 ms                                                          | 3.51 ms: 1.03x slower                                                        |
| pidigits                 | 254 ms                                                           | 263 ms: 1.04x slower                                                         |
| xml_etree_iterparse      | 103 ms                                                           | 106 ms: 1.04x slower                                                         |
| xml_etree_parse          | 144 ms                                                           | 151 ms: 1.05x slower                                                         |
| genshi_text              | 25.9 ms                                                          | 27.2 ms: 1.05x slower                                                        |
| deepcopy                 | 377 us                                                           | 397 us: 1.05x slower                                                         |
| Geometric mean           | (ref)                                                            | 1.01x faster                                                                 |

Benchmark hidden because not significant (20): async_tree_io_tg, bench_thread_pool, nbody, pycparser, docutils, pickle_pure_python, sympy_sum, sqlglot_transpile, asyncio_tcp_ssl, async_tree_none_tg, async_tree_memoization_tg, comprehensions, asyncio_tcp, spectral_norm, tornado_http, async_tree_cpu_io_mixed_tg, mypy2, dask, pylint, async_tree_memoization
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 97.42% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.98x